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
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649101"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="54411-103">Перечисление Впдаттрибутеформ</span><span class="sxs-lookup"><span data-stu-id="54411-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="54411-104">Тип перечисления **впдаттрибутеформ** описывает, как свойство хранит свои значения.</span><span class="sxs-lookup"><span data-stu-id="54411-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="54411-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54411-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="54411-106">Константы</span><span class="sxs-lookup"><span data-stu-id="54411-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="54411-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**не \_ \_ \_ указана форма атрибута свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="54411-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="54411-108">Форма данных свойства не задана.</span><span class="sxs-lookup"><span data-stu-id="54411-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="54411-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_ \_ \_ диапазон формы атрибута свойства \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="54411-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="54411-110">Значение выражается в диапазоне значений с минимальным и максимальным значением.</span><span class="sxs-lookup"><span data-stu-id="54411-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="54411-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ перечисление формы \_ атрибута свойства WPD**</span><span class="sxs-lookup"><span data-stu-id="54411-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="54411-112">Свойство имеет ряд отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="54411-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="54411-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_форма атрибута свойства WPD — \_ \_ \_ регулярное \_ выражение**</span><span class="sxs-lookup"><span data-stu-id="54411-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="54411-114">Значение свойства является регулярным выражением, а не литеральным выражением.</span><span class="sxs-lookup"><span data-stu-id="54411-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="54411-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_атрибут свойства \_ WPD \_ Форма \_ \_ идентификатора объект**</span><span class="sxs-lookup"><span data-stu-id="54411-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="54411-116">Значение свойства представляет идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="54411-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54411-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54411-117">Remarks</span></span>

<span data-ttu-id="54411-118">Это перечисление используется свойством [ \_ \_ \_ формы атрибута свойства WPD](attributes.md) для описания способа хранения данных свойства.</span><span class="sxs-lookup"><span data-stu-id="54411-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="54411-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54411-119">Requirements</span></span>



| <span data-ttu-id="54411-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54411-120">Requirement</span></span> | <span data-ttu-id="54411-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54411-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="54411-122">Header</span><span class="sxs-lookup"><span data-stu-id="54411-122">Header</span></span><br/> | <dl> <span data-ttu-id="54411-123"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="54411-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54411-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54411-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54411-125">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="54411-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




