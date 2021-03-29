---
description: В этом разделе описывается, как использовать API перекодирования для повторной кодировки файлов мультимедиа. API перекодирования появился в Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API перекодирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898710"
---
# <a name="transcode-api"></a><span data-ttu-id="9aa57-104">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="9aa57-104">Transcode API</span></span>

<span data-ttu-id="9aa57-105">В этом разделе описывается, как использовать API перекодирования для повторной кодировки файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9aa57-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="9aa57-106">API перекодирования появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9aa57-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="9aa57-107">*Перекодирование* — это преобразование файла цифрового мультимедиа из одного формата в другой.</span><span class="sxs-lookup"><span data-stu-id="9aa57-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="9aa57-108">API перекодирования предназначен для использования с [сеансом мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="9aa57-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="9aa57-109">Это упрощает использование сеанса мультимедиа для определенных типов приложений для перекодирования:</span><span class="sxs-lookup"><span data-stu-id="9aa57-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="9aa57-110">Кодирование с постоянной скоростью (CBR), где скорость целевого бита известна заранее.</span><span class="sxs-lookup"><span data-stu-id="9aa57-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="9aa57-111">Не более одного звукового потока и одного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="9aa57-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="9aa57-112">Кодирование из файла и в файл.</span><span class="sxs-lookup"><span data-stu-id="9aa57-112">Encoding from and to a file.</span></span>

<span data-ttu-id="9aa57-113">API перекодирования не поддерживает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="9aa57-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="9aa57-114">Переменная скорость (VBR) или многопроходная кодировка.</span><span class="sxs-lookup"><span data-stu-id="9aa57-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="9aa57-115">Несколько звуковых потоков или несколько видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="9aa57-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="9aa57-116">Защищенное DRM содержимое, отличное от ASF-файлов, защищенных с помощью WMDRM.</span><span class="sxs-lookup"><span data-stu-id="9aa57-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="9aa57-117">Потоковая передача в реальном времени, например потоковая передача в режиме реального времени или потоковая передача в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="9aa57-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="9aa57-118">Если приложение кодирования соответствует этим ограничениям, API-интерфейс перекодировки упрощает модель программирования, чем использование сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9aa57-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9aa57-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9aa57-119">In this section</span></span>



| <span data-ttu-id="9aa57-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="9aa57-120">Topic</span></span>                                                                                          | <span data-ttu-id="9aa57-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9aa57-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aa57-122">Сведения об API перекодирования</span><span class="sxs-lookup"><span data-stu-id="9aa57-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="9aa57-123">Общие сведения об API перекодирования.</span><span class="sxs-lookup"><span data-stu-id="9aa57-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="9aa57-124">Использование API перекодирования</span><span class="sxs-lookup"><span data-stu-id="9aa57-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="9aa57-125">Описывает, как приложение использует API перекодирования.</span><span class="sxs-lookup"><span data-stu-id="9aa57-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="9aa57-126">Учебник. Кодирование файла MP4</span><span class="sxs-lookup"><span data-stu-id="9aa57-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="9aa57-127">Пошаговое руководство, в котором показано, как использовать API перекодировки для кодирования MP4-файла.</span><span class="sxs-lookup"><span data-stu-id="9aa57-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="9aa57-128">Учебник. кодирование WMA-файла</span><span class="sxs-lookup"><span data-stu-id="9aa57-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="9aa57-129">Показывает, как использовать API перекодировки для кодирования WMA-файла.</span><span class="sxs-lookup"><span data-stu-id="9aa57-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="9aa57-130">В этом руководстве приводится изменение кода, показанного в [руководстве: кодирование файла MP4](tutorial--encoding-an-mp4-file-.md), поэтому сначала следует ознакомиться с этим руководством.</span><span class="sxs-lookup"><span data-stu-id="9aa57-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9aa57-131">См. также</span><span class="sxs-lookup"><span data-stu-id="9aa57-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa57-132">Кодировка и разработка файлов</span><span class="sxs-lookup"><span data-stu-id="9aa57-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="9aa57-133">Media Foundation: основные понятия</span><span class="sxs-lookup"><span data-stu-id="9aa57-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="9aa57-134">Общие сведения о кодировке в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9aa57-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




