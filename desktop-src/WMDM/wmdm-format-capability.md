---
title: Структура WMDM_FORMAT_CAPABILITY
description: '\_ \_ Структура возможностей формата вмдм описывает возможности устройства в определенном формате.'
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- WMDM_FORMAT_CAPABILITY структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694601"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="0559d-104">\_ \_ Структура возможностей формата вмдм</span><span class="sxs-lookup"><span data-stu-id="0559d-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="0559d-105">Структура **\_ \_ возможностей формата вмдм** описывает возможности устройства в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="0559d-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="0559d-106">Эта структура содержит набор конфигураций свойств в массиве структур **конфигурации вмдм \_ prop \_** .</span><span class="sxs-lookup"><span data-stu-id="0559d-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="0559d-107">Каждая конфигурация свойств представляет набор совместимых значений свойств во всех свойствах, поддерживаемых для данного формата.</span><span class="sxs-lookup"><span data-stu-id="0559d-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="0559d-108">Приложение может получить эту структуру, вызвав метод **IWMDMDevice3:: жетформаткапабилити** и передав код формата.</span><span class="sxs-lookup"><span data-stu-id="0559d-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="0559d-109">Список кодов форматов см. в разделе [**вмдм \_ форматкоде**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="0559d-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0559d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0559d-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="0559d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0559d-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="0559d-112">**нпропконфиг**</span><span class="sxs-lookup"><span data-stu-id="0559d-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="0559d-113">Количество конфигураций свойств в массиве **пконфигс** .</span><span class="sxs-lookup"><span data-stu-id="0559d-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="0559d-114">**пконфигс**</span><span class="sxs-lookup"><span data-stu-id="0559d-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="0559d-115">Указатель на массив структур [**конфигурации вмдм \_ prop \_**](wmdm-prop-config.md) .</span><span class="sxs-lookup"><span data-stu-id="0559d-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="0559d-116">Размер массива равен значению параметра **нпропконфиг**.</span><span class="sxs-lookup"><span data-stu-id="0559d-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0559d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0559d-117">Remarks</span></span>

<span data-ttu-id="0559d-118">Структура **\_ \_ возможностей формата вмдм** предоставляет гибкий механизм для выражения возможностей устройства в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="0559d-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="0559d-119">Если содержимое должно быть визуализировано устройством (например, звуковым файлом, который будет воспроизводиться устройством), свойства содержимого должны соответствовать одной из конфигураций свойств, возвращаемых [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) в структуре **\_ \_ возможностей формата вмдм** .</span><span class="sxs-lookup"><span data-stu-id="0559d-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="0559d-120">Например, для звукового файла скорость и частота дискретизации должны соответствовать одной из возвращаемых конфигураций свойств.</span><span class="sxs-lookup"><span data-stu-id="0559d-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="0559d-121">Вызывающий объект отвечает за освобождение памяти, выделенной для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="0559d-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="0559d-122">В следующей функции показано, как очистить структуру **\_ \_ возможностей формата вмдм** .</span><span class="sxs-lookup"><span data-stu-id="0559d-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="0559d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0559d-123">Requirements</span></span>



| <span data-ttu-id="0559d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0559d-124">Requirement</span></span> | <span data-ttu-id="0559d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0559d-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0559d-126">Header</span><span class="sxs-lookup"><span data-stu-id="0559d-126">Header</span></span><br/> | <dl> <span data-ttu-id="0559d-127"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0559d-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0559d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0559d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0559d-129">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="0559d-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="0559d-130">**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**</span><span class="sxs-lookup"><span data-stu-id="0559d-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="0559d-131">**\_Конфигурация вмдм Prop \_**</span><span class="sxs-lookup"><span data-stu-id="0559d-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="0559d-132">**ВМДМ \_ prop, \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0559d-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="0559d-133">**\_ \_ перечисление значений Prop вмдм \_**</span><span class="sxs-lookup"><span data-stu-id="0559d-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="0559d-134">**\_ \_ диапазон значений Prop \_ вмдм**</span><span class="sxs-lookup"><span data-stu-id="0559d-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="0559d-135">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="0559d-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





