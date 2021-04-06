---
description: В этом разделе описывается, как перечислить Media Foundation преобразования и как зарегистрировать настраиваемую таблицу MFT, чтобы приложения могли его обнаружить.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Регистрация и перечисление МФТС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991416"
---
# <a name="registering-and-enumerating-mfts"></a>Регистрация и перечисление МФТС

В этом разделе описывается, как перечислить Media Foundation преобразования и как зарегистрировать настраиваемую таблицу MFT, чтобы приложения могли его обнаружить.

-   [Перечисление МФТС](#registering-and-enumerating-mfts)
-   [Регистрация МФТС](#registering-mfts)
-   [См. также](#related-topics)

## <a name="enumerating-mfts"></a>Перечисление МФТС

Для обнаружения МФТС, зарегистрированных в системе, приложение может вызвать функцию [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

> [!Note]  
> Для этой функции требуется Windows 7. До Windows 7 в приложениях вместо этого следует использовать функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

 

Эта функция принимает в качестве входных данных следующие данные:

-   Категория MFT для перечисления, например видеодекодер или звуковой декодер.
-   Формат входного или выходного формата для сопоставления.
-   Флаги, указывающие дополнительные условия поиска.

Функция возвращает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей, каждый из которых представляет таблицу MFT, соответствующую критериям перечисления.

Например, следующий код выполняет перечисление декодеров видео Windows Media:


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



По умолчанию некоторые типы MFT исключаются из перечисления, включая асинхронные МФТС, оборудование МФТС и МФТС с помощью реструктур использования полей. Они исключены, так как все они нуждаются в специальной обработке какого-либо рода. Используйте параметр *flags* параметра [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , чтобы изменить значение по умолчанию. Например, чтобы включить оборудование МФТС в результаты перечисления, установите флаг **перечисления MFT для \_ \_ флага \_ оборудования** :


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>Регистрация МФТС

При регистрации Media Foundation преобразования (MFT) в реестр записываются два типа данных:

-   Идентификатор CLSID MFT, чтобы клиенты могли вызывать **CoCreateInstance** или **кожетклассобжект** для создания экземпляра MFT. Эта запись реестра соответствует стандартному формату фабрик классов COM. Дополнительные сведения см. в документации по Windows SDK для модели COM.
-   Сведения, позволяющие приложению перечислять МФТС по функциональной категории.

Чтобы создать записи перечисления MFT в реестре, вызовите функцию [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . Можно включить следующие сведения о MFT:

-   Категория MFT, например декодер видео или видеокодировщик. Список категорий см. в разделе [**MFT \_ Category**](mft-category.md).
-   Список форматов входных и выходных данных, поддерживаемых MFT. Каждый формат определяется основным типом и подтипом. (Чтобы получить более подробные сведения о форматировании, клиент должен создать таблицу MFT и вызвать методы [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) Загрузчик топологии использует эти сведения при разрешении частичной топологии.

Чтобы удалить записи из реестра, вызовите [**мфтунрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

В следующем коде показано, как зарегистрировать таблицу MFT. В этом примере предполагается, что MFT является видеодействием, которое поддерживает те же форматы как для входных, так и для выходных данных.


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Поле ограничений использования](field-of-use-restrictions.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



