# TRANSLATION

```
interface IInternationalization {
    rtl: boolean;
    language: string;
    flag: string;
}

sample:
    interface IInternationalization_fa extends IInternationalization {
        rtl: true;
        language: 'فارسی';
        flag: 'fa';
    }
    interface IInternationalization_en extends IInternationalization {
        rtl: false;
        language: 'english';
        flag: 'en';
    }
```

```
interface ILocalization_tr {
    [key: string]: string | ILocalization_tr;
}
```

> app has supported **Internationalization list** (language dictionary included in app (ILocalization_tr)).
> all **hard coded word and sentense** must translate using current app flag.
> all **msg** and **notify** must shown in current language.
