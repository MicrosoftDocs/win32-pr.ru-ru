---
description: Сведения об управлении скоростью
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Сведения об управлении скоростью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701470"
---
# <a name="about-rate-control"></a><span data-ttu-id="0f851-103">Сведения об управлении скоростью</span><span class="sxs-lookup"><span data-stu-id="0f851-103">About Rate Control</span></span>

<span data-ttu-id="0f851-104">В Media Foundation *скорость воспроизведения* выражается как отношение текущей скорости воспроизведения к нормальному темпу воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0f851-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="0f851-105">Например, частота 2,0 равна удвоенной нормальной скорости, а 0,5 — половина обычной скорости.</span><span class="sxs-lookup"><span data-stu-id="0f851-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="0f851-106">Отрицательные значения указывают на обратную воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="0f851-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="0f851-107">Скорость воспроизведения, равное-2,0, воспроизводится назад через поток в два раза подряд.</span><span class="sxs-lookup"><span data-stu-id="0f851-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="0f851-108">Нулевая скорость приводит к отображению одного кадра; После этого часы представления не изменяются.</span><span class="sxs-lookup"><span data-stu-id="0f851-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="0f851-109">Чтобы получить другой кадр с нулевой скоростью, приложение должно перейти к новой позиции.</span><span class="sxs-lookup"><span data-stu-id="0f851-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="0f851-110">Приложения используют следующие интерфейсы для управления скоростью воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0f851-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="0f851-111">[**Имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="0f851-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="0f851-112">Используется для определения наиболее быстрых и наиболее медленных доступных скоростей воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0f851-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="0f851-113">[**Имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="0f851-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="0f851-114">Используется для изменения скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0f851-114">Used to change the playback rate.</span></span>

<span data-ttu-id="0f851-115">Чтобы получить эти два интерфейса, вызовите [**имфжетсервице:: Get Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0f851-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="0f851-116">Идентификатор службы — \_ \_ Служба управления скоростью MF \_ .</span><span class="sxs-lookup"><span data-stu-id="0f851-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="0f851-117">С помощью службы управления скоростью приложение может реализовать быстрое пересылку и обратную воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="0f851-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="0f851-118">Тонкая</span><span class="sxs-lookup"><span data-stu-id="0f851-118">Thinning</span></span>

<span data-ttu-id="0f851-119">*Тонкая* — это любой процесс, который сокращает количество выборок в потоке, чтобы сократить общую скорость потока.</span><span class="sxs-lookup"><span data-stu-id="0f851-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="0f851-120">Для видео тонкое, как правило, выполняется путем удаления Дельта-кадров и доставки только ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="0f851-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="0f851-121">Зачастую конвейер может поддерживать более быстрые скорости воспроизведения с помощью тонкого воспроизведения, так как скорость передачи данных ниже, поскольку разностные кадры не декодированы.</span><span class="sxs-lookup"><span data-stu-id="0f851-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="0f851-122">Тонкое изменение не изменяет отметки времени и длительность выборки.</span><span class="sxs-lookup"><span data-stu-id="0f851-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="0f851-123">Например, если номинальная частота видеопотока составляет 25 кадров в секунду, то длительность каждого кадра по-прежнему будет отмечена как 40 миллисекунда, даже если источник мультимедиа удаляет все разностные кадры.</span><span class="sxs-lookup"><span data-stu-id="0f851-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="0f851-124">Это означает, что между концом одного кадра и началом следующего произойдет промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="0f851-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="0f851-125">Проведение</span><span class="sxs-lookup"><span data-stu-id="0f851-125">Scrubbing</span></span>

<span data-ttu-id="0f851-126">*Очистка* — это процесс мгновенного поиска в конкретных точках в потоке путем взаимодействия с полосой прокрутки, временной шкалой или другим визуальным представлением времени.</span><span class="sxs-lookup"><span data-stu-id="0f851-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="0f851-127">Термин поступает от эры лучшие-лучшиеных проигрывателей, когда для перехода на лучшие назад и вперед по поиску раздела требуется очистка головки воспроизведения на ленте.</span><span class="sxs-lookup"><span data-stu-id="0f851-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="0f851-128">Очистка реализуется в Media Foundation, устанавливая скорость воспроизведения равным нулю.</span><span class="sxs-lookup"><span data-stu-id="0f851-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="0f851-129">Дополнительные сведения см. [в разделе как выполнить очистку](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="0f851-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f851-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0f851-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f851-131">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="0f851-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="0f851-132">Поиск, быстрая переадресация и обратная игра</span><span class="sxs-lookup"><span data-stu-id="0f851-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="0f851-133">Интерфейсы службы</span><span class="sxs-lookup"><span data-stu-id="0f851-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



