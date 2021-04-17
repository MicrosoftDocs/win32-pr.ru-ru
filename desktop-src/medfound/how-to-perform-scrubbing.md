---
description: Как выполнить очистку
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Как выполнить очистку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543607"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="7d2da-103">Как выполнить очистку</span><span class="sxs-lookup"><span data-stu-id="7d2da-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="7d2da-104">Очистка выполняется для мгновенного поиска конкретных точек в файле путем взаимодействия с визуальным представлением времени, например с помощью полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7d2da-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="7d2da-105">В Media Foundation очистка означает поиск в файле и получение одного обновленного кадра.</span><span class="sxs-lookup"><span data-stu-id="7d2da-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="7d2da-106">Дополнительные сведения об очистке см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="7d2da-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="7d2da-107">Выполнение очистки</span><span class="sxs-lookup"><span data-stu-id="7d2da-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="7d2da-108">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить интерфейс [**Имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из [сеанса мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="7d2da-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="7d2da-109">Не получает интерфейс [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7d2da-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="7d2da-110">Всегда получите интерфейс из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7d2da-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="7d2da-111">Вызовите [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) , чтобы установить скорость воспроизведения равным нулю.</span><span class="sxs-lookup"><span data-stu-id="7d2da-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="7d2da-112">Дополнительные сведения о вызове этого метода см. в разделе [Установка скорости воспроизведения в сеансе мультимедиа](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="7d2da-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="7d2da-113">Создайте положение поиска в **пропвариант** , указав время презентации для поиска в типе **мфтиме** .</span><span class="sxs-lookup"><span data-stu-id="7d2da-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="7d2da-114">Вызовите [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) с позицией поиска, чтобы начать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="7d2da-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="7d2da-115">После завершения операции очистки сеанс мультимедиа отправляет событие [месессионскрубсамплекомплете](mesessionscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="7d2da-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="7d2da-116">Дождитесь этого события перед повторным вызовом [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) для другой операции очистки.</span><span class="sxs-lookup"><span data-stu-id="7d2da-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="7d2da-117">Пример</span><span class="sxs-lookup"><span data-stu-id="7d2da-117">Example</span></span>

<span data-ttu-id="7d2da-118">В следующем примере кода показано, как выполнить очистку.</span><span class="sxs-lookup"><span data-stu-id="7d2da-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="7d2da-119">Успешная операция очистки создает событие [месессионскрубсамплекомплете](mesessionscrubsamplecomplete.md) после того, как все приемники потока обновляются новым кадром, а операция очистки завершается успешно.</span><span class="sxs-lookup"><span data-stu-id="7d2da-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="7d2da-120">При очистке видеофайла отображается кадр, который был выполнен, но не создает звуковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="7d2da-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="7d2da-121">Приложение может выполнять пошаговое выполнение кадра, устанавливая скорость воспроизведения равным нулю, а затем передавая **пропвариант** , для которого задано значение **VT \_ Empty** , в вызове [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="7d2da-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d2da-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7d2da-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d2da-123">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7d2da-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="7d2da-124">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="7d2da-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



