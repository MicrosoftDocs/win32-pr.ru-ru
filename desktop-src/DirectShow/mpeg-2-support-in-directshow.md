---
description: Поддержка MPEG-2 в DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Поддержка MPEG-2 в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537799"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="d4b9a-103">Поддержка MPEG-2 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d4b9a-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="d4b9a-104">В этом разделе описываются компоненты, которые можно использовать для воспроизведения содержимого MPEG-2 в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="d4b9a-105">Хотя видео DVD основано на MPEG-2, в этом разделе не описывается воспроизведение DVD-дисков или Навигация.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="d4b9a-106">Сведения о DVD-дисках в DirectShow см. в разделе [DVD-приложения](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d4b9a-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="d4b9a-107">Данные MPEG-2 могут поступать из локального файла или из активного источника, например сетевого вещания или устройства D-ВХС.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="d4b9a-108">Воспроизведение файла называется *режимом опроса* , так как фильтр средства синтаксического анализа извлекает данные из файла в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="d4b9a-109">Активные источники называются *принудительным режимом* , так как фильтр источника отправляет данные в граф.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="d4b9a-110">DirectShow предоставляет два фильтра, которые могут анализировать системные потоки MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="d4b9a-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="d4b9a-111">[Демультиплексор MPEG-2](mpeg-2-demultiplexer.md) ("демультиплексирование"): Этот фильтр поддерживает режим принудительной отправки для потоков программы и потоков транспорта.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="d4b9a-112">В Windows XP и более поздних версиях он также поддерживает режим опроса для потоков программы.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="d4b9a-113">[Разделитель MPEG-2](mpeg-2-splitter.md): Этот фильтр поддерживает режим опроса для программных потоков на низкоуровневых платформах.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="d4b9a-114">Этот фильтр не рекомендуется к использованию в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="d4b9a-115">Чтобы использовать разделитель MPEG-2 демультиплексирование или MPEG-2, необходимо иметь встроенные и видеодекодеры MPEG-2, совместимые с DirectShow, которые принимают Пакетированные простые потоки (PES).</span><span class="sxs-lookup"><span data-stu-id="d4b9a-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="d4b9a-116">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="d4b9a-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d4b9a-117">Обзор систем MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4b9a-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="d4b9a-118">Использование демультиплексора MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4b9a-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="d4b9a-119">Использование разделителя MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d4b9a-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="d4b9a-120">Примеры свойств MPEG</span><span class="sxs-lookup"><span data-stu-id="d4b9a-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="d4b9a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d4b9a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b9a-122">Образец фильтра средства синтаксического анализа PSI</span><span class="sxs-lookup"><span data-stu-id="d4b9a-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



