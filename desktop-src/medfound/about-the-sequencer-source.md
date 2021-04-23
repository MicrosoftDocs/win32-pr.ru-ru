---
description: Сведения о источнике Sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Сведения о источнике Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542175"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="c21ea-103">Сведения о источнике Sequencer</span><span class="sxs-lookup"><span data-stu-id="c21ea-103">About the Sequencer Source</span></span>

<span data-ttu-id="c21ea-104">Источник Sequencer позволяет приложению последовательно воспроизводить коллекцию [источников мультимедиа](media-sources.md) с плавным переходом между источниками.</span><span class="sxs-lookup"><span data-stu-id="c21ea-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="c21ea-105">Источник Sequencer можно использовать в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="c21ea-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="c21ea-106">Создание списка воспроизведения, который легко переключается с одного источника мультимедиа на следующий.</span><span class="sxs-lookup"><span data-stu-id="c21ea-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="c21ea-107">Воспроизводить потоки из нескольких источников одновременно; Например, воспроизведение звука из одного файла с видео из другого.</span><span class="sxs-lookup"><span data-stu-id="c21ea-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="c21ea-108">Переключение между потоками в разных источниках мультимедиа в последовательных записях списка воспроизведения; Например, список воспроизведения может содержать записи с одинаковым источником видео, в то время как каждая запись содержит другой источник звука.</span><span class="sxs-lookup"><span data-stu-id="c21ea-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="c21ea-109">Для каждого элемента списка воспроизведения приложение создает отдельную топологию.</span><span class="sxs-lookup"><span data-stu-id="c21ea-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="c21ea-110">Источники мультимедиа в этих топологиях называются *собственными источниками*, чтобы отличать их от источника Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c21ea-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="c21ea-111">Во время воспроизведения вся последовательность топологий называется *представлением*, а Каждая топология в последовательности называется *сегментом*.</span><span class="sxs-lookup"><span data-stu-id="c21ea-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="c21ea-112">Воспроизведение управляется [сеансом мультимедиа](media-session.md), который предоставляет элементы управления транспорта, такие как воспроизведение, пауза и остановка.</span><span class="sxs-lookup"><span data-stu-id="c21ea-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="c21ea-113">Сеанс мультимедиа также управляет временем презентации и отправляет события в приложение.</span><span class="sxs-lookup"><span data-stu-id="c21ea-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="c21ea-114">(События из источника Sequencer перенаправляются в приложение через сеанс мультимедиа.)</span><span class="sxs-lookup"><span data-stu-id="c21ea-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="c21ea-115">Чтобы создать список воспроизведения, приложение создает одну или несколько топологий воспроизведения и помещает их в очередь источника Sequencer в нужном порядке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c21ea-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="c21ea-116">На внутреннем уровне источник Sequencer изменяет топологии таким образом, чтобы исходные узлы указывали на источник Sequencer, а не на собственный источник.</span><span class="sxs-lookup"><span data-stu-id="c21ea-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="c21ea-117">Приложение отправляет эти измененные топологии, а не исходные топологии, в сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c21ea-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="c21ea-118">Это позволяет источнику Sequencer объединять собственные источники и обмениваться данными с сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c21ea-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="c21ea-119">Чтобы обеспечить плавный переход между сегментами, источник Sequencer выполняет предочередную выработку каждого сегмента.</span><span class="sxs-lookup"><span data-stu-id="c21ea-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="c21ea-120">Хотя один сегмент воспроизводится и до начала воспроизведения следующего сегмента, источник Sequencer запускает событие [меневпресентатион](menewpresentation.md) , которое содержит дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="c21ea-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="c21ea-121">Приложение использует этот дескриптор презентации для получения топологии следующего сегмента в презентации и помещает топологию в очередь сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c21ea-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="c21ea-122">На следующем рисунке показан поток данных для записей списка воспроизведения через источник Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c21ea-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="c21ea-123">Приложение использует сопоставитель источников для создания собственных источников, создает топологии для каждого сегмента и помещает в очередь топологии в источнике Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c21ea-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![Схема, показывающая поток данных из сегментов имфмедиасессион, имфсекуенцерсаурце и списка воспроизведения, ведущих к имфмедиасаурце](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="c21ea-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c21ea-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c21ea-126">Создание списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c21ea-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="c21ea-127">Топологии</span><span class="sxs-lookup"><span data-stu-id="c21ea-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="c21ea-128">Использование источника Sequencer</span><span class="sxs-lookup"><span data-stu-id="c21ea-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="c21ea-129">Источник Sequencer</span><span class="sxs-lookup"><span data-stu-id="c21ea-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



