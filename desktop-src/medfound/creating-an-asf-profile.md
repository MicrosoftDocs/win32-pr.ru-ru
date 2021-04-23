---
description: В этом разделе описывается создание профиля ASF в Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Создание профиля ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682376"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="30e7b-103">Создание профиля ASF</span><span class="sxs-lookup"><span data-stu-id="30e7b-103">Creating an ASF Profile</span></span>

<span data-ttu-id="30e7b-104">В этом разделе описывается создание профиля ASF в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="30e7b-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="30e7b-105">Создать новый профиль</span><span class="sxs-lookup"><span data-stu-id="30e7b-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="30e7b-106">Получение профиля из объекта ASF Контентинфо</span><span class="sxs-lookup"><span data-stu-id="30e7b-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="30e7b-107">Получение профиля из дескриптора презентации</span><span class="sxs-lookup"><span data-stu-id="30e7b-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="30e7b-108">См. также</span><span class="sxs-lookup"><span data-stu-id="30e7b-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="30e7b-109">Создать новый профиль</span><span class="sxs-lookup"><span data-stu-id="30e7b-109">Create a New Profile</span></span>

<span data-ttu-id="30e7b-110">Чтобы создать пустой профиль ASF, вызовите функцию [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="30e7b-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="30e7b-111">Эта функция возвращает указатель на интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="30e7b-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="30e7b-112">Приложение может использовать этот интерфейс для добавления потоков в профиль и настройки каждого из потоков.</span><span class="sxs-lookup"><span data-stu-id="30e7b-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="30e7b-113">Дополнительные сведения см. в разделе [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="30e7b-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="30e7b-114">При необходимости приложение может добавлять взаимоисключающие объекты в два или более потоков.</span><span class="sxs-lookup"><span data-stu-id="30e7b-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="30e7b-115">См. раздел [Использование взаимного исключения для потоков ASF](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="30e7b-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="30e7b-116">Получение профиля из объекта ASF Контентинфо</span><span class="sxs-lookup"><span data-stu-id="30e7b-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="30e7b-117">Приложение может получить профиль ASF существующего файла ASF из [объекта ASF контентинфо](asf-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="30e7b-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="30e7b-118">Профиль уже настроен и содержит параметры для всех потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="30e7b-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="30e7b-119">Инициализируйте объект Контентинфо, анализируя объект заголовка ASF файла.</span><span class="sxs-lookup"><span data-stu-id="30e7b-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="30e7b-120">Это делается с помощью метода [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="30e7b-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="30e7b-121">После того как будут считаны все объекты заголовка и заполнена библиотека ASF, будет создан профиль для этого файла.</span><span class="sxs-lookup"><span data-stu-id="30e7b-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="30e7b-122">Приложение может получить указатель на этот инициализированный профиль, вызвав [**имфасфконтентинфо::-Profile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="30e7b-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="30e7b-123">Получение профиля из дескриптора презентации</span><span class="sxs-lookup"><span data-stu-id="30e7b-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="30e7b-124">Объект профиля существующего файла ASF можно получить из [дескриптора презентации](presentation-descriptors.md) для файла или из объекта [ASF контентинфо](asf-contentinfo-object.md) .</span><span class="sxs-lookup"><span data-stu-id="30e7b-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="30e7b-125">В этом случае профиль уже настроен и содержит параметры для всех потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="30e7b-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="30e7b-126">Это может быть полезно, если требуется изменить существующий профиль ASF.</span><span class="sxs-lookup"><span data-stu-id="30e7b-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="30e7b-127">Например, может потребоваться повторное Кодирование видеофайла Windows Media с более низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="30e7b-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="30e7b-128">Чтобы получить профиль из дескриптора презентации, вызовите [**мфкреатеасфпрофилефромпресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="30e7b-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="30e7b-129">Эта функция анализирует дескриптор представления и заполняет профиль ASF сведениями о файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="30e7b-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="30e7b-130">Функция возвращает указатель на интерфейс Имфасфпрофиле.</span><span class="sxs-lookup"><span data-stu-id="30e7b-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="30e7b-131">Затем этот интерфейс можно использовать для изменения профиля.</span><span class="sxs-lookup"><span data-stu-id="30e7b-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="30e7b-132">Чтобы получить дескриптор представления, вызовите один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="30e7b-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="30e7b-133">В источнике носителя ASF вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="30e7b-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="30e7b-134">Из объекта [ASF контентинфо](asf-contentinfo-object.md) вызовите [**Имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="30e7b-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="30e7b-135">Перед вызовом этого метода убедитесь, что объект Контентинфо инициализирован для чтения.</span><span class="sxs-lookup"><span data-stu-id="30e7b-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="30e7b-136">Дополнительные сведения см. в разделе "инициализация объекта Контентинфо из существующего файла ASF" [статьи чтение объекта заголовка ASF существующего файла](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="30e7b-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="30e7b-137">Однако если у вас уже есть инициализированный объект Контентинфо, вы можете получить профиль непосредственно из него.</span><span class="sxs-lookup"><span data-stu-id="30e7b-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="30e7b-138">Это описано в подразделе «Получение профиля из объекта Контентинфо» далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="30e7b-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="30e7b-139">В следующем примере показано, как создать профиль из дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="30e7b-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="30e7b-140">Функция создает источник мультимедиа для файла, получает дескриптор представления из источника мультимедиа и создает профиль.</span><span class="sxs-lookup"><span data-stu-id="30e7b-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="30e7b-141">В этом примере предполагается, что *pszFileName* указывает URL-адрес файла ASF.</span><span class="sxs-lookup"><span data-stu-id="30e7b-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="30e7b-142">В этом примере для высвобождения указателей интерфейса используется [саферелеасе](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="30e7b-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30e7b-143">См. также</span><span class="sxs-lookup"><span data-stu-id="30e7b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e7b-144">Профиль ASF</span><span class="sxs-lookup"><span data-stu-id="30e7b-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



