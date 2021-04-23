---
description: Конфигурация графа фильтра DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Конфигурация графа фильтра DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537955"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="16ee7-103">Конфигурация графа фильтра DVD</span><span class="sxs-lookup"><span data-stu-id="16ee7-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="16ee7-104">В этом разделе описаны различные конфигурации графов фильтров для воспроизведения DVD-дисков в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="16ee7-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="16ee7-105">Эти схемы предоставляются главным образом для справки.</span><span class="sxs-lookup"><span data-stu-id="16ee7-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="16ee7-106">Навигатор DVD строит граф, поэтому в целом нет необходимости понимать, как настроен график.</span><span class="sxs-lookup"><span data-stu-id="16ee7-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="16ee7-107">Дополнительные сведения см. [в разделе Создание диаграммы фильтра DVD](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="16ee7-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="16ee7-108">На следующем рисунке показан граф фильтра DVD с программным декодером.</span><span class="sxs-lookup"><span data-stu-id="16ee7-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![граф фильтра DVD для Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="16ee7-110">При наличии аппаратного декодера он обычно подключается непосредственно к видеоадаптеру через порт видео.</span><span class="sxs-lookup"><span data-stu-id="16ee7-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="16ee7-111">Это позволяет отправлять декодированные видеозаписи непосредственно в буфер кадров на графической карте без передачи в память узла.</span><span class="sxs-lookup"><span data-stu-id="16ee7-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="16ee7-112">Чтобы управлять этим прямым подключением в более ранних версиях Windows, DirectShow поддерживает расширения видеопортов DirectDraw (впе) через интерфейс в [фильтре микшера наложения](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="16ee7-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="16ee7-113">Микшер наложения теперь устарел.</span><span class="sxs-lookup"><span data-stu-id="16ee7-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="16ee7-114">В Windows XP и более поздних версиях аппаратный декодер может подключаться к фильтру [диспетчера видеопортов](video-port-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="16ee7-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![DVD-график для Windows XP с аппаратным декодером](images/dvd-hwgraph-xp.png)

<span data-ttu-id="16ee7-116">На всех этих диаграммах в качестве исходного фильтра используется Навигатор DVD. Он выполняет несколько задач:</span><span class="sxs-lookup"><span data-stu-id="16ee7-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="16ee7-117">Считывает данные о переходах и видео с диска.</span><span class="sxs-lookup"><span data-stu-id="16ee7-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="16ee7-118">Демультиплексирование данных видео, аудио и субтитров в отдельные потоки.</span><span class="sxs-lookup"><span data-stu-id="16ee7-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="16ee7-119">Переносит потоки в граф для дальнейшей обработки и отрисовки в конечном итоге.</span><span class="sxs-lookup"><span data-stu-id="16ee7-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="16ee7-120">Информирует ваше приложение о событиях, связанных с DVD.</span><span class="sxs-lookup"><span data-stu-id="16ee7-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="16ee7-121">В потоке воспроизведения DVD-навигатор подключается к аудио декодеру, который подключается к [фильтру модуля DirectSound](directsound-renderer-filter.md), используемому по умолчанию модулем подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="16ee7-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="16ee7-122">В потоках видео и субтитров нисходящие фильтры — это видеодекодер стороннего производителя, а также модуль подготовки видео для микширования (или [микшер наложения](overlay-mixer-filter.md), а также средство [просмотра видео](video-renderer-filter.md) в низкоуровневых приложениях).</span><span class="sxs-lookup"><span data-stu-id="16ee7-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="16ee7-123">Если приложение будет работать с закрытыми подписанными данными, то на диаграмму необходимо добавить фильтр DirectShow Line 21 декодер 2.</span><span class="sxs-lookup"><span data-stu-id="16ee7-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="16ee7-124">Это подразумевает один вызов метода. фильтр будет подключен автоматически.</span><span class="sxs-lookup"><span data-stu-id="16ee7-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="16ee7-125">Приложение взаимодействует с и управляет навигатором DVD через настраиваемые интерфейсы, предоставляемые навигатором DVD: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)— методы "Set" — и [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)— методы "Get".</span><span class="sxs-lookup"><span data-stu-id="16ee7-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="16ee7-126">Он также должен взаимодействовать с диспетчером графа фильтров (через [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol)), чтобы останавливаться, запускать и иным образом управлять графом.</span><span class="sxs-lookup"><span data-stu-id="16ee7-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="16ee7-127">Кроме того, может потребоваться управлять другими отдельными фильтрами, например фильтром микшера наложения для переключения между оконным и полноэкранным экраном.</span><span class="sxs-lookup"><span data-stu-id="16ee7-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="16ee7-128">Дополнительные сведения см. в разделе [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="16ee7-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="16ee7-129">Точная конфигурация диаграммы зависит от типа установленного декодера MPEG-2, требуется ли работа с данными, закрытыми с субтитрами 21, и другими факторами.</span><span class="sxs-lookup"><span data-stu-id="16ee7-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16ee7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="16ee7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16ee7-131">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="16ee7-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



