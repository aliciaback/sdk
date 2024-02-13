**@gala-chain/api** ∙ [API](../exports.md)

***

[API](../exports.md) > FetchAllowancesDto

# Class: FetchAllowancesDto

## Contents

- [Extends](FetchAllowancesDto.md#extends)
- [Constructors](FetchAllowancesDto.md#constructors)
  - [new FetchAllowancesDto()](FetchAllowancesDto.md#new-fetchallowancesdto)
- [Properties](FetchAllowancesDto.md#properties)
  - [additionalKey](FetchAllowancesDto.md#additionalkey)
  - [allowanceType](FetchAllowancesDto.md#allowancetype)
  - [bookmark](FetchAllowancesDto.md#bookmark)
  - [category](FetchAllowancesDto.md#category)
  - [collection](FetchAllowancesDto.md#collection)
  - [grantedBy](FetchAllowancesDto.md#grantedby)
  - [grantedTo](FetchAllowancesDto.md#grantedto)
  - [instance](FetchAllowancesDto.md#instance)
  - [limit](FetchAllowancesDto.md#limit)
  - [signature](FetchAllowancesDto.md#signature)
  - [signerPublicKey](FetchAllowancesDto.md#signerpublickey)
  - [trace](FetchAllowancesDto.md#trace)
  - [type](FetchAllowancesDto.md#type)
  - [uniqueKey](FetchAllowancesDto.md#uniquekey)
  - [DEFAULT\_LIMIT](FetchAllowancesDto.md#default-limit)
  - [ENCODING](FetchAllowancesDto.md#encoding)
  - [MAX\_LIMIT](FetchAllowancesDto.md#max-limit)
- [Methods](FetchAllowancesDto.md#methods)
  - [isSignatureValid()](FetchAllowancesDto.md#issignaturevalid)
  - [serialize()](FetchAllowancesDto.md#serialize)
  - [sign()](FetchAllowancesDto.md#sign)
  - [signed()](FetchAllowancesDto.md#signed)
  - [validate()](FetchAllowancesDto.md#validate)
  - [validateOrReject()](FetchAllowancesDto.md#validateorreject)
  - [deserialize()](FetchAllowancesDto.md#deserialize)

## Extends

- [`ChainCallDTO`](ChainCallDTO.md)

## Constructors

### new FetchAllowancesDto()

> **new FetchAllowancesDto**(): [`FetchAllowancesDto`](FetchAllowancesDto.md)

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`constructor`](ChainCallDTO.md#constructors)

## Properties

### additionalKey

> **additionalKey**?: `string`

#### Source

[chain-api/src/types/allowance.ts:78](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L78)

***

### allowanceType

> **allowanceType**?: [`AllowanceType`](../enumerations/AllowanceType.md)

#### Source

[chain-api/src/types/allowance.ts:89](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L89)

***

### bookmark

> **bookmark**?: `string`

#### Source

[chain-api/src/types/allowance.ts:103](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L103)

***

### category

> **category**?: `string`

#### Source

[chain-api/src/types/allowance.ts:64](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L64)

***

### collection

> **collection**?: `string`

#### Source

[chain-api/src/types/allowance.ts:57](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L57)

***

### grantedBy

> **grantedBy**?: `string`

#### Source

[chain-api/src/types/allowance.ts:96](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L96)

***

### grantedTo

> **grantedTo**: `string`

#### Source

[chain-api/src/types/allowance.ts:50](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L50)

***

### instance

> **instance**?: `string`

#### Source

[chain-api/src/types/allowance.ts:85](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L85)

***

### limit

> **limit**?: `number`

#### Source

[chain-api/src/types/allowance.ts:115](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L115)

***

### signature

> **signature**?: `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`signature`](ChainCallDTO.md#signature)

#### Source

[chain-api/src/types/dtos.ts:134](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L134)

***

### signerPublicKey

> **signerPublicKey**?: `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`signerPublicKey`](ChainCallDTO.md#signerpublickey)

#### Source

[chain-api/src/types/dtos.ts:143](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L143)

***

### trace

> **trace**?: [`TraceContext`](../interfaces/TraceContext.md)

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`trace`](ChainCallDTO.md#trace)

#### Source

[chain-api/src/types/dtos.ts:99](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L99)

***

### type

> **type**?: `string`

#### Source

[chain-api/src/types/allowance.ts:71](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L71)

***

### uniqueKey

> **uniqueKey**?: `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`uniqueKey`](ChainCallDTO.md#uniquekey)

#### Source

[chain-api/src/types/dtos.ts:114](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L114)

***

### DEFAULT\_LIMIT

> **`static`** **`readonly`** **DEFAULT\_LIMIT**: `1000` = `1000`

#### Source

[chain-api/src/types/allowance.ts:44](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L44)

***

### ENCODING

> **`static`** **`readonly`** **ENCODING**: `"base64"` = `"base64"`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`ENCODING`](ChainCallDTO.md#encoding)

#### Source

[chain-api/src/types/dtos.ts:100](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L100)

***

### MAX\_LIMIT

> **`static`** **`readonly`** **MAX\_LIMIT**: `number`

#### Source

[chain-api/src/types/allowance.ts:43](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/allowance.ts#L43)

## Methods

### isSignatureValid()

> **isSignatureValid**(`publicKey`): `boolean`

#### Parameters

▪ **publicKey**: `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`isSignatureValid`](ChainCallDTO.md#issignaturevalid)

#### Source

[chain-api/src/types/dtos.ts:185](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L185)

***

### serialize()

> **serialize**(): `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`serialize`](ChainCallDTO.md#serialize)

#### Source

[chain-api/src/types/dtos.ts:157](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L157)

***

### sign()

> **sign**(`privateKey`, `useDer`): `void`

#### Parameters

▪ **privateKey**: `string`

▪ **useDer**: `boolean`= `false`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`sign`](ChainCallDTO.md#sign)

#### Source

[chain-api/src/types/dtos.ts:168](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L168)

***

### signed()

> **signed**(`privateKey`, `useDer`): [`FetchAllowancesDto`](FetchAllowancesDto.md)

Creates a signed copy of current object.

#### Parameters

▪ **privateKey**: `string`

▪ **useDer**: `boolean`= `false`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`signed`](ChainCallDTO.md#signed)

#### Source

[chain-api/src/types/dtos.ts:179](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L179)

***

### validate()

> **validate**(): `Promise`\<`ValidationError`[]\>

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`validate`](ChainCallDTO.md#validate)

#### Source

[chain-api/src/types/dtos.ts:145](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L145)

***

### validateOrReject()

> **validateOrReject**(): `Promise`\<`void`\>

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`validateOrReject`](ChainCallDTO.md#validateorreject)

#### Source

[chain-api/src/types/dtos.ts:149](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L149)

***

### deserialize()

> **`static`** **deserialize**\<`T`\>(`constructor`, `object`): `T`

#### Type parameters

▪ **T**

#### Parameters

▪ **constructor**: [`ClassConstructor`](../interfaces/ClassConstructor.md)\<[`Inferred`](../type-aliases/Inferred.md)\<`T`, [`ChainCallDTO`](ChainCallDTO.md)\>\>

▪ **object**: `string` \| `Record`\<`string`, `unknown`\> \| `Record`\<`string`, `unknown`\>[]

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`deserialize`](ChainCallDTO.md#deserialize)

#### Source

[chain-api/src/types/dtos.ts:161](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L161)