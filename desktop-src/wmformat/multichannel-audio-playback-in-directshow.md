---
title: Многоканальное воспроизведение звука в DirectShow
description: Многоканальное воспроизведение звука в DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, многоканальное воспроизведение звука
- Windows Media Format SDK, воспроизведение звука
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), многоканальное воспроизведение звука
- ASF (Расширенный системный формат), многоканальное воспроизведение звука
- Расширенный формат систем (ASF), воспроизведение звука
- ASF (расширенный формат систем), воспроизведение звука
- DirectShow, многоканальное воспроизведение звука
- DirectShow, воспроизведение звука
- многоканальное аудио, воспроизведение
- воспроизведение звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412587"
---
# <a name="multichannel-audio-playback-in-directshow"></a><span data-ttu-id="9180c-116">Многоканальное воспроизведение звука в DirectShow</span><span class="sxs-lookup"><span data-stu-id="9180c-116">Multichannel Audio Playback in DirectShow</span></span>

<span data-ttu-id="9180c-117">Чтобы воспроизвести многоканальный звуковой файл Windows Media в DirectShow, необходимо задать \_ свойство "хиресаутпут" непосредственно в декодере после его подключения к модулю чтения WM ASF.</span><span class="sxs-lookup"><span data-stu-id="9180c-117">To play back a multichannel Windows Media Audio file in DirectShow, you must set the "\_HIRESOUTPUT" property directly on the decoder after it has been connected to the WM ASF Reader.</span></span> <span data-ttu-id="9180c-118">Настройка объекта модуля чтения не требуется.</span><span class="sxs-lookup"><span data-stu-id="9180c-118">No configuration of the Reader Object is necessary.</span></span> <span data-ttu-id="9180c-119">Однако для непосредственной работы с DMO требуется вмкодекконст. h из [примера кода для использования интерфейса кодеков аудио и видео Windows Media для](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) скачивания пакета.</span><span class="sxs-lookup"><span data-stu-id="9180c-119">However, to work with the DMO directly, you need wmcodecconst.h from the [Sample Code for Using the Windows Media Audio and Video Codec Interfaces](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) download package.</span></span>

<span data-ttu-id="9180c-120">**Примечание** . Эта процедура конфигурации поддерживается только для файлов, не защищенных с помощью цифровых Rights Management.</span><span class="sxs-lookup"><span data-stu-id="9180c-120">**Note** This configuration procedure is supported only for files that are not protected by Digital Rights Management.</span></span>

<span data-ttu-id="9180c-121">Ниже приведены основные действия по включению многоканального вывода.</span><span class="sxs-lookup"><span data-stu-id="9180c-121">The basic steps to enable multichannel output are as follows:</span></span>

1.  <span data-ttu-id="9180c-122">Вызовите функцию RenderFile, чтобы создать граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="9180c-122">Call RenderFile to create the filter graph.</span></span>
2.  <span data-ttu-id="9180c-123">Получение указателя на фильтр оболочки DMO</span><span class="sxs-lookup"><span data-stu-id="9180c-123">Obtain a pointer to the DMO Wrapper filter</span></span>
3.  <span data-ttu-id="9180c-124">Отключение оболочки DMO от модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="9180c-124">Disconnect the DMO Wrapper from the Audio Renderer</span></span>
4.  <span data-ttu-id="9180c-125">Задайте свойство " \_ хиресаутпут" для декодера.</span><span class="sxs-lookup"><span data-stu-id="9180c-125">Set the "\_HIRESOUTPUT" property on the decoder.</span></span>
5.  <span data-ttu-id="9180c-126">Повторно подключите оболочку DMO и модуль подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="9180c-126">Reconnect the DMO Wrapper and the Audio Renderer.</span></span>
6.  <span data-ttu-id="9180c-127">Запустите граф.</span><span class="sxs-lookup"><span data-stu-id="9180c-127">Run the graph.</span></span>

<span data-ttu-id="9180c-128">Эти шаги демонстрируются в следующих фрагментах кода.</span><span class="sxs-lookup"><span data-stu-id="9180c-128">The following code snippets demonstrate these steps.</span></span> <span data-ttu-id="9180c-129">(Для простоты пропущена вся проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="9180c-129">(All error checking has been omitted for the sake of simplicity.</span></span> <span data-ttu-id="9180c-130">При использовании этого кода в приложении следует добавить соответствующие подпрограммы обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="9180c-130">You should add proper error handling routines if you use this code in an application.)</span></span>


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



<span data-ttu-id="9180c-131">Функции Жетдмовраппер и Жетпин из предыдущего фрагмента кода реализуются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9180c-131">The GetDMOWrapper and GetPin functions from the previous code snippet are implemented as follows:</span></span>


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




