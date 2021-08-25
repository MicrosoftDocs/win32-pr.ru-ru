---
description: Задает идентификатор алгоритма.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482400"
---
# <a name="alg_id"></a>ALG_ID

Тип данных **ALG_ID** задает идентификатор алгоритма. Параметры этого типа данных передаются большинству функций в CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



В следующей таблице перечислены идентификаторы алгоритмов, которые в настоящее время определены. Авторы пользовательских [*поставщиков служб шифрования*](../secgloss/c-gly.md) (CSP) могут определять новые значения. Кроме того, **ALG_ID** , используемые пользовательскими CSP для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , являются зависимыми от поставщика. Текущие сопоставления следуют таблице.




| Идентификатор | Значение | Описание | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | Алгоритм шифрования <a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> . | 
| CALG_3DES_112 | 0x00006609 | <a href="/windows/desktop/SecGloss/t-gly"><em>Тройное шифрование Triple DES</em></a> с действующей длиной ключа, равной 112 битам. | 
| CALG_AES | 0x00006611 | AES (AES). Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>. | 
| CALG_AES_128 | 0x0000660e | 128 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>. | 
| CALG_AES_192 | 0x0000660f | 192 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>. | 
| CALG_AES_256 | 0x00006610 | 256 разрядов AES. Этот алгоритм поддерживается <a href="microsoft-aes-cryptographic-provider.md">поставщиком служб шифрования Microsoft AES</a>. | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Временный идентификатор алгоритма для дескрипторов согласованных ключей Диффи-Хелмана. | 
| CALG_CYLINK_MEK | 0x0000660c | Алгоритм для создания 40-разрядного ключа DES с битами четности и нулевыми битами ключа для обеспечения длины ключа 64 бит. Этот алгоритм поддерживается в <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_DES | 0x00006601 | Алгоритм шифрования DES. | 
| CALG_DESX | 0x00006604 | Алгоритм шифрования DESX. | 
| CALG_DH_EPHEM | 0x0000aa02 | Алгоритм обмена ключами с временным ключом Diffie-Hellman. | 
| CALG_DH_SF | 0x0000aa01 | Алгоритм обмена ключами с Diffie-Hellman Store и forward. | 
| CALG_DSS_SIGN | 0x00002200 | Алгоритм подписи <a href="/windows/desktop/SecGloss/p-gly"><em>открытого ключа</em></a> DSA. | 
| CALG_ECDH | 0x0000aa05 | Алгоритм обмена ключами на эллиптической кривой Diffie-Hellman.<blockquote>[!Note]<br />Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</blockquote><br /><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Многовременная эллиптическая кривая Diffie-Hellman алгоритм обмена ключами.<blockquote>[!Note]<br />Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</blockquote><br /><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_ECDSA | 0x00002203 | Алгоритм цифровых подписей на основе эллиптических кривых.<blockquote>[!Note]<br />Этот алгоритм поддерживается только через <a href="/windows/desktop/SecCNG/cng-portal">API шифрования: следующее поколение</a>.</blockquote><br /><strong>Windows Server 2003 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_ECMQV | 0x0000a001 | Алгоритм обмена ключами на эллиптических кривых Менезес, qu и Ванстоне (МКВ). Этот алгоритм не поддерживается. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Один из способов хэширования функций. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Алгоритм хэширования MD5 Хьюз. | 
| CALG_HMAC | 0x00008009 | Хэш-алгоритм с ключом HMAC. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_KEA_KEYX | 0x0000aa04 | Алгоритм обмена ключами Кеа (FORTEZZA). Этот алгоритм не поддерживается. | 
| CALG_MAC | 0x00008005 | Хэш-алгоритм с ключом <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_MD2 | 0x00008001 | Алгоритм хэширования MD2. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_MD4 | 0x00008002 | Алгоритм хэширования MD4. | 
| CALG_MD5 | 0x00008003 | Алгоритм хэширования MD5. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_NO_SIGN | 0x00002000 | Нет алгоритма подписи. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | Алгоритм реализуется только в CNG. Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | Алгоритм определяется в закодированных параметрах. Алгоритм поддерживается только с помощью CNG. Макрос IS_SPECIAL_OID_INFO_ALGID можно использовать, чтобы определить, поддерживается ли алгоритм шифрования только с помощью функций CNG. | 
| CALG_PCT1_MASTER | 0x00004c04 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_RC2 | 0x00006602 | Алгоритм шифрования блока RC2. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_RC4 | 0x00006801 | Алгоритм шифрования потока RC4. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_RC5 | 0x0000660d | Алгоритм шифрования блока RC5. | 
| CALG_RSA_KEYX | 0x0000a400 | Алгоритм обмена открытыми ключами RSA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_RSA_SIGN | 0x00002400 | Алгоритм подписи открытого ключа RSA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_SEAL | 0x00006802 | Запечатайте алгоритм шифрования. Этот алгоритм не поддерживается. | 
| CALG_SHA | 0x00008004 | Алгоритм хэширования SHA. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_SHA1 | 0x00008004 | То же, что и <strong>CALG_SHA</strong>. Этот алгоритм поддерживается в <a href="microsoft-base-cryptographic-provider.md">базовом поставщике служб шифрования Майкрософт</a>. | 
| CALG_SHA_256 | 0x0000800c | 256-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается в поставщике служб шифрования Microsoft Enhanced RSA и AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br /><strong>Windows xp с пакетом обновления 2 (SP2), Windows XP с пакетом обновления 1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_SHA_384 | 0x0000800d | 384-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br /><strong>Windows xp с пакетом обновления 2 (SP2), Windows XP с пакетом обновления 1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_SHA_512 | 0x0000800e | 512-разрядный алгоритм хэширования SHA. Этот алгоритм поддерживается поставщиком служб Microsoft Enhanced RSA and AES. <strong>Windows XP с пакетом обновления 3 (SP3):</strong> Этот алгоритм поддерживается в расширенном поставщике шифрования RSA и AES (прототипе) Майкрософт.<br /><strong>Windows xp с пакетом обновления 2 (SP2), Windows XP с пакетом обновления 1 и Windows XP:</strong> Этот алгоритм не поддерживается.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Алгоритм шифрования блоков Skipjack (FORTEZZA). Этот алгоритм не поддерживается. | 
| CALG_SSL2_MASTER | 0x00004c05 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_SSL3_MASTER | 0x00004c01 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_TEK | 0x0000660b | ТЕК (FORTEZZA). Этот алгоритм не поддерживается. | 
| CALG_TLS1_MASTER | 0x00004c06 | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 
| CALG_TLS1PRF | 0x0000800a | Используется системой Schannel.dllных операций. Эта <strong>ALG_ID</strong> не должна использоваться приложениями. | 




 

Для [базового поставщика служб шифрования Майкрософт](microsoft-base-cryptographic-provider.md), [поставщика строгой криптографии](microsoft-strong-cryptographic-provider.md)(Майкрософт) и [расширенного поставщика служб шифрования Майкрософт](microsoft-enhanced-cryptographic-provider.md) **ALG_IDs** , используемые для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , приведены ниже.

-   **CALG_RSA_KEYX** используется для **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** используется для **AT_SIGNATURE**.

Для [поставщика служб шифрования Microsoft Base DSS и Diffie-Hellman](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md) **ALG_IDs** , используемый для ключевых спецификаций **AT_KEYEXCHANGE** и **AT_SIGNATURE** , выглядит следующим образом:

-   **CALG_DH_SF** используется для **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** используется для **AT_SIGNATURE**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Винкрипт. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Криптографические функции](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**криптфиндоидинфо**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
