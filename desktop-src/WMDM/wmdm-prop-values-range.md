---
title: Структура WMDM_PROP_VALUES_RANGE
description: '\_ \_ Структура диапазона значений Prop вмдм \_ описывает диапазон допустимых значений для конкретного свойства в определенной конфигурации свойства.'
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694643"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="d0d31-104">\_ \_ Структура диапазона значений Prop вмдм \_</span><span class="sxs-lookup"><span data-stu-id="d0d31-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="d0d31-105">Структура **\_ \_ \_ диапазона значений Prop вмдм** описывает диапазон допустимых значений для конкретного свойства в определенной конфигурации свойства.</span><span class="sxs-lookup"><span data-stu-id="d0d31-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0d31-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="d0d31-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d0d31-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0d31-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="d0d31-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="d0d31-109">Минимальное значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="d0d31-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="d0d31-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="d0d31-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="d0d31-111">Максимальное значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="d0d31-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="d0d31-112">**ранжестеп**</span><span class="sxs-lookup"><span data-stu-id="d0d31-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="d0d31-113">Размер шага, в котором допустимы значения, увеличивающиеся из минимального значения до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d0d31-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="d0d31-114">Это позволяет указать дискретные допустимые значения в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="d0d31-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0d31-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0d31-115">Remarks</span></span>

<span data-ttu-id="d0d31-116">Эта структура используется в структуре [**вмдм \_ prop \_**](wmdm-prop-desc.md) , чтобы описать диапазон допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="d0d31-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="d0d31-117">Диапазон допустимых значений применим, если выбрано перечисление \_ \_ \_ допустимых значений Prop enum вмдм \_ \_ из перечисления [**\_ \_ \_ допустимых \_ значений \_ Свойства вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d31-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d31-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d0d31-118">Requirements</span></span>



| <span data-ttu-id="d0d31-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d0d31-119">Requirement</span></span> | <span data-ttu-id="d0d31-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d0d31-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d31-121">Header</span><span class="sxs-lookup"><span data-stu-id="d0d31-121">Header</span></span><br/> | <dl> <span data-ttu-id="d0d31-122"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0d31-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0d31-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0d31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d31-124">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="d0d31-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="d0d31-125">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="d0d31-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="d0d31-126">**\_возможность форматирования \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="d0d31-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="d0d31-127">**\_Конфигурация вмдм Prop \_**</span><span class="sxs-lookup"><span data-stu-id="d0d31-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="d0d31-128">**ВМДМ \_ prop, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="d0d31-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="d0d31-129">**\_ \_ перечисление значений Prop вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="d0d31-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="d0d31-130">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="d0d31-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





