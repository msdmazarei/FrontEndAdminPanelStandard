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

> separate words (key) with "**_**", for example "**insert_username_or_mobile: 'insert username or mobile'**"

## Example

### react

```localization.ts```

```
import LocalizedStrings, { LocalizedStringsMethods } from 'react-localization';
import { fa } from './fa';
import { en } from './en';

interface ILocalization extends LocalizedStringsMethods {
    name: string;
    register: String;
    insert_username_or_mobile: string;
    user_x_online: String;
}

export const Localization: ILocalization = new LocalizedStrings({
    fa: fa,
    en: en
});

Localization.setLanguage('fa'); // --> OR from App Setup file
```

```fa.ts```
```
export const fa = {
    name: "نام",
    register: "ثبت نام",
    insert_username_or_mobile: 'نام کاربری یا شماره تلفن همراه را وارد کنید',
    user_x_online: 'کاربر با نام کاربری {0} آنلاین شد'
}
```

```en.ts```
```
export const en = {
    name: "name",
    register: "register",
    insert_username_or_mobile: 'insert username or mobile',
    user_x_online: 'user with username {0} is online now'
}
```

```in template```

```Localization.name```

```Localization.formatString(Localization.user_x_online, 'jafar')```

for more information see [react-localization](https://www.npmjs.com/package/react-localization)
