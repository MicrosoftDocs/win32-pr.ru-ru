---
description: Указывает тип поставщика служб шифрования (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: Перечисление CAPICOM_PROV_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879024"
---
# <a name="capicom_prov_type-enumeration"></a>\_ \_ Перечисление типов CAPICOM Prov

Перечисление **\_ \_ типа CAPICOM Prov** указывает тип [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Элементы



| Член                             | Описание                                                                                                                                                                                                                                                                                                                                                                        | Значение |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Prov \_ RSA \_ Full**       | Полный CSP [*RSA*](../secgloss/r-gly.md) . Этот тип поставщика поддерживает [*цифровые подписи*](../secgloss/d-gly.md) и [*Шифрование*](../secgloss/e-gly.md)данных.<br/>                                                            | 1     |
| **CAPICOM \_ Prov \_ RSA \_ SIG**        | Подмножество CSP RSA, которое поддерживает только те функции и алгоритмы, которые необходимы для хэширования и цифровых подписей.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ Prov \_ DSS**             | CSP [*стандарта цифровой подписи*](../secgloss/d-gly.md) (DSS). Этот тип поставщика поддерживает только хэши и Цифровые подписи. DSS использует [*алгоритм цифровых подписей*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **CAPICOM \_ Prov \_ Fortezza**        | CSP, содержащий криптографические протоколы и алгоритмы, принадлежащие [*национальным институтам стандартов и технологий*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM \_ Prov \_ MS \_ Exchange**    | CSP, разработанный для криптографических потребностей Exchange и других приложений, совместимых с Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ Prov \_ SSL**             | CSP, поддерживающий протокол [*SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ Prov \_ RSA \_ SChannel**   | CSP, поддерживающий протоколы [*RSA*](../secgloss/r-gly.md) и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ Prov \_ DSS \_ DH**         | CSP, поддерживающий протоколы DSS и [*Диффи-Хелмана*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ Prov \_ EC \_ , \_ подпись**  | CSP, который поддерживает функции алгоритма цифровых подписей на основе эллиптических кривых (ECDSA) и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ Prov \_ EC \_ екнра \_ SIG**  | CSP, поддерживающий эллиптическую кривую Nyberg-Rueppel аналоговые (ЕКНРА) функции и алгоритмы, необходимые для цифровых подписей.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ Prov \_ EC \_ ECDSA \_ Full** | CSP, поддерживающий полное значение ECDSA.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ Prov \_ EC \_ екнра \_ Full** | CSP, поддерживающий полную ЕКНРА.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ Prov \_ DH \_ SChannel**    | CSP, поддерживающий протоколы [*Диффи-Хелмана*](../secgloss/d-gly.md) и [*SChannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ Prov \_ спирус \_ Линкс**   | CSP, поддерживающий устройство СПИРУС Линкс Card.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ Prov \_ РНГ**             | CSP, обрабатывающий генерацию случайных чисел.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ Prov \_ Intel \_ sec**      | CSP, обеспечивающий безопасность Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ Prov \_ заменить \_ OWF**    | CSP, поддерживающий замену способа, с помощью которого односторонние форматы создаются из паролей.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ Prov \_ RSA \_ AES**        | CSP, поддерживающий цифровые подписи и шифрование данных с помощью алгоритма AES ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Remarks

Перечисление **\_ \_ типа CAPICOM Prov** используется следующими методами и свойствами:

-   Свойство [**PrivateKey. ProviderType**](privatekey-providertype.md) .
-   Метод [**PrivateKey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Заголовок<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
