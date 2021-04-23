---
description: Управление состояниями представления
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Управление состояниями представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692568"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="13b4d-103">Управление состояниями представления</span><span class="sxs-lookup"><span data-stu-id="13b4d-103">How to Control Presentation States</span></span>

<span data-ttu-id="13b4d-104">Сеанс мультимедиа обеспечивает управление транспортом, например изменение состояния презентации (воспроизведение, пауза и остановка в сценарии воспроизведения в стиле списка воспроизведения).</span><span class="sxs-lookup"><span data-stu-id="13b4d-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="13b4d-105">В этом разделе описываются методы сеансов мультимедиа, которые должны вызываться приложением для изменения состояния воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="13b4d-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="13b4d-106">В следующей таблице показаны допустимые переходы состояния представления.</span><span class="sxs-lookup"><span data-stu-id="13b4d-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="13b4d-107">Смена состояния</span><span class="sxs-lookup"><span data-stu-id="13b4d-107">State transition</span></span> | <span data-ttu-id="13b4d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="13b4d-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b4d-109">Воспроизведение-> пауза</span><span class="sxs-lookup"><span data-stu-id="13b4d-109">Play -> Pause</span></span> | <span data-ttu-id="13b4d-110">Время презентации зависает.</span><span class="sxs-lookup"><span data-stu-id="13b4d-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="13b4d-111">Воспроизведение — ></span><span class="sxs-lookup"><span data-stu-id="13b4d-111">Play -> Stop</span></span>  | <span data-ttu-id="13b4d-112">Часы презентации сброшены.</span><span class="sxs-lookup"><span data-stu-id="13b4d-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="13b4d-113">Пауза > Play</span><span class="sxs-lookup"><span data-stu-id="13b4d-113">Pause -> Play</span></span> | <span data-ttu-id="13b4d-114">Часы презентации возобновляются со времени, Фрозе во время воспроизведения, чтобы приостановить переход.</span><span class="sxs-lookup"><span data-stu-id="13b4d-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="13b4d-115">Пауза-> остановить</span><span class="sxs-lookup"><span data-stu-id="13b4d-115">Pause -> Stop</span></span> | <span data-ttu-id="13b4d-116">Часы презентации сброшены.</span><span class="sxs-lookup"><span data-stu-id="13b4d-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="13b4d-117">> воспроизведение</span><span class="sxs-lookup"><span data-stu-id="13b4d-117">Stop -> Play</span></span>  | <span data-ttu-id="13b4d-118">Часы презентации начинаются с начала презентации.</span><span class="sxs-lookup"><span data-stu-id="13b4d-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="13b4d-119">Остановка-> приостановка</span><span class="sxs-lookup"><span data-stu-id="13b4d-119">Stop -> Pause</span></span> | <span data-ttu-id="13b4d-120">Не допускается.</span><span class="sxs-lookup"><span data-stu-id="13b4d-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="13b4d-121">Изменение состояния представления</span><span class="sxs-lookup"><span data-stu-id="13b4d-121">To change presentation states</span></span>

-   <span data-ttu-id="13b4d-122">Вызовите метод [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) , чтобы приостановить воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="13b4d-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="13b4d-123">Перед вызовом этого метода приложение должно вызвать метод [**имфмедиасессион:: жетсессионкапабилитиес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) , чтобы определить, поддерживает ли источник мультимедиа состояние паузы.</span><span class="sxs-lookup"><span data-stu-id="13b4d-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="13b4d-124">Если это так, этот метод возвращает **мфсессионкап \_ Pause** в параметре *пдвкапс* .</span><span class="sxs-lookup"><span data-stu-id="13b4d-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="13b4d-125">Pause временно останавливает сеанс мультимедиа, часы презентации и приемник потока для текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="13b4d-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="13b4d-126">После успешного завершения вызова приложение получает событие [месессионпаусед](mesessionpaused.md) .</span><span class="sxs-lookup"><span data-stu-id="13b4d-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="13b4d-127">Вызовите метод [**имфмедиасессион:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) , чтобы прерывать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="13b4d-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="13b4d-128">Этот метод останавливает сеанс мультимедиа, останавливая источник мультимедиа, соответствующие часы и приемники потоков.</span><span class="sxs-lookup"><span data-stu-id="13b4d-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="13b4d-129">Если сеанс мультимедиа управляет [источником Sequencer](sequencer-source.md), базовые машинные источники останавливаются источником Sequencer.</span><span class="sxs-lookup"><span data-stu-id="13b4d-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="13b4d-130">После остановки сеанса мультимедиа приложение получает событие [месессионстоппед](mesessionstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="13b4d-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="13b4d-131">Вызовите метод [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , чтобы начать воспроизведение или найти новую точку.</span><span class="sxs-lookup"><span data-stu-id="13b4d-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="13b4d-132">Этот метод запускает сеанс мультимедиа из состояний паузы и остановки.</span><span class="sxs-lookup"><span data-stu-id="13b4d-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="13b4d-133">Сеанс мультимедиа отвечает за настройку потока данных в конвейере.</span><span class="sxs-lookup"><span data-stu-id="13b4d-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="13b4d-134">Этот метод указывает сеансу мультимедиа запустить часы презентации.</span><span class="sxs-lookup"><span data-stu-id="13b4d-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="13b4d-135">После этого вызова сеанс мультимедиа отправляет приложению событие [месессионстартед](mesessionstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="13b4d-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13b4d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="13b4d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13b4d-137">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="13b4d-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



