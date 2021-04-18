---
description: Тип перечисления "WPD SMS Encoding Types" \_ \_ \_ описывает тип кодировки сообщения SMS.
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Перечисление WPD_SMS_ENCODING_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648986"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>\_ \_ \_ Перечисление типов кодирования SMS типа WPD

Тип перечисления " **WPD \_ SMS \_ Encoding \_** Types" описывает тип кодировки сообщения SMS.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Кодировка SMS \_ 7 \_ bit**
</dt> <dd>

7-разрядная кодировка.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**\_ \_ 8 бит кодирования \_ SMS**
</dt> <dd>

8-разрядная кодировка.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Кодирование SMS \_ UTF \_ 16**
</dt> <dd>

16-битная кодировка (UTF).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется свойством [ \_ \_ кодирования WPD в SMS](sms-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




