---
title: Свойства (общие элементы)
description: Платформа текстовых служб (TSF) предоставляет свойства, связывающие метаданные с диапазоном текста.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Платформа текстовых служб (TSF), свойства
- TSF (платформа текстовых служб), свойства
- текстовые службы, свойства
- Приложения, поддерживающие TSF, свойства
- properties
- Платформа текстовых служб (TSF), типы свойств
- TSF (платформа текстовых служб), типы свойств
- текстовые службы, типы свойств
- Приложения с поддержкой TSF, типы свойств
- типы свойств
- Платформа текстовых служб (TSF), постоянное хранение свойств
- TSF (платформа текстовых служб), постоянное хранение свойств
- текстовые службы, постоянное хранение свойств
- Приложения с поддержкой TSF, постоянное хранение свойств
- Постоянное хранение свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105681738"
---
# <a name="properties-common-elements"></a><span data-ttu-id="90dc5-118">Свойства (общие элементы)</span><span class="sxs-lookup"><span data-stu-id="90dc5-118">Properties (Common Elements)</span></span>

<span data-ttu-id="90dc5-119">Платформа текстовых служб (TSF) предоставляет свойства, связывающие метаданные с диапазоном текста.</span><span class="sxs-lookup"><span data-stu-id="90dc5-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="90dc5-120">Эти свойства включают, но не ограничиваются, отображение таких атрибутов, как полужирный текст, идентификатор языка текста и необработанные данные, предоставляемые текстовыми службами, такими как звуковые данные, связанные с текстом из службы речевого текста.</span><span class="sxs-lookup"><span data-stu-id="90dc5-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="90dc5-121">В следующем примере показано, как можно просмотреть свойство гипотетического цвета текста с возможными значениями красного (R), зеленого (G) или синего цветов (B).</span><span class="sxs-lookup"><span data-stu-id="90dc5-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="90dc5-122">Свойства различных типов могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="90dc5-122">Properties of different types can overlap.</span></span> <span data-ttu-id="90dc5-123">Например, возьмем предыдущий пример и добавим текстовый атрибут, который может быть полужирным (B) или курсивом (I).</span><span class="sxs-lookup"><span data-stu-id="90dc5-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="90dc5-124">Текст «this» будет полужирным, а ««» — полужирным и красным, «часть» будет отображаться обычным шрифтом, «цвет» будет зеленым и курсивом, а «текст» будет курсивом.</span><span class="sxs-lookup"><span data-stu-id="90dc5-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="90dc5-125">Свойства одного типа не могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="90dc5-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="90dc5-126">Например, следующая ситуация недопустима, так как "-" и "Цветные" имеют перекрывающиеся значения одних и тех же типов.</span><span class="sxs-lookup"><span data-stu-id="90dc5-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="90dc5-127">Типы свойств</span><span class="sxs-lookup"><span data-stu-id="90dc5-127">Property Types</span></span>

