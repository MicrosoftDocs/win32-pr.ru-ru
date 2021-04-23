---
title: Структура WMDM_PROP_CONFIG
description: '\_ \_ Структура конфигурации вмдм Prop описывает набор совместимых значений свойств во всех свойствах, поддерживаемых устройством в определенном формате. Эта структура содержит ряд описаний свойств в массиве \_ структур вмдм Prop \_ DESC.'
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694437"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="30cdb-105">\_ \_ Структура конфигурации вмдм Prop</span><span class="sxs-lookup"><span data-stu-id="30cdb-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="30cdb-106">Структура **\_ \_ конфигурации вмдм Prop** описывает набор совместимых значений свойств во всех свойствах, поддерживаемых устройством в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="30cdb-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="30cdb-107">Эта структура содержит ряд описаний свойств в массиве структур [**вмдм \_ prop \_ DESC**](wmdm-prop-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="30cdb-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cdb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30cdb-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="30cdb-109">Члены</span><span class="sxs-lookup"><span data-stu-id="30cdb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="30cdb-110">**нпреференце**</span><span class="sxs-lookup"><span data-stu-id="30cdb-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="30cdb-111">Уровень предпочтения устройства для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30cdb-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="30cdb-112">Наименьшее значение указывает наиболее предпочтительную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="30cdb-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="30cdb-113">**нпропдеск**</span><span class="sxs-lookup"><span data-stu-id="30cdb-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="30cdb-114">Количество описаний свойств, содержащихся в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30cdb-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="30cdb-115">Для каждого свойства, поддерживаемого для указанного формата, существует одно описание свойства.</span><span class="sxs-lookup"><span data-stu-id="30cdb-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="30cdb-116">**ппропдеск**</span><span class="sxs-lookup"><span data-stu-id="30cdb-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="30cdb-117">Указатель на массив [**вмдм \_ prop \_**](wmdm-prop-desc.md) структуры, содержащий описания свойств.</span><span class="sxs-lookup"><span data-stu-id="30cdb-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="30cdb-118">Размер массива равен значению параметра **нпропдеск**.</span><span class="sxs-lookup"><span data-stu-id="30cdb-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="30cdb-119">Приложение должно освободить эту память по завершении работы с ней.</span><span class="sxs-lookup"><span data-stu-id="30cdb-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30cdb-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30cdb-120">Remarks</span></span>

<span data-ttu-id="30cdb-121">Структура [**\_ \_ возможностей формата вмдм**](wmdm-format-capability.md) , возвращаемая [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) для конкретного формата, состоит из нескольких конфигураций свойств.</span><span class="sxs-lookup"><span data-stu-id="30cdb-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="30cdb-122">**Вмдм \_ Структуры \_ конфигурации Prop** описывают эти конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30cdb-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="30cdb-123">Конфигурация свойств описывает значения всех свойств, поддерживаемых для данного формата.</span><span class="sxs-lookup"><span data-stu-id="30cdb-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="30cdb-124">Значения различных свойств в одной конфигурации совместимы друг с другом.</span><span class="sxs-lookup"><span data-stu-id="30cdb-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="30cdb-125">Например, для звукового файла конфигурация будет включать допустимые значения частоты выборки и допустимые значения скорости, что позволяет воспроизводить на устройстве все сочетания этих образцов и ставок.</span><span class="sxs-lookup"><span data-stu-id="30cdb-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="30cdb-126">Вызывающий объект необходим для высвобождения памяти, используемой **ппропдеск**.</span><span class="sxs-lookup"><span data-stu-id="30cdb-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="30cdb-127">Пример того, как это сделать, см. в [**разделе \_ \_ функция форматирования вмдм**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="30cdb-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30cdb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="30cdb-128">Requirements</span></span>



| <span data-ttu-id="30cdb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="30cdb-129">Requirement</span></span> | <span data-ttu-id="30cdb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="30cdb-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="30cdb-131">Header</span><span class="sxs-lookup"><span data-stu-id="30cdb-131">Header</span></span><br/> | <dl> <span data-ttu-id="30cdb-132"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30cdb-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30cdb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30cdb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cdb-134">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="30cdb-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="30cdb-135">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="30cdb-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="30cdb-136">**\_возможность форматирования \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="30cdb-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="30cdb-137">**ВМДМ \_ prop, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="30cdb-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="30cdb-138">**\_ \_ перечисление значений Prop вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="30cdb-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="30cdb-139">**\_ \_ диапазон значений Prop \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="30cdb-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="30cdb-140">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="30cdb-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





