---
description: Определяет алгоритмы, используемые при шифровании и расшифровке.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Перечисление CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668526"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>\_ \_ Перечисление АЛГОРИТМа CAPICOM

Тип перечисления для **\_ \_ алгоритма CAPICOM** определяет алгоритмы, используемые при шифровании и расшифровке.

## <a name="members"></a>Элементы



| Член                                   | Описание                                                                                                                                                                                              | Значение     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **\_Алгоритм шифрования \_ CAPICOM \_ RC2**  | Используйте шифрование RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **\_Алгоритм шифрования \_ CAPICOM \_ RC4**  | Используйте шифрование RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **\_алгоритм шифрования \_ CAPICOM \_ des**  | Используйте шифрование DES.<br/>                                                                                                                                                                           | 2         |
| **\_Алгоритм шифрования \_ CAPICOM \_ 3DES** | Используйте тройное шифрование DES.<br/>                                                                                                                                                                    | 3         |
| **\_алгоритм шифрования \_ CAPICOM \_ AES**  | Используйте алгоритм [*AES*](../secgloss/a-gly.md) (AES). Это значение допустимо только для объекта [**EncryptedData**](encrypteddata.md) .<br/> | 4//v 2.0 |



## <a name="remarks"></a>Комментарии

Тип перечисления для **\_ \_ алгоритма CAPICOM-шифрования** используется свойством [**Algorithm.Name**](algorithm-name.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
