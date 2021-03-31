---
description: Определение поддерживаемых ставок
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Определение поддерживаемых ставок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263443"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="6b387-103">Определение поддерживаемых ставок</span><span class="sxs-lookup"><span data-stu-id="6b387-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="6b387-104">Прежде чем изменять скорость воспроизведения, приложение должно проверить, поддерживается ли скорость воспроизведения объектами в конвейере.</span><span class="sxs-lookup"><span data-stu-id="6b387-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="6b387-105">Интерфейс [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) предоставляет методы для получения максимальной скорости прямого и обратного тарифа, поддерживаемой частоты, ближайшей к запрошенной ставке, и самой медленной скорости.</span><span class="sxs-lookup"><span data-stu-id="6b387-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="6b387-106">Каждый из этих запросов скорости может задавать направление воспроизведения и необходимость использования тонкого.</span><span class="sxs-lookup"><span data-stu-id="6b387-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="6b387-107">Точный уровень воспроизведения запрашивается с помощью интерфейса [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .</span><span class="sxs-lookup"><span data-stu-id="6b387-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="6b387-108">Сведения об изменении скорости воспроизведения см. в разделе [Установка скорости воспроизведения для сеанса мультимедиа](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="6b387-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="6b387-109">Общие сведения о скорости воспроизведения см. в разделе [сведения об управлении скоростью](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="6b387-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="6b387-110">Определение текущей скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="6b387-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="6b387-111">Получение службы управления скоростью из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b387-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="6b387-112">Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="6b387-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="6b387-113">Приложение должно запросить службу управления скоростью через сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b387-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="6b387-114">На внутреннем уровне сеанс мультимедиа запрашивает объекты в топологии.</span><span class="sxs-lookup"><span data-stu-id="6b387-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="6b387-115">Вызовите метод [**имфратеконтрол:: Rate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) , чтобы получить текущую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6b387-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="6b387-116">Параметр *пфсин* параметра [**Rate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) получает **логическое** значение, указывающее, является ли поток в данный момент тонким.</span><span class="sxs-lookup"><span data-stu-id="6b387-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="6b387-117">Приложение должно передать **значение NULL** , если не нужно запрашивать тонкую поддержку потока.</span><span class="sxs-lookup"><span data-stu-id="6b387-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="6b387-118">Параметр *пфлрате* получает текущую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6b387-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="6b387-119">Определение ближайшей поддерживаемой частоты</span><span class="sxs-lookup"><span data-stu-id="6b387-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="6b387-120">Получите службу поддержки по скорости из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b387-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="6b387-121">Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="6b387-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="6b387-122">Вызовите метод [**имфратесуппорт:: исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) , чтобы получить поддерживаемую частоту, ближайшую к запрошенному темпу воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6b387-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="6b387-123">В примере запрашивается, поддерживается ли скорость воспроизведения 4,0 с тонкой.</span><span class="sxs-lookup"><span data-stu-id="6b387-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="6b387-124">Это указывается путем передачи значения **true** в параметре *ФСИН* объекта [**исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span><span class="sxs-lookup"><span data-stu-id="6b387-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="6b387-125">Если эта скорость поддерживается, *актуалрате* содержит частоту воспроизведения 4,0, и вызов будет выполнен успешно с возвращаемым значением S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6b387-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="6b387-126">Если точный коэффициент воспроизведения не поддерживается, в *актуалрате* получается Ближайшая поддерживаемая ставка.</span><span class="sxs-lookup"><span data-stu-id="6b387-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="6b387-127">Если скорость не поддерживается и нет доступной ближайшей скорости воспроизведения, вызов возвращает соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6b387-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="6b387-128">Эти значения могут изменяться в зависимости от того, какие компоненты конвейера загружены.</span><span class="sxs-lookup"><span data-stu-id="6b387-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="6b387-129">Поэтому при загрузке нового топололги необходимо повторно запрашивать значения.</span><span class="sxs-lookup"><span data-stu-id="6b387-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="6b387-130">Если желаемая скорость воспроизведения не поддерживается, можно запросить каждый объект в топологии по отдельности, чтобы определить, не поддерживает ли конкретный компонент скорость.</span><span class="sxs-lookup"><span data-stu-id="6b387-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="6b387-131">Вы можете перестроить топологию без этого компонента, а затем воспроизвести ее с желаемой скоростью.</span><span class="sxs-lookup"><span data-stu-id="6b387-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="6b387-132">Например, если каждый компонент, за исключением модуля подготовки звука, поддерживает заданную скорость, можно перестроить топологию без звуковой ветви и воспроизвести желаемую скорость без звука.</span><span class="sxs-lookup"><span data-stu-id="6b387-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="6b387-133">Определение самой медленной поддерживаемой скорости</span><span class="sxs-lookup"><span data-stu-id="6b387-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="6b387-134">Получите службу поддержки по скорости из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6b387-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="6b387-135">Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="6b387-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="6b387-136">Вызовите метод [**имфратесуппорт:: жетсловестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) , чтобы получить наиболее медленную поддерживаемую частоту.</span><span class="sxs-lookup"><span data-stu-id="6b387-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="6b387-137">В примере запрашиваются самые медленные обратные скорости воспроизведения с тонкой.</span><span class="sxs-lookup"><span data-stu-id="6b387-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="6b387-138">Нижняя граница получается в параметре *словестрате* объекта [**жетсловестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span><span class="sxs-lookup"><span data-stu-id="6b387-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="6b387-139">Если обратная или тонкое воспроизведение не поддерживается, вызов возвращает соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6b387-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b387-140">См. также</span><span class="sxs-lookup"><span data-stu-id="6b387-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b387-141">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="6b387-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="6b387-142">Управление скоростью</span><span class="sxs-lookup"><span data-stu-id="6b387-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="6b387-143">Поиск, быстрая переадресация и обратная игра</span><span class="sxs-lookup"><span data-stu-id="6b387-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



