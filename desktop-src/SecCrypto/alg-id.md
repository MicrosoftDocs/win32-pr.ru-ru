---
description: Задает идентификатор алгоритма.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664639"
---
# <a name="alg_id"></a>ALG_ID

Тип данных **ALG_ID** задает идентификатор алгоритма. Параметры этого типа данных передаются большинству функций в CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



В следующей таблице перечислены идентификаторы алгоритмов, которые в настоящее время определены. Авторы пользовательских [*поставщиков служб шифрования*](../secgloss/c-gly.md) (CSP) могут определять новые значения. Кроме того, **ALG_ID** , используемые пользовательскими CSP для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , являются зависимыми от поставщика. Текущие сопоставления следуют таблице.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Идентификатор</th>
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td>Алгоритм шифрования <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> .</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td><a href="/windows/desktop/SecGloss/t-gly"><em>Тройное шифрование Triple DES</em></a> с действующей длиной ключа, равной 112 битам.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>AES (AES). Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>128 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>192 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>256 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Временный идентификатор алгоритма для дескрипторов согласованных ключей Диффи-Хелмана.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Алгоритм для создания 40-разрядного ключа DES с битами четности и нулевыми битами ключа для обеспечения длины ключа 64 бит. Этот алгоритм поддерживается в <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>Алгоритм шифрования DES.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>Алгоритм шифрования DESX.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Алгоритм обмена ключами с временным ключом Diffie-Hellman.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Алгоритм обмена ключами с Diffie-Hellman Store и forward.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>Алгоритм подписи <a href="/windows/desktop/SecGloss/p-gly"><em>открытого ключа</em></a> DSA.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Алгоритм обмена ключами на эллиптической кривой Diffie-Hellman.
<blockquote>
[!Note]<br />
Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.
</blockquote>
<br/> <strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Многовременная эллиптическая кривая Diffie-Hellman алгоритм обмена ключами.
<blockquote>
[!Note]<br />
Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.
</blockquote>
<br/> <strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Алгоритм цифровых подписей на основе эллиптических кривых.
<blockquote>
[!Note]<br />
Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.
</blockquote>
<br/> <strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Алгоритм обмена ключами на эллиптических кривых Менезес, qu и Ванстоне (МКВ). Этот алгоритм не поддерживается.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Один из способов хэширования функций.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Алгоритм хэширования MD5 Хьюз.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>Хэш-алгоритм с ключом HMAC. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>Алгоритм обмена ключами Кеа (FORTEZZA). Этот алгоритм не поддерживается.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td>Хэш-алгоритм с ключом <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>Алгоритм хэширования MD2. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>Алгоритм хэширования MD4.</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>Алгоритм хэширования MD5. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>Нет алгоритма подписи.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xFFFFFFFF</td>
<td>Алгоритм реализуется только в CNG. Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>Алгоритм определяется в закодированных параметрах. Алгоритм поддерживается только с помощью CNG. Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>Алгоритм шифрования блока RC2. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>Алгоритм шифрования потока RC4. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>Алгоритм шифрования блока RC5.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>Алгоритм обмена открытыми ключами RSA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>Алгоритм подписи открытого ключа RSA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>Запечатайте алгоритм шифрования. Этот алгоритм не поддерживается.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>Алгоритм хэширования SHA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>То же, что и <strong>CALG_SHA</strong>. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>256-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается в поставщике служб шифрования Microsoft Enhanced RSA и AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br/> <strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>384-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br/> <strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>512-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br/> <strong>Windows XP с пакетом обновления 2 (SP2), Windows XP с пакетом обновления SP1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Алгоритм шифрования блоков Skipjack (FORTEZZA). Этот алгоритм не поддерживается.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>ТЕК (FORTEZZA). Этот алгоритм не поддерживается.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями.</td>
</tr>
</tbody>
</table>



 

Для [базового поставщика служб шифрования Майкрософт](microsoft-base-cryptographic-provider.md), [поставщика строгой криптографии](microsoft-strong-cryptographic-provider.md)(Майкрософт) и [расширенного поставщика служб шифрования Майкрософт](microsoft-enhanced-cryptographic-provider.md) **ALG_IDs** , используемые для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , приведены ниже.

-   **CALG_RSA_KEYX** используется для **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** используется для **AT_SIGNATURE**.

Для [поставщика служб шифрования Microsoft Base DSS и Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md) **ALG_IDs** , используемый для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , выглядит следующим образом:

-   **CALG_DH_SF** используется для **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** используется для **AT_SIGNATURE**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические функции](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**криптфиндоидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
