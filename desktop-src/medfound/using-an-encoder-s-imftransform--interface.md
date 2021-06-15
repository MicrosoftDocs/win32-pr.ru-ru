---
description: Для преобразования файлов мультимедиа в формат ASF можно использовать кодировщики Windows Media. Сведения о создании кодировщика с помощью CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Создание кодировщика с помощью функции CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068470"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="71bca-104">Создание кодировщика с помощью функции CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="71bca-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="71bca-105">Для преобразования файлов мультимедиа в формат ASF можно использовать кодировщики Windows Media.</span><span class="sxs-lookup"><span data-stu-id="71bca-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="71bca-106">Чтобы использовать эти кодировщики, они должны быть зарегистрированы в системе.</span><span class="sxs-lookup"><span data-stu-id="71bca-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="71bca-107">Кодировщики реализуются в виде [Media Foundation преобразований](media-foundation-transforms.md) (МФТС) и должны предоставлять интерфейс имфтрансформ.</span><span class="sxs-lookup"><span data-stu-id="71bca-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="71bca-108">В этом разделе описывается, как приложение может получить указатель на необходимый интерфейс Имфтрансформ кодировщика MFT и создать его экземпляр для использования.</span><span class="sxs-lookup"><span data-stu-id="71bca-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="71bca-109">Дополнительные сведения о регистрации кодировщика см. [в разделе Создание экземпляра MFT кодировщика](instantiating-the-encoder-mft.md).</span><span class="sxs-lookup"><span data-stu-id="71bca-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="71bca-110">Использование интерфейса Имфтрансформ кодировщика</span><span class="sxs-lookup"><span data-stu-id="71bca-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="71bca-111">Пример создания кодировщика</span><span class="sxs-lookup"><span data-stu-id="71bca-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="71bca-112">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="71bca-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="71bca-113">Использование интерфейса Имфтрансформ кодировщика</span><span class="sxs-lookup"><span data-stu-id="71bca-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="71bca-114">После успешной регистрации кодировщиков Windows Media в системе приложение может перечислить кодировщики, вызвав [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span><span class="sxs-lookup"><span data-stu-id="71bca-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="71bca-115">Для поиска правильного кодировщика необходимо указать следующее:</span><span class="sxs-lookup"><span data-stu-id="71bca-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="71bca-116">Идентификатор GUID, представляющий категорию, которая является **\_ \_ \_ кодировщиком** **\_ аудио- \_ \_ кодировщика** или категории MFT в формате MFT.</span><span class="sxs-lookup"><span data-stu-id="71bca-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="71bca-117">Формат для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="71bca-117">The format to match.</span></span> <span data-ttu-id="71bca-118">Это значение задается [**в \_ \_ \_ информационной структуре реестра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , указывающей основной тип и подтип типа мультимедиа, в котором кодировщик будет создавать образцы.</span><span class="sxs-lookup"><span data-stu-id="71bca-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="71bca-119">Эта структура передается в параметр *паутпуттипе* .</span><span class="sxs-lookup"><span data-stu-id="71bca-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="71bca-120">Дополнительные сведения о поддерживаемых типах см. в разделе Типы [носителей GUID](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="71bca-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="71bca-121">Сведения о типе входных данных в параметре *пинпуттипе* не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="71bca-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="71bca-122">Это обусловлено тем, что тип входных данных известен приложению, а кодировщику требуется, чтобы входной поток наследовался в несжатом формате.</span><span class="sxs-lookup"><span data-stu-id="71bca-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="71bca-123">[**Мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) возвращает массив указателей [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для МФТС кодировщика, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="71bca-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="71bca-124">Можно создать экземпляр кодировщика, вызвав функцию COM **CoCreateInstance** и ПЕРЕДАВ идентификатор CLSID кодировщика, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="71bca-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="71bca-125">Эта функция возвращает указатель на интерфейс **имфтрансформ** , представляющий кодировщик.</span><span class="sxs-lookup"><span data-stu-id="71bca-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="71bca-126">Дополнительные сведения об этом вызове функции см. в документации по Windows SDK для модели COM.</span><span class="sxs-lookup"><span data-stu-id="71bca-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="71bca-127">Пример создания кодировщика</span><span class="sxs-lookup"><span data-stu-id="71bca-127">Encoder Creation Example</span></span>

<span data-ttu-id="71bca-128">В следующем примере кода показано, как создать аудио или видео кодировщик.</span><span class="sxs-lookup"><span data-stu-id="71bca-128">The following code example shows how to create an audio or video encoder.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="71bca-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="71bca-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71bca-130">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="71bca-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="71bca-131">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="71bca-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



