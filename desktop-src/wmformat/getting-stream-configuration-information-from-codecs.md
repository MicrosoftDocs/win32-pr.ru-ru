---
title: Получение сведений о конфигурации потока из кодеков
description: Получение сведений о конфигурации потока из кодеков
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- потоки, конфигурации из кодеков
- кодеки, получение конфигураций потоков из
- потоки, форматы кодеков
- кодеки, форматы
- потоки, интерфейс ИвмкодеЦинфо
- ИвмкодеЦинфо, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104412683"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="0652d-109">Получение сведений о конфигурации потока из кодеков</span><span class="sxs-lookup"><span data-stu-id="0652d-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="0652d-110">Для потоков аудио и видео, использующих аудиокодеки Windows Media аудио и видео, необходимо получить значения для структур конфигурации потока из кодека, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="0652d-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="0652d-111">Хотя эти значения можно задать самостоятельно, использование кодеков гарантирует точность значений.</span><span class="sxs-lookup"><span data-stu-id="0652d-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="0652d-112">Не следует изменять значения этих структур, если только в документации специально не рекомендовано конкретное изменение.</span><span class="sxs-lookup"><span data-stu-id="0652d-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="0652d-113">Сведения из кодеков поступают в формате кодеков.</span><span class="sxs-lookup"><span data-stu-id="0652d-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="0652d-114">Каждый формат кодека — это единый формат потока, поддерживаемый кодеком.</span><span class="sxs-lookup"><span data-stu-id="0652d-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="0652d-115">Дополнительные сведения о форматах потоков см. в разделе [formats](formats.md).</span><span class="sxs-lookup"><span data-stu-id="0652d-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="0652d-116">Вы можете запросить информацию из кодеков Windows Media с помощью интерфейсов [**ивмкодеЦинфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)и [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) объекта диспетчера профилей.</span><span class="sxs-lookup"><span data-stu-id="0652d-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="0652d-117">Чтобы получить интерфейс [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) объекта диспетчера профилей, вызовите функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="0652d-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="0652d-118">Вызовите **QueryInterface** для **ивмпрофилеманажер** , чтобы получить **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="0652d-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="0652d-119">В следующих разделах описано, как получить необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="0652d-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="0652d-120">Section</span><span class="sxs-lookup"><span data-stu-id="0652d-120">Section</span></span>                                                                                                | <span data-ttu-id="0652d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="0652d-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0652d-122">Перечисление всех установленных кодеков Windows Media</span><span class="sxs-lookup"><span data-stu-id="0652d-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="0652d-123">Описывает, как использовать методы интерфейсов **ивмкодеЦинфо** и **IWMCodecInfo2** для получения имени и индекса кодека каждого установленного кодека Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0652d-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="0652d-124">Перечисление форматов кодеков</span><span class="sxs-lookup"><span data-stu-id="0652d-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="0652d-125">Описывает, как получить объекты конфигурации потока из кодеков для использования в профилях.</span><span class="sxs-lookup"><span data-stu-id="0652d-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0652d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0652d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0652d-127">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="0652d-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




