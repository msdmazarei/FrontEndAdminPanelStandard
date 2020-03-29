# CatodFormElement

CatodFormElement is abstract class and it's look like this:

```
export interface ICatodFormElementState {
    
}

export interface ICatodFormElementProps {
    defaultValue?: any;
    onChange?: (value: any, isValid: boolean) => void;
    elRef?: (elName: HTMLElement) => void;
    pattern?: RegExp;
    patternError?: string;
    label?: string;
    required?: boolean;
    validationFunc?: (value: any) => boolean;
    placeholder?: string;
    readOnly?: boolean;
    disabled?: boolean;
    hideError?: boolean;
    hideErrorMsg?: boolean;
    className?: string;
}

export abstract class CatodFormElement<
    P extends ICatodFormElementProps,
    S extends ICatodFormElementState
    >
    extends BaseComponent<P, S> {

}
```