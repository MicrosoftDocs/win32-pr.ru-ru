---
description: Режимы Run-Time MPEG-2 демультиплексирование
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Режимы Run-Time MPEG-2 демультиплексирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140463"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="cd217-103">Режимы Run-Time MPEG-2 демультиплексирование</span><span class="sxs-lookup"><span data-stu-id="cd217-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="cd217-104">[Демультиплексор MPEG-2](mpeg-2-demultiplexer.md) ("демультиплексирование") может действовать в режиме принудительной отправки или в режиме опроса.</span><span class="sxs-lookup"><span data-stu-id="cd217-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="cd217-105">В режиме принудительной отправки данные поступают из активного источника, такого как Сетевая трансляция.</span><span class="sxs-lookup"><span data-stu-id="cd217-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="cd217-106">В режиме опроса данные поступают из локального файла.</span><span class="sxs-lookup"><span data-stu-id="cd217-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="cd217-107">Режим Pull доступен в Windows XP и более поздних версиях, только для потоков программ.</span><span class="sxs-lookup"><span data-stu-id="cd217-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="cd217-108">На платформах нижнего уровня используйте фильтр [разделителя MPEG-2](mpeg-2-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="cd217-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="cd217-109">Режим принудительной отправки доступен на всех платформах как для потоков программы, так и для потоков транспорта.</span><span class="sxs-lookup"><span data-stu-id="cd217-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="cd217-110">Таким образом, демультиплексирование поддерживает три возможных режима: потоки программы в режиме Pull, потоки программы в режиме Push-уведомлений и транспортные потоки в режиме принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="cd217-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="cd217-111">Демультиплексирование определяет режим, используемый во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd217-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="cd217-112">Режим определяется при соединении входного ПИН-кода или при настройке первого выходного контакта в зависимости от того, что происходит первым:</span><span class="sxs-lookup"><span data-stu-id="cd217-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="cd217-113">При подключении входного ПИН-кода: в Windows XP и более поздних версиях демультиплексирование запрашивает вышестоящий фильтр для интерфейса [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Если вышестоящий фильтр предоставляет этот интерфейс, демультиплексирование настраивает себя для потоков программы в режиме опроса.</span><span class="sxs-lookup"><span data-stu-id="cd217-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="cd217-114">В противном случае демультиплексирование использует режим push-уведомлений, а тип мультимедиа определяет тип потока (поток программы или транспортный поток).</span><span class="sxs-lookup"><span data-stu-id="cd217-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="cd217-115">Список входных типов см. в статье [**типы носителей для демультиплексирования MPEG-2**](mpeg-2-demultiplexer-media-types.md) .</span><span class="sxs-lookup"><span data-stu-id="cd217-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="cd217-116">При настройке первого выходного ПИН-кода: Если вы создаете закрепление вывода и запрашиваете его для [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), демультиплексирование настраивает себя для потоков транспорта в режиме принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="cd217-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="cd217-117">Если вы запрашиваете ПИН-код для [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), демультиплексирование настраивает себя для потоков программ, а также в режиме принудительной отправки.</span><span class="sxs-lookup"><span data-stu-id="cd217-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="cd217-118">Все последующие запросы для другого интерфейса завершаются ошибкой, так как демультиплексирование не может работать одновременно в двух режимах.</span><span class="sxs-lookup"><span data-stu-id="cd217-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="cd217-119">После того как демультиплексирование настроен для конкретного режима, он остается в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="cd217-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="cd217-120">Чтобы использовать другой режим, необходимо создать новый экземпляр демультиплексирование.</span><span class="sxs-lookup"><span data-stu-id="cd217-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd217-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cd217-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd217-122">Использование демультиплексора MPEG-2</span><span class="sxs-lookup"><span data-stu-id="cd217-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



