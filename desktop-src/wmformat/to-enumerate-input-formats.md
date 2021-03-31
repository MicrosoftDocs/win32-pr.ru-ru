---
title: Перечисление входных форматов
description: Перечисление входных форматов
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Расширенный системный формат (ASF), перечисление входных форматов
- ASF (Расширенный системный формат), перечисление входных форматов
- профили, перечисление входных форматов
- кодеки, перечисление входных форматов
- Расширенные системные форматы (ASF), перечисления входного формата
- ASF (Расширенный системный формат), перечисления входного формата
- профили, перечисления входных форматов
- кодеки, перечисления входного формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069699"
---
# <a name="to-enumerate-input-formats"></a>Перечисление входных форматов

Каждый кодек Windows Media поддерживает один или несколько типов входных носителей для сжатия. Пакет SDK для формата Windows Media позволяет вводить более широкий спектр форматов, чем поддерживаемые кодеками. Пакет SDK делает это путем выполнения предварительной обработки преобразований для входных данных, например для изменения размера кадров видео или перевыборки звука. В любом случае необходимо убедиться, что форматы ввода для файлов, которые вы пишете, совпадают с данными, отправляемыми в модуль записи. Каждый кодек имеет входной формат носителя по умолчанию, который задается в модуле записи при загрузке профиля. Вы можете проверить формат ввода по умолчанию, вызвав [**ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

Видеокодеки поддерживают следующие форматы: ИЙУВ, I420, YV12, YUY2, UYVY, ИВЮ, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 и RGB 8. Аудиокодеки поддерживают аудио PCM.

Чтобы перечислить входные форматы, поддерживаемые кодеком, выполните следующие действия.

1.  Создайте объект модуля записи и задайте профиль для использования. Дополнительные сведения о настройке профилей в средстве записи см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).
2.  Укажите номер входного номера, для которого необходимо проверить форматы. Дополнительные сведения об идентификации входных номеров см. [в разделе Определение входных данных по номеру](to-identify-inputs-by-number.md).
3.  Получите общее число входных форматов, поддерживаемых требуемыми входными данными, вызвав [**ивмвритер:: жетинпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Выполните цикл по всем поддерживаемым входным форматам, выполнив следующие действия для каждого из них.
    -   Получите интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входного формата, вызвав [**Ивмвритер:: жетинпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Получение структуры [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для формата входных данных. Вызовите метод [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), передав параметру *птипе* **значение NULL** , чтобы получить размер структуры. Затем выделите память для хранения структуры и снова вызовите **жетмедиатипе** , чтобы получить структуру. [**Ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) наследует от [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), поэтому можно выполнять вызовы **жетмедиатипе** из экземпляра **ивминпутмедиапропс** , полученного на предыдущем шаге.
    -   Формат, описанный в разделе Структура [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) , содержит все необходимые сведения о формате входных данных. Базовый формат носителя определяется с помощью **WM \_ Media \_ Type.** подтип. Для видеопотоков элемент **пбформат** указывает на динамически выделенную структуру [**вмвидеоинфохеадер**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) , которая содержит дополнительные сведения о потоке, включая размер прямоугольника. Размер входных кадров не обязательно должен точно соответствовать размеру, поддерживаемому кодеком. Если они не совпадают, компоненты времени выполнения пакета SDK, во многих случаях, автоматически изменяют размер входных видеокадров на то, что может принимать кодек.

В следующем примере кода выполняется поиск входного формата подтипа, переданного в качестве параметра. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 




