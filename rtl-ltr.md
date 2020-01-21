# rtl-ltr

for **multiple language admin panel**, base on the [language (Internationalization)](/translation.md) that displays, theme should work in that direction:

## rtl

we have multiple solution to create css code that fully support rtl direction.
lets check 3 main solution.

1. separate rtl and ltr css files.
2. scss config file: rtl, ltr variables.
3. scss rtl align fix.

### 1-separate files

in this scenario we have our ltr css file(s) working properly.

1. for each file (or one css file like bootstrap.css) we should create one rtl file and we load the rtl or ltr file(s) in document whenever it needed.

2. or we can load ltr css file(s) and append needed rtl file(s) at the end.

> you can find bootstrap or other css framwork rtl file that writen by developers.

### 2-scss config file: rtl, ltr variables

two config files: rtl & ltr variable needed, and finaly create two css bundle file base on these configs.

```ltr variables```
```
$dir-mode-direction         : ltr;
$dir-mode-direction-inverse : rtl;
$dir-mode-align             : left;
$dir-mode-align-inverse     : right;
```

```rtl variables```
```
$dir-mode-direction         : rtl;
$dir-mode-direction-inverse : ltr;
$dir-mode-align             : right;
$dir-mode-align-inverse     : left;
```

now in all scss files we should replace align values with these variables.

for example:
```
.card-title {
    text-align: $dir-mode-align;
}
.bordered-inverse-2 {
    border-#{$dir-mode-align-inverse}: 2px solid;
}
```

### 3-scss rtl align fix

in scss or css files we can add **rtl align fix code**, in this solution for changing app direction, no extra binding needed.
you should add *rtl* class to *body tag* in *rtl direction*.

for rtl fix we can do these two ways:

original css code:
```
.wrapper-class {
    .inner-class {
        left: 1rem;
    }
}
```

#### 1

```
.wrapper-class {
    .inner-class {
        body:not(.rtl) & {
            left: 1rem;
        }
        body.rtl & {
            right: 1rem;
        }
    }
}
```

#### 2

```
body:not(.rtl) {
    .wrapper-class {
        .inner-class {
            left: 1rem;
        }
    }
}
body.rtl {
    .wrapper-class {
        .inner-class {
            right: 1rem;
        }
    }
}
```

## ltr

the default behaviar of html and style code are *ltr*, so in this case, all css code or css framework work as it should.
