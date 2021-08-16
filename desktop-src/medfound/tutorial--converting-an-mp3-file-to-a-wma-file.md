---
description: в этом руководстве показано, как использовать API перекодирования для кодирования файла Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: Учебник. кодирование WMA-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86301f301bb4f39f6c9258ec3eacfdd1646af8e76791e2df37ae6bf7d8f89880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972793"
---
# <a name="tutorial-encoding-a-wma-file"></a>Учебник. кодирование WMA-файла

в этом руководстве показано, как использовать [API перекодирования](transcode-api.md) для кодирования файла Windows Media Audio (WMA).

В этом руководстве используется большая часть кода из учебника [Кодирование файла MP4](tutorial--encoding-an-mp4-file-.md), поэтому сначала ознакомьтесь с этим руководством. Единственным кодом, который отличается, является функция `CreateTranscodeProfile` , которая создает профиль перекодирования.

## <a name="create-the-transcode-profile"></a>Создание профиля перекодирования

*Профиль* перекодировки описывает параметры кодирования и контейнер файла. Для файлов WMA контейнер файла представляет собой файл формата ASF. файл ASF содержит аудиопоток, закодированный с помощью [**Windows Media audio Encoder**](windowsmediaaudioencoder.md).

Чтобы создать топологию перекодирования, создайте профиль перекодирования и укажите параметры для аудиопотока и контейнера. Затем создайте топологию, указав источник входных данных, URL-адрес вывода и профиль перекодирования.

Чтобы создать профиль, выполните следующие действия.

1.  Вызовите функцию [**мфкреатетранскодепрофиле**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) , чтобы создать пустой профиль перекодирования.
2.  Вызовите [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , чтобы получить список типов звуковых носителей из кодировщика. Эта функция возвращает указатель [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , представляющий коллекцию указателей [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .
3.  Выберите тип мультимедиа, соответствующий требованиям к кодированию, и скопируйте атрибуты в хранилище атрибутов. В этом руководстве используется первый тип носителя в списке.
    -   Вызовите [**имфколлектион:: «элемент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) », чтобы выбрать тип звукового носителя из списка.
    -   Запросите тип носителя, чтобы получить указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) хранилища атрибутов типа мультимедиа.
    -   Вызовите [**имфаттрибутес:: NOCOUNT**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) , чтобы получить количество атрибутов, содержащихся в типе мультимедиа.
    -   Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.
    -   Вызовите метод [**имфаттрибутес:: копяллитемс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) , чтобы скопировать атрибуты из типа мультимедиа в новое хранилище атрибутов.
4.  Вызовите метод [**имфтранскодепрофиле:: сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) , чтобы задать атрибуты для аудиопотока.
5.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов для атрибутов уровня контейнера.
6.  Задайте для [атрибута \_ \_ контаинертипе перекодировки MF](mf-transcode-containertype.md) значение **мфтранскодеконтаинертипе \_ ASF**, которое указывает контейнер файла ASF.
7.  Вызовите метод [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) , чтобы задать атрибуты уровня контейнера для профиля.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[API перекодирования](transcode-api.md)
</dt> </dl>

 

 



