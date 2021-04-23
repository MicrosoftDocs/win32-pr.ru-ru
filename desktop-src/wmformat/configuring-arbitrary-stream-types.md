---
title: Настройка произвольных типов потоков
description: Настройка произвольных типов потоков
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- потоки, Настройка произвольных типов потоков
- кодеки, Настройка произвольных типов потоков
- потоки, Женпрофиле
- кодеки, Женпрофиле
- женпрофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710079"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="b7568-108">Настройка произвольных типов потоков</span><span class="sxs-lookup"><span data-stu-id="b7568-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="b7568-109">Для большинства произвольных типов потоков требуется только скорость потока, окно буфера и соответствующий основной тип носителя в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b7568-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="b7568-110">Однако для некоторых произвольных типов требуется дополнительная настройка.</span><span class="sxs-lookup"><span data-stu-id="b7568-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="b7568-111">Если при настройке потока возникли проблемы, см. пример приложения с именем Женпрофиле, которое входит в состав этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="b7568-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="b7568-112">Библиотека, определенная в Женпрофиле, содержит код для включения всех типов потоков.</span><span class="sxs-lookup"><span data-stu-id="b7568-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="b7568-113">Дополнительные сведения о Женпрофиле и других примерах см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b7568-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="b7568-114">В следующих разделах описывается настройка произвольных типов потоков.</span><span class="sxs-lookup"><span data-stu-id="b7568-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="b7568-115">Section</span><span class="sxs-lookup"><span data-stu-id="b7568-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="b7568-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b7568-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7568-117">Настройка потоков скриптов</span><span class="sxs-lookup"><span data-stu-id="b7568-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="b7568-118">Описывает настройку потоков скриптов.</span><span class="sxs-lookup"><span data-stu-id="b7568-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="b7568-119">Настройка потоков обмена файлами</span><span class="sxs-lookup"><span data-stu-id="b7568-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="b7568-120">Описывает настройку потоков обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="b7568-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="b7568-121">Настройка веб-потоков</span><span class="sxs-lookup"><span data-stu-id="b7568-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="b7568-122">Описывает настройку веб-потоков.</span><span class="sxs-lookup"><span data-stu-id="b7568-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="b7568-123">Настройка текстовых потоков</span><span class="sxs-lookup"><span data-stu-id="b7568-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="b7568-124">Описывает настройку текстовых потоков.</span><span class="sxs-lookup"><span data-stu-id="b7568-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="b7568-125">Настройка настраиваемых произвольных потоков</span><span class="sxs-lookup"><span data-stu-id="b7568-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="b7568-126">Описывает настройку потоков для пользовательских произвольных типов потоков.</span><span class="sxs-lookup"><span data-stu-id="b7568-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="b7568-127">Вычисление скорости потока и значений окна буфера для произвольных потоков</span><span class="sxs-lookup"><span data-stu-id="b7568-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="b7568-128">Описывает, как вычислить скорость передачи и параметры окна буфера для произвольного потока.</span><span class="sxs-lookup"><span data-stu-id="b7568-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b7568-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b7568-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7568-130">**Произвольные потоки**</span><span class="sxs-lookup"><span data-stu-id="b7568-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="b7568-131">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="b7568-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




