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
# <a name="multichannel-audio-playback-in-directshow"></a>Многоканальное воспроизведение звука в DirectShow

Чтобы воспроизвести многоканальный звуковой файл Windows Media в DirectShow, необходимо задать \_ свойство "хиресаутпут" непосредственно в декодере после его подключения к модулю чтения WM ASF. Настройка объекта модуля чтения не требуется. Однако для непосредственной работы с DMO требуется вмкодекконст. h из [примера кода для использования интерфейса кодеков аудио и видео Windows Media для](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) скачивания пакета.

**Примечание** . Эта процедура конфигурации поддерживается только для файлов, не защищенных с помощью цифровых Rights Management.

Ниже приведены основные действия по включению многоканального вывода.

1.  Вызовите функцию RenderFile, чтобы создать граф фильтра.
2.  Получение указателя на фильтр оболочки DMO
3.  Отключение оболочки DMO от модуля подготовки звука
4.  Задайте свойство " \_ хиресаутпут" для декодера.
5.  Повторно подключите оболочку DMO и модуль подготовки звука.
6.  Запустите граф.

Эти шаги демонстрируются в следующих фрагментах кода. (Для простоты пропущена вся проверка ошибок. При использовании этого кода в приложении следует добавить соответствующие подпрограммы обработки ошибок.


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



Функции Жетдмовраппер и Жетпин из предыдущего фрагмента кода реализуются следующим образом:


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



 

 




