---
title: Получение возможностей форматирования через IWMDMDevice3
description: Получение возможностей форматирования на устройствах, поддерживающих IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Диспетчер устройств Windows Media, возможности устройств
- Диспетчер устройств, возможности устройства
- рекомендации по программированию, возможности устройств
- Классические приложения, возможности устройств
- Создание приложений диспетчер устройств Windows Media, возможности устройств
- запись файлов на устройства, возможности устройств
- Метод IWMDMDevice3
- Диспетчер устройств Windows Media, метод IWMDMDevice3
- Диспетчер устройств, метод IWMDMDevice3
- инструкции по программированию, метод IWMDMDevice3
- Классические приложения, метод IWMDMDevice3
- Создание приложений диспетчер устройств Windows Media, метод IWMDMDevice3
- запись файлов на устройства, метод IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2019
ms.locfileid: "104069418"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="5935b-116">Получение возможностей форматирования через IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="5935b-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="5935b-117">[**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) — это предпочтительный метод для запроса устройства, какие форматы он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="5935b-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="5935b-118">Ниже показано, как использовать этот метод для запроса устройства в отношении его возможностей форматирования:</span><span class="sxs-lookup"><span data-stu-id="5935b-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="5935b-119">Приложение должно определить, какие форматы поддерживает устройство, а какие — интересны.</span><span class="sxs-lookup"><span data-stu-id="5935b-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="5935b-120">Для этого приложение может запросить список форматов, поддерживаемых устройством, вызвав [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span><span class="sxs-lookup"><span data-stu-id="5935b-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="5935b-121">Приложение выполняет цикл по всем поддерживаемым форматам и запрашивает возможности форматирования устройства для определенного формата (например, WMA или WMV) путем вызова **IWMDMDevice3:: жетформаткапабилити** и указания формата с помощью перечисления [**вмдм \_ форматкоде**](wmdm-formatcode.md) .</span><span class="sxs-lookup"><span data-stu-id="5935b-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="5935b-122">Этот метод получает структуру [**\_ \_ возможностей формата вмдм**](wmdm-format-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="5935b-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="5935b-123">Перебрать все [**структуры \_ \_ конфигурации вмдм Prop**](wmdm-prop-config.md) в извлеченной **структуре \_ \_ возможностей формата вмдм** .</span><span class="sxs-lookup"><span data-stu-id="5935b-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="5935b-124">Каждая **Структура \_ \_ конфигурации Prop вмдм** содержит группу свойств с поддерживаемыми значениями, представляющая одну конфигурацию для этого формата.</span><span class="sxs-lookup"><span data-stu-id="5935b-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="5935b-125">Каждая конфигурация имеет номер предпочтения, где меньшее число указывает на большее предпочтение устройству.</span><span class="sxs-lookup"><span data-stu-id="5935b-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="5935b-126">Перебрать все [**структуры \_ вмдм \_ prop**](wmdm-prop-desc.md) в извлеченной **\_ \_ конфигурации Prop вмдм**.</span><span class="sxs-lookup"><span data-stu-id="5935b-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="5935b-127">Каждое **вмдм \_ prop \_ DESC** содержит список поддерживаемых пар "свойство-значение".</span><span class="sxs-lookup"><span data-stu-id="5935b-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="5935b-128">Извлеките имена и значения свойств из структуры **вмдм \_ prop \_** .</span><span class="sxs-lookup"><span data-stu-id="5935b-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="5935b-129">Свойства включают битовую скорость, кодек и размер кадра.</span><span class="sxs-lookup"><span data-stu-id="5935b-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="5935b-130">Имена свойств определяются в файле заголовка мсвмдм. h; список большинства этих констант задается в [константах метаданных](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5935b-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="5935b-131">Возможны три типа значений свойств:</span><span class="sxs-lookup"><span data-stu-id="5935b-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="5935b-132">Единственное значение, ВМДМ \_ enum, \_ \_ Допустимые \_ значения \_ ANY, указывающее на поддержку любых значений для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="5935b-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="5935b-133">Диапазон значений, определяемый максимальным значением, минимальным значением и интервалом.</span><span class="sxs-lookup"><span data-stu-id="5935b-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="5935b-134">Список дискретных значений.</span><span class="sxs-lookup"><span data-stu-id="5935b-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="5935b-135">Очистите сохраненные значения.</span><span class="sxs-lookup"><span data-stu-id="5935b-135">Clear the stored values.</span></span> <span data-ttu-id="5935b-136">Память для этих значений выделяется Windows Media диспетчер устройств; устройство отвечает за освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="5935b-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="5935b-137">Способ их выполнения описан в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="5935b-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="5935b-138">При ответе на **жетформаткапабилити** устройство может сообщать вмдм \_ о \_ \_ допустимых \_ значениях Prop Enum \_ ANY для **\_ возможности форматирования вмдм \_ . \_Конфигурация вмдм Prop \_ . ВМДМ \_ prop \_ , DESC. Валидвалуесформ** , чтобы запрашивать поддержку для любых значений скорости, каналов и т. д.</span><span class="sxs-lookup"><span data-stu-id="5935b-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="5935b-139">Однако это утверждение следует рассматривать с осторожностью, так как устройства иногда могут сообщать о поддержке любых значений, если они не поддерживают все скорости или размеры изображений.</span><span class="sxs-lookup"><span data-stu-id="5935b-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="5935b-140">Вы можете подумать о том, что приложение может перекодировать очень большие или высокоскоростные файлы в меньшие версии или уменьшить объемы ресурсоемких и ресурсоемких версий при их отправке на устройства, предназначенные для воспроизведения этих файлов.</span><span class="sxs-lookup"><span data-stu-id="5935b-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="5935b-141">Следующая функция C++ показывает, как запросить поддержку формата устройства для определенного формата.</span><span class="sxs-lookup"><span data-stu-id="5935b-141">The following C++ function shows how to request device format support for a specific format.</span></span>


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



<span data-ttu-id="5935b-142">**Очистка выделенной памяти**</span><span class="sxs-lookup"><span data-stu-id="5935b-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="5935b-143">После получения возможностей форматирования с устройства приложение должно освободить память, выделенную для хранения описания.</span><span class="sxs-lookup"><span data-stu-id="5935b-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="5935b-144">[**Жетформатсуппорт**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) и [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) имеют массивы простых структур, которые можно очистить, просто вызвав **CoTaskMemFree** с массивом.</span><span class="sxs-lookup"><span data-stu-id="5935b-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="5935b-145">Однако **жетформаткапабилити** имеет более сложную структуру данных с динамически выделяемой памятью, которую необходимо очистить путем цикла по всем элементам и освобождения их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="5935b-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="5935b-146">В следующем коде C++ показано, как приложение может освободить память, выделенную для **структуры \_ \_ возможностей формата вмдм** .</span><span class="sxs-lookup"><span data-stu-id="5935b-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


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



<span data-ttu-id="5935b-147">**Запрос всех поддерживаемых форматов**</span><span class="sxs-lookup"><span data-stu-id="5935b-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="5935b-148">Как правило, приложение запрашивает у устройства конкретный формат, так как он хочет отправить конкретный файл на устройство.</span><span class="sxs-lookup"><span data-stu-id="5935b-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="5935b-149">Однако, если вы хотите запросить приложение для всех поддерживаемых форматов, можно вызвать [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) и передать g \_ всзвмдмформатссуппортед для получения полного списка.</span><span class="sxs-lookup"><span data-stu-id="5935b-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="5935b-150">Если устройство возвращает только один элемент, ВМДМ \_ форматкоде \_ undefine, это обычно означает, что устройство не поддерживает коды форматов.</span><span class="sxs-lookup"><span data-stu-id="5935b-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="5935b-151">Вызов **жетформаткапабилити** с вмдм \_ форматкоде \_ undefine может получить возможности, но эти свойства могут быть довольно универсальными (например, имя, размер файла, Дата последнего изменения и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5935b-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="5935b-152">В следующих шагах показано, как запросить список всех поддерживаемых форматов:</span><span class="sxs-lookup"><span data-stu-id="5935b-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="5935b-153">Запросите список всех кодов форматов, поддерживаемых вызовом **IWMDMDevice3::-Property** и передавая g \_ всзвмдмформатссуппортед.</span><span class="sxs-lookup"><span data-stu-id="5935b-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="5935b-154">Он возвращает **пропвариант** , содержащий **массив SafeArray** поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="5935b-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="5935b-155">Пройдите по элементам, вызвав **сафеаррайжетелемент**.</span><span class="sxs-lookup"><span data-stu-id="5935b-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="5935b-156">Каждый элемент является перечислением **вмдм \_ форматкоде** .</span><span class="sxs-lookup"><span data-stu-id="5935b-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="5935b-157">Запросите возможности для каждого формата, освобождая память для каждого **элемента \_ \_ возможности форматирования вмдм** после завершения работы с ним.</span><span class="sxs-lookup"><span data-stu-id="5935b-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="5935b-158">Очистите **пропвариант** , полученную на шаге 1, вызвав **пропвариантклеар**.</span><span class="sxs-lookup"><span data-stu-id="5935b-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="5935b-159">В следующем примере кода C++ извлекается список поддерживаемых форматов для устройства.</span><span class="sxs-lookup"><span data-stu-id="5935b-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5935b-160">См. также</span><span class="sxs-lookup"><span data-stu-id="5935b-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5935b-161">**Обнаружение возможностей форматирования устройств**</span><span class="sxs-lookup"><span data-stu-id="5935b-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




