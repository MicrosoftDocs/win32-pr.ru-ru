---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD Focus modes \_ описывает режим фокусировки, используемый устройством захвата образа.'
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Перечисление WPD_FOCUS_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668681"
---
# <a name="wpd_focus_modes-enumeration"></a>\_ \_ Перечисление режимов фокусировки WPD

Тип **перечисления \_ WPD \_ Focus** Modes описывает режим фокусировки, используемый устройством захвата образа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**фокус WPD не \_ \_ определен**
</dt> <dd>

Режим фокусировки не указан.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_руководство по возфокусу WPD \_**
</dt> <dd>

Указывает ручной фокус.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_Автоматический фокус в WPD \_**
</dt> <dd>

Задает автоматический фокус, управляемый устройством.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ автоматический макрос ФОКУСа WPD \_**
</dt> <dd>

Указывает, что устройство должно автоматически переключаться между макросом и нормальным фокусом при необходимости.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется в свойстве [ \_ \_ \_ \_ режима фокусировки WPD-изображений](still-image-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




