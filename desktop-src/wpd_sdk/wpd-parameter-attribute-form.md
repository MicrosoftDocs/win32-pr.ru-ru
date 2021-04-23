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
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648037"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="576d6-103">Перечисление Впдпараметераттрибутеформ</span><span class="sxs-lookup"><span data-stu-id="576d6-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="576d6-104">Тип перечисления [**впдпараметераттрибутеформ**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) описывает, как параметр (метод или событие) сохраняет свое значение.</span><span class="sxs-lookup"><span data-stu-id="576d6-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="576d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="576d6-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="576d6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="576d6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="576d6-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**не \_ \_ \_ указана форма атрибута параметра WPD \_**</span><span class="sxs-lookup"><span data-stu-id="576d6-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="576d6-108">Форма параметра не указана.</span><span class="sxs-lookup"><span data-stu-id="576d6-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="576d6-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_ \_ \_ диапазон формы атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="576d6-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="576d6-110">Параметр задает диапазон.</span><span class="sxs-lookup"><span data-stu-id="576d6-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="576d6-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ перечисление форм \_ атрибута параметра WPD**</span><span class="sxs-lookup"><span data-stu-id="576d6-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="576d6-112">Параметр является перечислением.</span><span class="sxs-lookup"><span data-stu-id="576d6-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="576d6-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_форма атрибута параметра WPD. \_ \_ \_ регулярное \_ выражение**</span><span class="sxs-lookup"><span data-stu-id="576d6-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="576d6-114">Параметр является регулярным выражением.</span><span class="sxs-lookup"><span data-stu-id="576d6-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="576d6-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_ \_ \_ идентификатор объекта атрибута параметра \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="576d6-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="576d6-116">Параметр является идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="576d6-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="576d6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="576d6-117">Requirements</span></span>



| <span data-ttu-id="576d6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="576d6-118">Requirement</span></span> | <span data-ttu-id="576d6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="576d6-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="576d6-120">Header</span><span class="sxs-lookup"><span data-stu-id="576d6-120">Header</span></span><br/> | <dl> <span data-ttu-id="576d6-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="576d6-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

