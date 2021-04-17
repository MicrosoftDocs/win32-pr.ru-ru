---
description: Для преобразования файлов мультимедиа в формат ASF можно использовать кодировщики Windows Media. Чтобы использовать эти кодировщики, они должны быть зарегистрированы в системе.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Создание кодировщика с помощью функции CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692771"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Создание кодировщика с помощью функции CoCreateInstance

Для преобразования файлов мультимедиа в формат ASF можно использовать кодировщики Windows Media. Чтобы использовать эти кодировщики, они должны быть зарегистрированы в системе. Кодировщики реализуются в виде [Media Foundation преобразований](media-foundation-transforms.md) (МФТС) и должны предоставлять интерфейс имфтрансформ. В этом разделе описывается, как приложение может получить указатель на необходимый интерфейс Имфтрансформ кодировщика MFT и создать его экземпляр для использования.

Дополнительные сведения о регистрации кодировщика см. [в разделе Создание экземпляра MFT кодировщика](instantiating-the-encoder-mft.md).

-   [Использование интерфейса Имфтрансформ кодировщика](#creating-an-encoder-by-using-cocreateinstance)
    -   [Пример создания кодировщика](#encoder-creation-example)
-   [См. также](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Использование интерфейса Имфтрансформ кодировщика

После успешной регистрации кодировщиков Windows Media в системе приложение может перечислить кодировщики, вызвав [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Для поиска правильного кодировщика необходимо указать следующее:

-   Идентификатор GUID, представляющий категорию, которая является **\_ \_ \_ кодировщиком** **\_ аудио- \_ \_ кодировщика** или категории MFT в формате MFT.

-   Формат для сопоставления. Это значение задается [**в \_ \_ \_ информационной структуре реестра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , указывающей основной тип и подтип типа мультимедиа, в котором кодировщик будет создавать образцы. Эта структура передается в параметр *паутпуттипе* . Дополнительные сведения о поддерживаемых типах см. в разделе Типы [носителей GUID](media-type-guids.md).

    > [!Note]  
    > Сведения о типе входных данных в параметре *пинпуттипе* не являются обязательными. Это обусловлено тем, что тип входных данных известен приложению, а кодировщику требуется, чтобы входной поток наследовался в несжатом формате.

     

[**Мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) возвращает массив указателей [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для МФТС кодировщика, соответствующих условиям поиска. Можно создать экземпляр кодировщика, вызвав функцию COM **CoCreateInstance** и ПЕРЕДАВ идентификатор CLSID кодировщика, который вы хотите использовать. Эта функция возвращает указатель на интерфейс **имфтрансформ** , представляющий кодировщик. Дополнительные сведения об этом вызове функции см. в документации по Windows SDK для модели COM.

### <a name="encoder-creation-example"></a>Пример создания кодировщика

В следующем примере кода показано, как создать аудио или видео кодировщик.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание экземпляра MFT для кодировщика](instantiating-the-encoder-mft.md)
</dt> <dt>

[Кодировщики Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



