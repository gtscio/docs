# Class: ValidationError

Class to handle errors which are triggered by entity validation.

## Hierarchy

- [`BaseError`](BaseError.md)

  ↳ **`ValidationError`**

## Constructors

### constructor

• **new ValidationError**(`source`, `validationObject`, `validationFailures`): [`ValidationError`](ValidationError.md)

Create a new instance of ValidationError.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `source` | `string` | The source of the error. |
| `validationObject` | `string` | The object that failed validation. |
| `validationFailures` | [`IValidationFailure`](../interfaces/IValidationFailure.md)[] | The validation failures. |

#### Returns

[`ValidationError`](ValidationError.md)

#### Overrides

[BaseError](BaseError.md).[constructor](BaseError.md#constructor)

## Properties

### cause

• `Optional` **cause**: `unknown`

#### Inherited from

[BaseError](BaseError.md).[cause](BaseError.md#cause)

___

### inner

• `Optional` **inner**: [`IError`](../interfaces/IError.md)

The inner error if there was one.

#### Inherited from

[BaseError](BaseError.md).[inner](BaseError.md#inner)

___

### message

• **message**: `string`

The message for the error.

#### Inherited from

[BaseError](BaseError.md).[message](BaseError.md#message)

___

### name

• **name**: `string`

The name for the error.

#### Inherited from

[BaseError](BaseError.md).[name](BaseError.md#name)

___

### properties

• `Optional` **properties**: `Object`

Any additional information for the error.

#### Index signature

▪ [id: `string`]: `unknown`

#### Inherited from

[BaseError](BaseError.md).[properties](BaseError.md#properties)

___

### source

• `Optional` **source**: `string`

The source of the error.

#### Inherited from

[BaseError](BaseError.md).[source](BaseError.md#source)

___

### stack

• `Optional` **stack**: `string`

The stack trace for the error.

#### Inherited from

[BaseError](BaseError.md).[stack](BaseError.md#stack)

___

### CLASS\_NAME

▪ `Static` `Readonly` **CLASS\_NAME**: `string`

Runtime name for the class.s

## Methods

### toJsonObject

▸ **toJsonObject**(`includeStack?`): [`IError`](../interfaces/IError.md)

Serialize the error to the error model.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `includeStack?` | `boolean` | Include the stack in the error. |

#### Returns

[`IError`](../interfaces/IError.md)

The error model.

#### Inherited from

[BaseError](BaseError.md).[toJsonObject](BaseError.md#tojsonobject)

___

### expand

▸ **expand**(`errors`): `undefined` \| [`IError`](../interfaces/IError.md)

Expand an error tree.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `errors` | `undefined` \| [`IError`](../interfaces/IError.md)[] | The list of errors to expand. |

#### Returns

`undefined` \| [`IError`](../interfaces/IError.md)

The first level error.

#### Inherited from

[BaseError](BaseError.md).[expand](BaseError.md#expand)

___

### flatten

▸ **flatten**(`err`): [`IError`](../interfaces/IError.md)[]

Flatten an error tree.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `err` | `unknown` | The starting error. |

#### Returns

[`IError`](../interfaces/IError.md)[]

The list of all internal errors.

#### Inherited from

[BaseError](BaseError.md).[flatten](BaseError.md#flatten)

___

### fromError

▸ **fromError**(`err`): [`BaseError`](BaseError.md)

Construct an error from an existing one.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `err` | `unknown` | The existing error. |

#### Returns

[`BaseError`](BaseError.md)

The new instance.

#### Inherited from

[BaseError](BaseError.md).[fromError](BaseError.md#fromerror)

___

### isErrorCode

▸ **isErrorCode**(`error`, `code`): `boolean`

Test to see if the error has the specified error code.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `code` | `string` \| `RegExp` | The code to check for. |

#### Returns

`boolean`

True if the error has the code.

#### Inherited from

[BaseError](BaseError.md).[isErrorCode](BaseError.md#iserrorcode)

___

### isErrorMessage

▸ **isErrorMessage**(`error`, `message`): error is BaseError

Test to see if the error has the specified error message.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `message` | `string` \| `RegExp` | The message to check for. |

#### Returns

error is BaseError

True if the error has the name.

#### Inherited from

[BaseError](BaseError.md).[isErrorMessage](BaseError.md#iserrormessage)

___

### isErrorName

▸ **isErrorName**(`error`, `name`): error is BaseError

Test to see if the error has the specified error name.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `name` | `string` \| `RegExp` | The name to check for. |

#### Returns

error is BaseError

True if the error has the name.

#### Inherited from

[BaseError](BaseError.md).[isErrorName](BaseError.md#iserrorname)

___

### someErrorCode

▸ **someErrorCode**(`error`, `code`): error is BaseError

Test to see if any of the errors or children have the given error code.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `code` | `string` \| `RegExp` | The code to check for. |

#### Returns

error is BaseError

True if the error has the name.

#### Inherited from

[BaseError](BaseError.md).[someErrorCode](BaseError.md#someerrorcode)

___

### someErrorMessage

▸ **someErrorMessage**(`error`, `message`): error is BaseError

Test to see if any of the errors or children have the given error message.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `message` | `string` \| `RegExp` | The message to check for. |

#### Returns

error is BaseError

True if the error has the name.

#### Inherited from

[BaseError](BaseError.md).[someErrorMessage](BaseError.md#someerrormessage)

___

### someErrorName

▸ **someErrorName**(`error`, `name`): error is BaseError

Test to see if any of the errors or children have the given error name.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | `unknown` | The error to test. |
| `name` | `string` \| `RegExp` | The name to check for. |

#### Returns

error is BaseError

True if the error has the name.

#### Inherited from

[BaseError](BaseError.md).[someErrorName](BaseError.md#someerrorname)
