---
description: В этом разделе описывается работа с профилями ASF в Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Профиль ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539647"
---
# <a name="asf-profile"></a><span data-ttu-id="8ca6a-103">Профиль ASF</span><span class="sxs-lookup"><span data-stu-id="8ca6a-103">ASF Profile</span></span>

<span data-ttu-id="8ca6a-104">В этом разделе описывается работа с профилями ASF в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="8ca6a-105">Файл в формате ASF содержит один или несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="8ca6a-106">Для каждого потока заголовок ASF содержит заголовок свойства потока, описывающий поток.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="8ca6a-107">На уровне [вмконтаинер](wmcontainer-asf-components.md) для установки или чтения свойств потоков ASF используются следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="8ca6a-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="8ca6a-108">Объект *профиля ASF* : описывает потоки и их связи друг с другом.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="8ca6a-109">Объект профиля ASF предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="8ca6a-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="8ca6a-110">Объект *конфигурации потока* : описывает один поток.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="8ca6a-111">Объект конфигурации потока содержит тип мультимедиа, описывающий формат потока.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="8ca6a-112">Для потоков аудио и видео тип мультимедиа точно описывает настройку потока и используется кодеками, которые кодируют или декодировать поток.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="8ca6a-113">Объект конфигурации потока предоставляет интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="8ca6a-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="8ca6a-114">Допустимый профиль ASF содержит по крайней мере один объект конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="8ca6a-115">Объект *взаимного исключения* : описывает несколько потоков, которые не предназначены для одновременного чтения.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="8ca6a-116">Объект взаимного исключения предоставляет интерфейс [**имфасфмутуалексклусион**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) .</span><span class="sxs-lookup"><span data-stu-id="8ca6a-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="8ca6a-117">Профиль ASF содержит ноль или более взаимоисключающих объектов.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="8ca6a-118">На следующей схеме показана связь между профилем ASF и объектами, содержащимися в профиле.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![схема дерева узла профиля ASF с дочерними узлами конфигурации потока; Первый указывает на тип носителя, два следующих для взаимного исключения](images/asf-components02.png)

<span data-ttu-id="8ca6a-120">Для воспроизведения профиль ASF используется для перечисления потоков и поиска форматов потоков.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="8ca6a-121">Для кодирования профиль ASF используется для настройки потоков в конечном файле.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="8ca6a-122">Профиль ASF также используется для настройки [приемника мультимедиа ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="8ca6a-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="8ca6a-123">Для каждого потока в профиле ASF приемник мультимедиа ASF создает соответствующий приемник потока.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8ca6a-124">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="8ca6a-124">In this section</span></span>



| <span data-ttu-id="8ca6a-125">Раздел</span><span class="sxs-lookup"><span data-stu-id="8ca6a-125">Topic</span></span>                                                                                           | <span data-ttu-id="8ca6a-126">Описание</span><span class="sxs-lookup"><span data-stu-id="8ca6a-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8ca6a-127">Создание профиля ASF</span><span class="sxs-lookup"><span data-stu-id="8ca6a-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="8ca6a-128">Описывает создание объекта профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="8ca6a-129">Создание и настройка потоков ASF</span><span class="sxs-lookup"><span data-stu-id="8ca6a-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="8ca6a-130">Описывает добавление потоков в профиль ASF.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="8ca6a-131">Использование взаимного исключения для потоков ASF</span><span class="sxs-lookup"><span data-stu-id="8ca6a-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="8ca6a-132">Описывает добавление взаимоисключающих исключений в потоки ASF.</span><span class="sxs-lookup"><span data-stu-id="8ca6a-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8ca6a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="8ca6a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ca6a-134">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="8ca6a-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="8ca6a-135">Учебник. 1. Передача кодирования мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="8ca6a-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="8ca6a-136">Руководство. запись файла WMA с помощью CBR Encoding</span><span class="sxs-lookup"><span data-stu-id="8ca6a-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="8ca6a-137">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="8ca6a-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




