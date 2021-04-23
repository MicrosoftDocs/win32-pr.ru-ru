---
description: Сведения о заголовке ASF хранятся в объектах заголовка ASF файла мультимедиа.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Получение сведений из объектов заголовка ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710813"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="b3dd0-103">Получение сведений из объектов заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="b3dd0-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="b3dd0-104">Сведения о заголовке ASF хранятся в объектах заголовка ASF файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="b3dd0-105">Media Foundation предоставляет [объект ASF контентинфо](asf-contentinfo-object.md) для работы с объектом Header.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="b3dd0-106">Заполненный объект Контентинфо требуется для того, чтобы приложение читало данные заголовка существующего файла.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="b3dd0-107">Это достигается путем вызова [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="b3dd0-108">Если синтаксический анализ успешно завершен, Библиотека ASF для файла, которая поддерживается внутренне Media Foundation, заполняется данными заголовка из различных объектов заголовков.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="b3dd0-109">Некоторые из этих свойств предоставляются приложению, которое может извлекать через атрибуты дескриптора презентации, дескриптора потока, профиля и свойств метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="b3dd0-110">Полный список атрибутов см. в разделе [атрибуты Media Foundation для объектов заголовка ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="b3dd0-111">Получение сведений о заголовке из дескриптора презентации</span><span class="sxs-lookup"><span data-stu-id="b3dd0-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="b3dd0-112">Объект дескриптора представления содержит описание конкретного источника мультимедиа, в данном случае источник медиа ASF.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="b3dd0-113">Если вызов **парсехеадер** завершается успешно, сведения на уровне файла из объекта заголовка сохраняются как атрибуты в дескрипторе презентации.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="b3dd0-114">Чтобы создать дескриптор представления, вызовите метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="b3dd0-115">Этот метод возвращает указатель на заполненный объект дескриптора представления, содержащий эти атрибуты для ASF-файла, связанного с объектом Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="b3dd0-116">Чтобы получить значения для конкретных атрибутов, вызовите методы **имфаттрибутес:: жеткскскс** в дескрипторе представления и укажите **атрибут \_ MF \_ PD ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="b3dd0-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="b3dd0-117">В следующем примере кода извлекается длительность воспроизведения ASF-файла, указанного в объекте Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="b3dd0-118">Дополнительные сведения о дескрипторах презентаций в целом см. в разделе [дескрипторы представления](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="b3dd0-119">Полный набор атрибутов дескриптора презентации см. в разделе [атрибуты дескриптора представления](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="b3dd0-120">Получение сведений о заголовке из дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="b3dd0-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="b3dd0-121">Объект дескриптора потока предоставляет интерфейс [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) и описывает характеристики потоков в файле.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="b3dd0-122">Дескриптор представления для содержимого ASF содержит один или несколько дескрипторов потоков, представляющих потоки, перечисленные в объекте Header.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="b3dd0-123">После успешного завершения вызова [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) базовые дескрипторы потоков заполняются данными уровня потока из различных объектов заголовка.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="b3dd0-124">Чтобы получить дескриптор потока для потока ASF, вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) в дескрипторе представления, созданном из объекта контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="b3dd0-125">Некоторые свойства потока задаются как атрибуты дескрипторов потока.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="b3dd0-126">Вызовите методы **имфаттрибутес:: жеткскскс** в дескрипторе потока и укажите **атрибут \_ MF \_ SD \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="b3dd0-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="b3dd0-127">Полный набор атрибутов дескриптора потока см. в разделе атрибуты дескриптора потока ASF, перечисленные в разделе [атрибуты дескриптора потока](stream-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="b3dd0-128">Получение сведений о заголовках из объекта Profile</span><span class="sxs-lookup"><span data-stu-id="b3dd0-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="b3dd0-129">Помимо дескрипторов потоков, объект профиля ASF также описывает свойства потока.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="b3dd0-130">Чтобы получить профиль существующего файла ASF, вызовите [**имфасфконтентинфо:: onprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="b3dd0-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="b3dd0-131">Объект профиля ASF, возвращенный этим методом, не содержит атрибутов **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="b3dd0-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="b3dd0-132">Эти атрибуты доступны приложению только после того, как оно вызовет [**мфкреатеасфпрофилефромпресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) для создания объекта профиля из дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="b3dd0-133">Профиль можно использовать для получения указателей на объекты взаимного исключения и определения приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="b3dd0-134">Дополнительные сведения об объекте Profile см. в разделе [профиль ASF](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="b3dd0-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="b3dd0-135">Получение метаданных из объектов заголовков</span><span class="sxs-lookup"><span data-stu-id="b3dd0-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="b3dd0-136">Файл ASF может содержать несколько свойств метаданных, заданных во время кодирования файлов.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="b3dd0-137">Приложение может перечислить эти свойства с помощью объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="b3dd0-138">Некоторые из этих свойств, такие как сведения о переменной скорости (VBR), доступны приложению с помощью атрибутов в дескрипторе представления, потоках и типах мультимедиа для файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b3dd0-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="b3dd0-139">Эти атрибуты задаются для объекта Контентинфо во время инициализации через вызов [**парсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="b3dd0-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3dd0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="b3dd0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3dd0-141">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="b3dd0-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



