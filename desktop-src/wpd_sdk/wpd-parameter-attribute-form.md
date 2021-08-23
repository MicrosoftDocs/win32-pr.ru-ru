---
description: Описывает, как параметр (метод или событие) сохраняет свое значение.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Перечисление Впдпараметераттрибутеформ (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f50665768d62d8155bd0ac9001f4ae5029766d7d5b27a942941f8f41b9492e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026752"
---
# <a name="wpdparameterattributeform-enumeration"></a>Перечисление Впдпараметераттрибутеформ

Тип перечисления [**впдпараметераттрибутеформ**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) описывает, как параметр (метод или событие) сохраняет свое значение.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**не \_ \_ \_ указана форма атрибута параметра WPD \_**
</dt> <dd>

Форма параметра не указана.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_ \_ \_ диапазон формы атрибута параметра \_ WPD**
</dt> <dd>

Параметр задает диапазон.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ перечисление форм \_ атрибута параметра WPD**
</dt> <dd>

Параметр является перечислением.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_форма атрибута параметра WPD. \_ \_ \_ регулярное \_ выражение**
</dt> <dd>

Параметр является регулярным выражением.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_ \_ \_ идентификатор объекта атрибута параметра \_ WPD**
</dt> <dd>

Параметр является идентификатором объекта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



 

