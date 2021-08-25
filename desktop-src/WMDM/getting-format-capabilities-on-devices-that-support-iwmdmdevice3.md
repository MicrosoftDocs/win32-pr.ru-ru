---
title: Получение возможностей форматирования через IWMDMDevice3
description: Получение возможностей форматирования на устройствах, поддерживающих IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Диспетчер устройств мультимедиа, возможности устройства
- Диспетчер устройств, возможности устройства
- рекомендации по программированию, возможности устройств
- Классические приложения, возможности устройств
- создание Windows мультимедиа диспетчер устройств приложений, возможности устройств
- запись файлов на устройства, возможности устройств
- Метод IWMDMDevice3
- Windows Диспетчер устройств мультимедиа, метод IWMDMDevice3
- Диспетчер устройств, метод IWMDMDevice3
- инструкции по программированию, метод IWMDMDevice3
- Классические приложения, метод IWMDMDevice3
- создание Windows мультимедиа диспетчер устройств приложений, метод IWMDMDevice3
- запись файлов на устройства, метод IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eadde80f957573563468375ea06cd64b95cf83815491a3f21775fb1ebcefc7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957533"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Получение возможностей форматирования через IWMDMDevice3

[**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) — это предпочтительный метод для запроса устройства, какие форматы он поддерживает. Ниже показано, как использовать этот метод для запроса устройства в отношении его возможностей форматирования:

1.  Приложение должно определить, какие форматы поддерживает устройство, а какие — интересны. Для этого приложение может запросить список форматов, поддерживаемых устройством, вызвав [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  Приложение выполняет цикл по всем поддерживаемым форматам и запрашивает возможности форматирования устройства для определенного формата (например, WMA или WMV) путем вызова **IWMDMDevice3:: жетформаткапабилити** и указания формата с помощью перечисления [**вмдм \_ форматкоде**](wmdm-formatcode.md) . Этот метод получает структуру [**\_ \_ возможностей формата вмдм**](wmdm-format-capability.md) .
3.  Перебрать все [**структуры \_ \_ конфигурации вмдм Prop**](wmdm-prop-config.md) в извлеченной **структуре \_ \_ возможностей формата вмдм** . Каждая **Структура \_ \_ конфигурации Prop вмдм** содержит группу свойств с поддерживаемыми значениями, представляющая одну конфигурацию для этого формата. Каждая конфигурация имеет номер предпочтения, где меньшее число указывает на большее предпочтение устройству.
4.  Перебрать все [**структуры \_ вмдм \_ prop**](wmdm-prop-desc.md) в извлеченной **\_ \_ конфигурации Prop вмдм**. Каждое **вмдм \_ prop \_ DESC** содержит список поддерживаемых пар "свойство-значение".
5.  Извлеките имена и значения свойств из структуры **вмдм \_ prop \_** . Свойства включают битовую скорость, кодек и размер кадра. Имена свойств определяются в файле заголовка мсвмдм. h; список большинства этих констант задается в [константах метаданных](metadata-constants.md). Возможны три типа значений свойств:
    -   Единственное значение, ВМДМ \_ enum, \_ \_ Допустимые \_ значения \_ ANY, указывающее на поддержку любых значений для этого свойства.
    -   Диапазон значений, определяемый максимальным значением, минимальным значением и интервалом.
    -   Список дискретных значений.
6.  Очистите сохраненные значения. память для этих значений выделяется Windows Media диспетчер устройств; устройство отвечает за освобождение памяти. Способ их выполнения описан в конце этого раздела.

При ответе на **жетформаткапабилити** устройство может сообщать вмдм \_ о \_ \_ допустимых \_ значениях Prop Enum \_ ANY для **\_ возможности форматирования вмдм \_ . \_Конфигурация вмдм Prop \_ . ВМДМ \_ prop \_ , DESC. Валидвалуесформ** , чтобы запрашивать поддержку для любых значений скорости, каналов и т. д. Однако это утверждение следует рассматривать с осторожностью, так как устройства иногда могут сообщать о поддержке любых значений, если они не поддерживают все скорости или размеры изображений. Вы можете подумать о том, что приложение может перекодировать очень большие или высокоскоростные файлы в меньшие версии или уменьшить объемы ресурсоемких и ресурсоемких версий при их отправке на устройства, предназначенные для воспроизведения этих файлов.

Следующая функция C++ показывает, как запросить поддержку формата устройства для определенного формата.


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



**Очистка выделенной памяти**

После получения возможностей форматирования с устройства приложение должно освободить память, выделенную для хранения описания. [**Жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) и [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) имеют массивы простых структур, которые можно очистить, просто вызвав **CoTaskMemFree** с массивом. Однако **жетформаткапабилити** имеет более сложную структуру данных с динамически выделяемой памятью, которую необходимо очистить путем цикла по всем элементам и освобождения их по отдельности.

В следующем коде C++ показано, как приложение может освободить память, выделенную для **структуры \_ \_ возможностей формата вмдм** .


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
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



**Запрос всех поддерживаемых форматов**

Как правило, приложение запрашивает у устройства конкретный формат, так как он хочет отправить конкретный файл на устройство. Однако, если вы хотите запросить приложение для всех поддерживаемых форматов, можно вызвать [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) и передать g \_ всзвмдмформатссуппортед для получения полного списка.

Если устройство возвращает только один элемент, ВМДМ \_ форматкоде \_ undefine, это обычно означает, что устройство не поддерживает коды форматов. Вызов **жетформаткапабилити** с вмдм \_ форматкоде \_ undefine может получить возможности, но эти свойства могут быть довольно универсальными (например, имя, размер файла, Дата последнего изменения и т. д.).

В следующих шагах показано, как запросить список всех поддерживаемых форматов:

1.  Запросите список всех кодов форматов, поддерживаемых вызовом **IWMDMDevice3::-Property** и передавая g \_ всзвмдмформатссуппортед. Он возвращает **пропвариант** , содержащий **массив SafeArray** поддерживаемых форматов.
2.  Пройдите по элементам, вызвав **сафеаррайжетелемент**. Каждый элемент является перечислением **вмдм \_ форматкоде** .
3.  Запросите возможности для каждого формата, освобождая память для каждого **элемента \_ \_ возможности форматирования вмдм** после завершения работы с ним.
4.  Очистите **пропвариант** , полученную на шаге 1, вызвав **пропвариантклеар**.

В следующем примере кода C++ извлекается список поддерживаемых форматов для устройства.


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Обнаружение возможностей форматирования устройств**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