<span data-ttu-id="90dc5-128">TSF определяет три различных типа свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc5-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dc5-129">Статические</span><span class="sxs-lookup"><span data-stu-id="90dc5-129">Static</span></span>         | <span data-ttu-id="90dc5-130">Объект статического свойства хранит данные свойства с текстом.</span><span class="sxs-lookup"><span data-stu-id="90dc5-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="90dc5-131">Он также хранит диапазон текстовых данных для каждого диапазона, к которому применяется свойство.</span><span class="sxs-lookup"><span data-stu-id="90dc5-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="90dc5-132">Итфреадонлипроперти:: GetType возвращает \_ \_ СТАТИЧЕСКУЮ категорию GUID тфкат пропстиле \_ .</span><span class="sxs-lookup"><span data-stu-id="90dc5-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="90dc5-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="90dc5-133">Static-Compact</span></span> | <span data-ttu-id="90dc5-134">Объект свойства со статическим сжатием идентичен объекту статического свойства, за исключением того, что свойство со статическим сжатием не сохраняет данные диапазона.</span><span class="sxs-lookup"><span data-stu-id="90dc5-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="90dc5-135">Когда запрашивается диапазон, охватываемый статическим свойством-Compact, для каждой группы смежных свойств создается диапазон.</span><span class="sxs-lookup"><span data-stu-id="90dc5-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="90dc5-136">Статические свойства — это наиболее эффективный способ хранения свойств для отдельных символов.</span><span class="sxs-lookup"><span data-stu-id="90dc5-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="90dc5-137">Итфреадонлипроперти:: GetType возвращает категорию GUID \_ тфкат \_ пропстиле \_ статиккомпакт.</span><span class="sxs-lookup"><span data-stu-id="90dc5-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="90dc5-138">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="90dc5-138">Custom</span></span>         | <span data-ttu-id="90dc5-139">Объект пользовательского свойства хранит сведения о диапазоне для каждого диапазона, к которому применяется свойство.</span><span class="sxs-lookup"><span data-stu-id="90dc5-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="90dc5-140">Однако он не хранит фактические данные для свойства.</span><span class="sxs-lookup"><span data-stu-id="90dc5-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="90dc5-141">Вместо этого в пользовательском свойстве хранится объект Итфпропертисторе.</span><span class="sxs-lookup"><span data-stu-id="90dc5-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="90dc5-142">Диспетчер TSF использует этот объект для доступа к данным свойств и их обслуживания. Итфреадонлипроперти:: GetType возвращает GUID \_ тфкат \_ пропстиле \_ настраиваемую категорию.</span><span class="sxs-lookup"><span data-stu-id="90dc5-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="90dc5-143">Работа со свойствами</span><span class="sxs-lookup"><span data-stu-id="90dc5-143">Working with Properties</span></span>

