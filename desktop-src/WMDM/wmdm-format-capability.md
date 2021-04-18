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
# <a name="wmdm_format_capability-structure"></a>\_ \_ Структура возможностей формата вмдм

Структура **\_ \_ возможностей формата вмдм** описывает возможности устройства в определенном формате. Эта структура содержит набор конфигураций свойств в массиве структур **конфигурации вмдм \_ prop \_** . Каждая конфигурация свойств представляет набор совместимых значений свойств во всех свойствах, поддерживаемых для данного формата. Приложение может получить эту структуру, вызвав метод **IWMDMDevice3:: жетформаткапабилити** и передав код формата. Список кодов форматов см. в разделе [**вмдм \_ форматкоде**](wmdm-formatcode.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Члены

<dl> <dt>

**нпропконфиг**
</dt> <dd>

Количество конфигураций свойств в массиве **пконфигс** .

</dd> <dt>

**пконфигс**
</dt> <dd>

Указатель на массив структур [**конфигурации вмдм \_ prop \_**](wmdm-prop-config.md) . Размер массива равен значению параметра **нпропконфиг**.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Структура **\_ \_ возможностей формата вмдм** предоставляет гибкий механизм для выражения возможностей устройства в определенном формате.

Если содержимое должно быть визуализировано устройством (например, звуковым файлом, который будет воспроизводиться устройством), свойства содержимого должны соответствовать одной из конфигураций свойств, возвращаемых [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) в структуре **\_ \_ возможностей формата вмдм** . Например, для звукового файла скорость и частота дискретизации должны соответствовать одной из возвращаемых конфигураций свойств.

Вызывающий объект отвечает за освобождение памяти, выделенной для этой структуры. В следующей функции показано, как очистить структуру **\_ \_ возможностей формата вмдм** .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWMDMDevice3:: Жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_Конфигурация вмдм Prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**ВМДМ \_ prop, \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ перечисление значений Prop вмдм \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_ \_ диапазон значений Prop \_ вмдм**](wmdm-prop-values-range.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





