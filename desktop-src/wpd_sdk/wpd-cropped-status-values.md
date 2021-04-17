---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD "кадрированные \_ значения состояния" \_ описывает состояние кадрирования изображения.'
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Перечисление WPD_CROPPED_STATUS_VALUES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674839"
---
# <a name="wpd_cropped_status_values-enumeration"></a>\_ \_ Перечисление значений состояния КАДРИРОВАНия WPD \_

Тип перечисления **WPD " \_ кадрированные \_ \_ значения состояния** " описывает состояние кадрирования изображения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_состояние кадрирования \_ WPD \_ не \_ обрезано**
</dt> <dd>

Изображение не обрезано.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**обрезанное \_ \_ состояние WPD \_**
</dt> <dd>

Изображение обрезано.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_состояние кадрирования \_ WPD \_ \_ не следует \_ \_ обрезать**
</dt> <dd>

Изображение не было, и его не следует обрезать.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обозначает обрезанное состояние изображения. Это перечисление используется свойством " [ \_ \_ \_ состояние кадрирования изображения WPD](image-properties.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




