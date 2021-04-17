---
description: Указывает используемый тип кодировки.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Перечисление CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669188"
---
# <a name="capicom_encoding_type-enumeration"></a>\_Перечисление типов кодировки CAPICOM \_

Тип **перечисления \_ CAPICOM \_ Encoding** указывает используемый тип кодировки.

## <a name="members"></a>Элементы



| Член                      | Описание                                                                                                                                                                                 | Значение      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ кодирует \_ ANY**    | Данные сохраняются в виде строки в кодировке Base64 или в виде чисто двоичной последовательности. Этот тип кодирования используется только для входных данных, имеющих неизвестный тип кодирования. Представлено в CAPICOM 2,0.<br/> | 0xFFFFFFFF |
| **CAPICOM \_ кодирует \_ Base64** | Данные сохраняются в виде строки в кодировке Base64.<br/>                                                                                                                                        | 0          |
| **\_двоичная кодировка CAPICOM \_** | Данные сохраняются в виде чисто двоичной последовательности.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Комментарии

Этот тип перечисления используется следующими методами и свойствами элемента CAPICOM:

-   Метод [**Certificate. Export**](certificate-export.md)
-   [**Енкодеддата. Value,**](encodeddata-value.md) свойство
-   Метод [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)
-   [**Енвелопеддата. Encrypt,**](envelopeddata-encrypt.md) метод
-   [**ExtendedProperty. Value,**](extendedproperty-value.md) свойство
-   [**Сигнеддата. Sign,**](signeddata-sign.md) метод
-   [**Сигнеддата. Кознаковый**](signeddata-cosign.md) метод
-   Метод [**Store. Export**](store-export.md)
-   Метод [**Utilities. Random**](utilities-getrandom.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




