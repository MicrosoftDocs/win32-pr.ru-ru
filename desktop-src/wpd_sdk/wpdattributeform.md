---
description: Тип перечисления Впдаттрибутеформ описывает, как свойство хранит свои значения.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Перечисление Впдаттрибутеформ (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8366f90fe41eaa92d826f4d761fe8cdf58304f54e1f57cb074ae94d6fd9f1ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696282"
---
# <a name="wpdattributeform-enumeration"></a>Перечисление Впдаттрибутеформ

Тип перечисления **впдаттрибутеформ** описывает, как свойство хранит свои значения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**не \_ \_ \_ указана форма атрибута свойства WPD \_**
</dt> <dd>

Форма данных свойства не задана.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_ \_ \_ диапазон формы атрибута свойства \_ WPD**
</dt> <dd>

Значение выражается в диапазоне значений с минимальным и максимальным значением.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ перечисление формы \_ атрибута свойства WPD**
</dt> <dd>

Свойство имеет ряд отдельных значений.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_форма атрибута свойства WPD — \_ \_ \_ регулярное \_ выражение**
</dt> <dd>

Значение свойства является регулярным выражением, а не литеральным выражением.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_атрибут свойства \_ WPD \_ Форма \_ \_ идентификатора объект**
</dt> <dd>

Значение свойства представляет идентификатор объекта.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление используется свойством [ \_ \_ \_ формы атрибута свойства WPD](attributes.md) для описания способа хранения данных свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




