---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ SMS Message Types \_ описывает тип содержимого сообщения SMS.'
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Перечисление SMS_MESSAGE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717862"
---
# <a name="sms_message_types-enumeration"></a>\_ \_ Перечисление типов сообщений SMS

Тип **перечисления \_ SMS \_ Message** Types описывает тип содержимого сообщения SMS.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ Text \_ Message**
</dt> <dd>

Текстовое сообщение.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_двоичное \_ сообщение SMS**
</dt> <dd>

Двоичное сообщение.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется [**командой "WPD" \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