<span data-ttu-id="90dc5-144">Значения и атрибуты свойства получаются с помощью интерфейса [итфреадонлипроперти](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) и изменяются с помощью интерфейса [итфпроперти](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .</span><span class="sxs-lookup"><span data-stu-id="90dc5-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="90dc5-145">Если требуется указать конкретный тип свойства, используется [ITfContext::-Property](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="90dc5-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="90dc5-146">Для **ITfContext::-Property** требуется **GUID** , определяющий получаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="90dc5-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="90dc5-147">TSF определяет набор [стандартных идентификаторов свойств](predefined-properties.md) , которые используются, или служба текстового ввода может определять собственные идентификаторы свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc5-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="90dc5-148">Если используется пользовательское свойство, поставщик свойств должен опубликовать **идентификатор GUID** свойства и формат полученных данных.</span><span class="sxs-lookup"><span data-stu-id="90dc5-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="90dc5-149">Например, чтобы получить **идентификатор CLSID** для владельца диапазона текста, вызовите метод **ITfContext::** GetObject, чтобы получить объект свойства, вызовите [итфпроперти:: финдранже](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) , чтобы получить диапазон, который полностью охватывает свойство, а затем вызовите метод [Итфреадонлипроперти:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) , чтобы получить [тфгуидатом](/windows/desktop/TSF/tfguidatom) , который представляет **идентификатор CLSID** службы текстового ввода, владеющей текстом.</span><span class="sxs-lookup"><span data-stu-id="90dc5-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="90dc5-150">В следующем примере показана функция, которая задается контекстом, Range и Edit cookie, получит **идентификатор CLSID** службы текстового ввода, владеющей текстом.</span><span class="sxs-lookup"><span data-stu-id="90dc5-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="90dc5-151">Свойства также можно перечислить, получая интерфейс [иенумтфпропертиес](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) из [ITfContext:: енумпропертиес](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="90dc5-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="90dc5-152">Постоянное хранение свойств</span><span class="sxs-lookup"><span data-stu-id="90dc5-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="90dc5-153">Часто свойства являются прозрачными для приложения и используются одной или несколькими текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="90dc5-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="90dc5-154">Чтобы сохранить данные свойств, например, при сохранении в файл, приложение должно сериализовать данные свойства при сохранении и десериализации данных свойства при восстановлении данных.</span><span class="sxs-lookup"><span data-stu-id="90dc5-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="90dc5-155">В этом случае приложению не следует заинтересовать отдельные свойства, но следует перечислить все свойства в контексте и сохранить их.</span><span class="sxs-lookup"><span data-stu-id="90dc5-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="90dc5-156">При хранении данных свойств приложение должно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90dc5-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="90dc5-157">Получите перечислитель свойств путем вызова **ITfContext:: енумпропертиес**.</span><span class="sxs-lookup"><span data-stu-id="90dc5-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="90dc5-158">Перечислите каждое свойство, вызвав метод [иенумтфпропертиес:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span><span class="sxs-lookup"><span data-stu-id="90dc5-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="90dc5-159">Для каждого свойства получите перечислитель диапазона, вызвав [итфреадонлипроперти:: енумранжес](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="90dc5-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="90dc5-160">Перечислите каждый диапазон в свойстве, вызвав метод [иенумтфранжес:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span><span class="sxs-lookup"><span data-stu-id="90dc5-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="90dc5-161">Для каждого диапазона в свойстве вызовите [итекстстореакпсервицес:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) со свойством, Range, структурой [ \_ \_ \_ \_ ACP постоянного свойства "TF PERSISTENT](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) " и объектом потока, реализованным приложением.</span><span class="sxs-lookup"><span data-stu-id="90dc5-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="90dc5-162">Запишите содержимое структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF persistent** " в постоянную память.</span><span class="sxs-lookup"><span data-stu-id="90dc5-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="90dc5-163">Запись содержимого объекта потока в постоянную память.</span><span class="sxs-lookup"><span data-stu-id="90dc5-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="90dc5-164">Продолжайте предыдущие шаги для всех диапазонов во всех свойствах.</span><span class="sxs-lookup"><span data-stu-id="90dc5-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="90dc5-165">Приложение должно записывать некоторый тип терминиатор в поток, чтобы при восстановлении данных можно было идентифицировать точку останова.</span><span class="sxs-lookup"><span data-stu-id="90dc5-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="90dc5-166">**Итекстстореакпсервицес:: сериализует**[Итфпропертисторе:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="90dc5-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="90dc5-167">При восстановлении данных свойств приложение должно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90dc5-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="90dc5-168">Установите указатель потока на начало первой структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF PERSISTENT** ".</span><span class="sxs-lookup"><span data-stu-id="90dc5-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="90dc5-169">Чтение структуры **\_ постоянного \_ \_ заголовка \_ Свойства "TF PERSISTENT** ".</span><span class="sxs-lookup"><span data-stu-id="90dc5-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="90dc5-170">Вызовите **ITfContext:: Property** с элементом **гуидтипе** структуры **\_ \_ \_ \_ ACP постоянного свойства "TF PERSISTENT** ".</span><span class="sxs-lookup"><span data-stu-id="90dc5-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="90dc5-171">На этом этапе приложение может выполнить одно из двух действий.</span><span class="sxs-lookup"><span data-stu-id="90dc5-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="90dc5-172">Создайте экземпляр объекта [итфперсистентпропертилоадеракп](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) , который должен быть реализован приложением.</span><span class="sxs-lookup"><span data-stu-id="90dc5-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="90dc5-173">Затем вызовите [итекстстореакпсервицес:: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) со **значением NULL** для *пстреам* и указателем **итфперсистентпропертилоадеракп** .</span><span class="sxs-lookup"><span data-stu-id="90dc5-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="90dc5-174">Передайте входной поток в **итекстстореакпсервицес:: unserialize** и **null** для *плоадер*.</span><span class="sxs-lookup"><span data-stu-id="90dc5-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="90dc5-175">Первый метод является предпочтительным, так как он наиболее эффективен.</span><span class="sxs-lookup"><span data-stu-id="90dc5-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="90dc5-176">Реализация второго метода приводит к считыванию всех данных свойств из потока во время вызова **итекстстореакпсервицес:: unserialize** .</span><span class="sxs-lookup"><span data-stu-id="90dc5-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="90dc5-177">Первый метод приводит к тому, что данные свойств будут считываться по запросу в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="90dc5-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="90dc5-178">Повторите предыдущие шаги, пока не будут десериализованы все блоки свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc5-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
