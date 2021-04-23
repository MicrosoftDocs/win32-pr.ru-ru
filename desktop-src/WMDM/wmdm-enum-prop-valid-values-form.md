---
title: Перечисление WMDM_ENUM_PROP_VALID_VALUES_FORM
description: '\_ \_ Допустимые значения параметра prop enum вмдм \_ \_ \_ . тип перечисления содержит описание возможных форм допустимых значений для свойства.'
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694524"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="f5ff8-104">\_ \_ \_ Перечисление допустимых \_ значений свойства Prop enum вмдм \_</span><span class="sxs-lookup"><span data-stu-id="f5ff8-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="f5ff8-105">**\_ \_ \_ Допустимые \_ значения \_ параметра prop enum вмдм** . тип перечисления содержит описание возможных форм допустимых значений для свойства.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ff8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5ff8-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="f5ff8-107">Константы</span><span class="sxs-lookup"><span data-stu-id="f5ff8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5ff8-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**ВМДМ \_ Enum \_ prop \_ Допустимые \_ значения \_ ANY**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff8-109">Все значения допустимы.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="f5ff8-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_ \_ \_ диапазон допустимых \_ значений Prop Enum \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff8-111">Допустимые значения выражаются в виде диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="f5ff8-112">Подробные сведения см. в разделе [**Структура \_ \_ \_ диапазона значений свойств вмдм**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ff8-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f5ff8-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_ \_ \_ перечисление допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff8-114">Допустимые значения — перечислимый набор.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="f5ff8-115">Подробные сведения см. в описании [**\_ \_ \_ перечисления вмдм Prop Values**](wmdm-prop-values-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ff8-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5ff8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5ff8-116">Remarks</span></span>

<span data-ttu-id="f5ff8-117">Это перечисление используется в [**структуре \_ вмдм \_ prop**](wmdm-prop-desc.md) , чтобы указать форму допустимых значений для свойства.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ff8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f5ff8-118">Requirements</span></span>



| <span data-ttu-id="f5ff8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f5ff8-119">Requirement</span></span> | <span data-ttu-id="f5ff8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f5ff8-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ff8-121">Header</span><span class="sxs-lookup"><span data-stu-id="f5ff8-121">Header</span></span><br/> | <dl> <span data-ttu-id="f5ff8-122"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5ff8-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ff8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5ff8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ff8-124">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="f5ff8-125">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="f5ff8-126">**\_возможность форматирования \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="f5ff8-127">**\_Конфигурация вмдм Prop \_**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="f5ff8-128">**ВМДМ \_ prop, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="f5ff8-129">**\_ \_ перечисление значений Prop вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="f5ff8-130">**\_ \_ диапазон значений Prop \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="f5ff8-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





