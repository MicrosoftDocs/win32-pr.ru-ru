---
description: Поведение демультиплексирование Clock
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Поведение демультиплексирование Clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072259"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="24043-103">Поведение демультиплексирование Clock</span><span class="sxs-lookup"><span data-stu-id="24043-103">Demux Clock Behavior</span></span>

<span data-ttu-id="24043-104">В режиме принудительной отправки MPEG-2 демультиплексора (демультиплексирование) предоставляет интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="24043-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="24043-105">Он выступает в качестве активного источника, поэтому он будет выбран по умолчанию в качестве таймера ссылок на граф; Дополнительные сведения см. в разделе [Live Sources](live-sources.md) .</span><span class="sxs-lookup"><span data-stu-id="24043-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="24043-106">Для транспортных потоков демультиплексирование синхронизирует свои часы с потоком PCR, который соответствует потоку аудио или видео, который в последнее время сопоставлен с приложением.</span><span class="sxs-lookup"><span data-stu-id="24043-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="24043-107">На внутреннем уровне демультиплексирование отслеживает таблицы PAT и ПЛТ.</span><span class="sxs-lookup"><span data-stu-id="24043-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="24043-108">Когда приложение сопоставляет идентификатор процесса простейшего потока с выходным закреплением, демультиплексирование ищет поток PCR для этого PID и использует этот поток PCR.</span><span class="sxs-lookup"><span data-stu-id="24043-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="24043-109">(В настоящее время не существует способа, которым приложение может явно указать идентификатор PCR.)</span><span class="sxs-lookup"><span data-stu-id="24043-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="24043-110">Для потоков программы демультиплексирование синхронизирует свои часы с потоком SCR.</span><span class="sxs-lookup"><span data-stu-id="24043-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="24043-111">Синхронизация часов фильтра в поток PCR или SCR предотвращает переполнение данных или потерю точности, что может произойти, если часы графа изменяются из потоковых часов.</span><span class="sxs-lookup"><span data-stu-id="24043-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="24043-112">Демультиплексирование также преобразует PES PTS значений в время ссылок DirectShow и использует эти значения для отметки времени выборки мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="24043-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="24043-113">Отметки времени применяются к следующей границе кадра; нет никакой гарантии, что граница кадра будет согласована с началом примера носителя.</span><span class="sxs-lookup"><span data-stu-id="24043-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="24043-114">Демультиплексирование гарантирует, что отметки времени увеличиваются монотонно.</span><span class="sxs-lookup"><span data-stu-id="24043-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="24043-115">Это означает, например, что если транспортный поток включает в себя сегмент, например коммерческий, который был создан с часами, отличным от часов основной программы, демультиплексирование настроит метки времени презентации, чтобы скрыть время отключения от нисходящих фильтров.</span><span class="sxs-lookup"><span data-stu-id="24043-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24043-116">См. также</span><span class="sxs-lookup"><span data-stu-id="24043-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24043-117">Использование демультиплексора MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24043-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



