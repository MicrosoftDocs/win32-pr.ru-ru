---
description: Установка скорости воспроизведения в сеансе мультимедиа
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Установка скорости воспроизведения в сеансе мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820181"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="de6d9-103">Установка скорости воспроизведения в сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="de6d9-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="de6d9-104">Для реализации таких функций воспроизведения, как быстрая переадресация и перемотка назад, приложениям может потребоваться изменить скорость воспроизведения потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="de6d9-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="de6d9-105">Media Foundation предоставляет службу контроля скорости, которую приложения должны использовать для динамического задания скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="de6d9-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="de6d9-106">Перед установкой скорости воспроизведения приложение должно проверить, поддерживается ли скорость источником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="de6d9-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="de6d9-107">Сведения о запросах поддерживаемых тарифов см. [в разделе Определение поддерживаемых тарифов](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="de6d9-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="de6d9-108">Сведения о тарифах на воспроизведение см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="de6d9-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="de6d9-109">Установка скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="de6d9-109">To set the playback rate</span></span>

1.  <span data-ttu-id="de6d9-110">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить объект управления скоростью из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="de6d9-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="de6d9-111">Приложения, вызывающие [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , должны обеспечить следующее:</span><span class="sxs-lookup"><span data-stu-id="de6d9-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="de6d9-112">Параметр *объект punkObject* содержит инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="de6d9-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="de6d9-113">Объект управления скоростью, полученный в параметре *ппвобжект* , освобождается, чтобы избежать утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="de6d9-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="de6d9-114">Вызовите метод [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) , чтобы задать скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="de6d9-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="de6d9-115">После асинхронного завершения **сетрате** приложение получает событие [месессионратечанжед](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="de6d9-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="de6d9-116">Пример</span><span class="sxs-lookup"><span data-stu-id="de6d9-116">Example</span></span>

<span data-ttu-id="de6d9-117">В следующем коде показано, как задать скорость воспроизведения, вызвав метод [**сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .</span><span class="sxs-lookup"><span data-stu-id="de6d9-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



<span data-ttu-id="de6d9-118">Приложение должно быть остановлено или приостановлено, прежде чем оно сможет выполнить переход с отрицательной или нулевой ставки на положительный коэффициент.</span><span class="sxs-lookup"><span data-stu-id="de6d9-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="de6d9-119">Сведения об этих состояниях см. [в разделе Управление состояниями представления](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="de6d9-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de6d9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="de6d9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de6d9-121">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="de6d9-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="de6d9-122">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="de6d9-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="de6d9-123">Поиск, быстрая переадресация и обратная игра</span><span class="sxs-lookup"><span data-stu-id="de6d9-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



