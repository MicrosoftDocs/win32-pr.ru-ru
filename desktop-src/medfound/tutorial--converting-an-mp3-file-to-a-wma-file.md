---
description: В этом руководстве показано, как использовать API перекодировки для кодирования WMA-файла Windows Media Audio.
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: Учебник. кодирование WMA-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692782"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="240ad-103">Учебник. кодирование WMA-файла</span><span class="sxs-lookup"><span data-stu-id="240ad-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="240ad-104">В этом руководстве показано, как использовать [API перекодировки](transcode-api.md) для кодирования WMA-файла Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="240ad-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="240ad-105">В этом руководстве используется большая часть кода из учебника [Кодирование файла MP4](tutorial--encoding-an-mp4-file-.md), поэтому сначала ознакомьтесь с этим руководством.</span><span class="sxs-lookup"><span data-stu-id="240ad-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="240ad-106">Единственным кодом, который отличается, является функция `CreateTranscodeProfile` , которая создает профиль перекодирования.</span><span class="sxs-lookup"><span data-stu-id="240ad-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="240ad-107">Создание профиля перекодирования</span><span class="sxs-lookup"><span data-stu-id="240ad-107">Create the Transcode Profile</span></span>

<span data-ttu-id="240ad-108">*Профиль* перекодировки описывает параметры кодирования и контейнер файла.</span><span class="sxs-lookup"><span data-stu-id="240ad-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="240ad-109">Для файлов WMA контейнер файла представляет собой файл формата ASF.</span><span class="sxs-lookup"><span data-stu-id="240ad-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="240ad-110">Файл ASF содержит аудиопоток, закодированный с помощью [**кодировщика Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="240ad-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="240ad-111">Чтобы создать топологию перекодирования, создайте профиль перекодирования и укажите параметры для аудиопотока и контейнера.</span><span class="sxs-lookup"><span data-stu-id="240ad-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="240ad-112">Затем создайте топологию, указав источник входных данных, URL-адрес вывода и профиль перекодирования.</span><span class="sxs-lookup"><span data-stu-id="240ad-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="240ad-113">Чтобы создать профиль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="240ad-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="240ad-114">Вызовите функцию [**мфкреатетранскодепрофиле**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) , чтобы создать пустой профиль перекодирования.</span><span class="sxs-lookup"><span data-stu-id="240ad-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="240ad-115">Вызовите [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , чтобы получить список типов звуковых носителей из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="240ad-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="240ad-116">Эта функция возвращает указатель [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , представляющий коллекцию указателей [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="240ad-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="240ad-117">Выберите тип мультимедиа, соответствующий требованиям к кодированию, и скопируйте атрибуты в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="240ad-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="240ad-118">В этом руководстве используется первый тип носителя в списке.</span><span class="sxs-lookup"><span data-stu-id="240ad-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="240ad-119">Вызовите [**имфколлектион:: «элемент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) », чтобы выбрать тип звукового носителя из списка.</span><span class="sxs-lookup"><span data-stu-id="240ad-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="240ad-120">Запросите тип носителя, чтобы получить указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) хранилища атрибутов типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="240ad-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="240ad-121">Вызовите [**имфаттрибутес:: NOCOUNT**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) , чтобы получить количество атрибутов, содержащихся в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="240ad-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="240ad-122">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="240ad-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="240ad-123">Вызовите метод [**имфаттрибутес:: копяллитемс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) , чтобы скопировать атрибуты из типа мультимедиа в новое хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="240ad-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="240ad-124">Вызовите метод [**имфтранскодепрофиле:: сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) , чтобы задать атрибуты для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="240ad-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="240ad-125">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов для атрибутов уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="240ad-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="240ad-126">Задайте для [атрибута \_ \_ контаинертипе перекодировки MF](mf-transcode-containertype.md) значение **мфтранскодеконтаинертипе \_ ASF**, которое указывает контейнер файла ASF.</span><span class="sxs-lookup"><span data-stu-id="240ad-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="240ad-127">Вызовите метод [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) , чтобы задать атрибуты уровня контейнера для профиля.</span><span class="sxs-lookup"><span data-stu-id="240ad-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="240ad-128">См. также</span><span class="sxs-lookup"><span data-stu-id="240ad-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="240ad-129">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="240ad-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



