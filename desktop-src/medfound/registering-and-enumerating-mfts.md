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
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="9969b-103">Регистрация и перечисление МФТС</span><span class="sxs-lookup"><span data-stu-id="9969b-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="9969b-104">В этом разделе описывается, как перечислить Media Foundation преобразования и как зарегистрировать настраиваемую таблицу MFT, чтобы приложения могли его обнаружить.</span><span class="sxs-lookup"><span data-stu-id="9969b-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="9969b-105">Перечисление МФТС</span><span class="sxs-lookup"><span data-stu-id="9969b-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="9969b-106">Регистрация МФТС</span><span class="sxs-lookup"><span data-stu-id="9969b-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="9969b-107">См. также</span><span class="sxs-lookup"><span data-stu-id="9969b-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="9969b-108">Перечисление МФТС</span><span class="sxs-lookup"><span data-stu-id="9969b-108">Enumerating MFTs</span></span>

<span data-ttu-id="9969b-109">Для обнаружения МФТС, зарегистрированных в системе, приложение может вызвать функцию [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="9969b-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="9969b-110">Для этой функции требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9969b-110">This function requires to Windows 7.</span></span> <span data-ttu-id="9969b-111">До Windows 7 в приложениях вместо этого следует использовать функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="9969b-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="9969b-112">Эта функция принимает в качестве входных данных следующие данные:</span><span class="sxs-lookup"><span data-stu-id="9969b-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="9969b-113">Категория MFT для перечисления, например видеодекодер или звуковой декодер.</span><span class="sxs-lookup"><span data-stu-id="9969b-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="9969b-114">Формат входного или выходного формата для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9969b-114">An input or output format to match.</span></span>
-   <span data-ttu-id="9969b-115">Флаги, указывающие дополнительные условия поиска.</span><span class="sxs-lookup"><span data-stu-id="9969b-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="9969b-116">Функция возвращает массив [**имфактиватеных**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателей, каждый из которых представляет таблицу MFT, соответствующую критериям перечисления.</span><span class="sxs-lookup"><span data-stu-id="9969b-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="9969b-117">Например, следующий код выполняет перечисление декодеров видео Windows Media:</span><span class="sxs-lookup"><span data-stu-id="9969b-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


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



<span data-ttu-id="9969b-118">По умолчанию некоторые типы MFT исключаются из перечисления, включая асинхронные МФТС, оборудование МФТС и МФТС с помощью реструктур использования полей.</span><span class="sxs-lookup"><span data-stu-id="9969b-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="9969b-119">Они исключены, так как все они нуждаются в специальной обработке какого-либо рода.</span><span class="sxs-lookup"><span data-stu-id="9969b-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="9969b-120">Используйте параметр *flags* параметра [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , чтобы изменить значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9969b-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="9969b-121">Например, чтобы включить оборудование МФТС в результаты перечисления, установите флаг **перечисления MFT для \_ \_ флага \_ оборудования** :</span><span class="sxs-lookup"><span data-stu-id="9969b-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


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



## <a name="registering-mfts"></a><span data-ttu-id="9969b-122">Регистрация МФТС</span><span class="sxs-lookup"><span data-stu-id="9969b-122">Registering MFTs</span></span>

<span data-ttu-id="9969b-123">При регистрации Media Foundation преобразования (MFT) в реестр записываются два типа данных:</span><span class="sxs-lookup"><span data-stu-id="9969b-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="9969b-124">Идентификатор CLSID MFT, чтобы клиенты могли вызывать **CoCreateInstance** или **кожетклассобжект** для создания экземпляра MFT.</span><span class="sxs-lookup"><span data-stu-id="9969b-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="9969b-125">Эта запись реестра соответствует стандартному формату фабрик классов COM.</span><span class="sxs-lookup"><span data-stu-id="9969b-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="9969b-126">Дополнительные сведения см. в документации по Windows SDK для модели COM.</span><span class="sxs-lookup"><span data-stu-id="9969b-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="9969b-127">Сведения, позволяющие приложению перечислять МФТС по функциональной категории.</span><span class="sxs-lookup"><span data-stu-id="9969b-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="9969b-128">Чтобы создать записи перечисления MFT в реестре, вызовите функцию [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="9969b-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="9969b-129">Можно включить следующие сведения о MFT:</span><span class="sxs-lookup"><span data-stu-id="9969b-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="9969b-130">Категория MFT, например декодер видео или видеокодировщик.</span><span class="sxs-lookup"><span data-stu-id="9969b-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="9969b-131">Список категорий см. в разделе [**MFT \_ Category**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="9969b-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="9969b-132">Список форматов входных и выходных данных, поддерживаемых MFT.</span><span class="sxs-lookup"><span data-stu-id="9969b-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="9969b-133">Каждый формат определяется основным типом и подтипом.</span><span class="sxs-lookup"><span data-stu-id="9969b-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="9969b-134">(Чтобы получить более подробные сведения о форматировании, клиент должен создать таблицу MFT и вызвать методы [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) Загрузчик топологии использует эти сведения при разрешении частичной топологии.</span><span class="sxs-lookup"><span data-stu-id="9969b-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="9969b-135">Чтобы удалить записи из реестра, вызовите [**мфтунрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="9969b-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="9969b-136">В следующем коде показано, как зарегистрировать таблицу MFT.</span><span class="sxs-lookup"><span data-stu-id="9969b-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="9969b-137">В этом примере предполагается, что MFT является видеодействием, которое поддерживает те же форматы как для входных, так и для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9969b-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9969b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9969b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9969b-139">Поле ограничений использования</span><span class="sxs-lookup"><span data-stu-id="9969b-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="9969b-140">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9969b-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



