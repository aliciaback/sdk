**@gala-chain/api** ∙ [API](../exports.md)

***

[API](../exports.md) > TransferTokenDto

# Class: TransferTokenDto

## Contents

- [Extends](TransferTokenDto.md#extends)
- [Constructors](TransferTokenDto.md#constructors)
  - [new TransferTokenDto()](TransferTokenDto.md#new-transfertokendto)
- [Properties](TransferTokenDto.md#properties)
  - [from](TransferTokenDto.md#from)
  - [quantity](TransferTokenDto.md#quantity)
  - [signature](TransferTokenDto.md#signature)
  - [signerPublicKey](TransferTokenDto.md#signerpublickey)
  - [to](TransferTokenDto.md#to)
  - [tokenInstance](TransferTokenDto.md#tokeninstance)
  - [trace](TransferTokenDto.md#trace)
  - [uniqueKey](TransferTokenDto.md#uniquekey)
  - [useAllowances](TransferTokenDto.md#useallowances)
  - [ENCODING](TransferTokenDto.md#encoding)
- [Methods](TransferTokenDto.md#methods)
  - [isSignatureValid()](TransferTokenDto.md#issignaturevalid)
  - [serialize()](TransferTokenDto.md#serialize)
  - [sign()](TransferTokenDto.md#sign)
  - [signed()](TransferTokenDto.md#signed)
  - [validate()](TransferTokenDto.md#validate)
  - [validateOrReject()](TransferTokenDto.md#validateorreject)
  - [deserialize()](TransferTokenDto.md#deserialize)

## Extends

- [`ChainCallDTO`](ChainCallDTO.md)

## Constructors

### new TransferTokenDto()

> **new TransferTokenDto**(): [`TransferTokenDto`](TransferTokenDto.md)

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`constructor`](ChainCallDTO.md#constructors)

## Properties

### from

> **from**?: `string`

#### Source

[chain-api/src/types/token.ts:486](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/token.ts#L486)

***

### quantity

> **quantity**: `BigNumber`

#### Source

[chain-api/src/types/token.ts:507](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/token.ts#L507)

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

### to

> **to**: `string`

#### Source

[chain-api/src/types/token.ts:489](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/token.ts#L489)

***

### tokenInstance

> **tokenInstance**: [`TokenInstanceKey`](TokenInstanceKey.md)

#### Source

[chain-api/src/types/token.ts:499](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/token.ts#L499)

***

### trace

> **trace**?: [`TraceContext`](../interfaces/TraceContext.md)

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`trace`](ChainCallDTO.md#trace)

#### Source

[chain-api/src/types/dtos.ts:99](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L99)

***

### uniqueKey

> **uniqueKey**?: `string`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`uniqueKey`](ChainCallDTO.md#uniquekey)

#### Source

[chain-api/src/types/dtos.ts:114](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L114)

***

### useAllowances

> **useAllowances**?: `string`[]

#### Source

[chain-api/src/types/token.ts:515](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/token.ts#L515)

***

### ENCODING

> **`static`** **`readonly`** **ENCODING**: `"base64"` = `"base64"`

#### Inherited from

[`ChainCallDTO`](ChainCallDTO.md).[`ENCODING`](ChainCallDTO.md#encoding)

#### Source

[chain-api/src/types/dtos.ts:100](https://github.com/GalaChain/sdk/blob/bcbbb18/chain-api/src/types/dtos.ts#L100)

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

> **signed**(`privateKey`, `useDer`): [`TransferTokenDto`](TransferTokenDto.md)

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