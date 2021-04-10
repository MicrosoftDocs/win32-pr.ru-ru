---
description: Сведения о сеансе мультимедиа
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Сведения о сеансе мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999854"
---
# <a name="about-the-media-session"></a><span data-ttu-id="15488-103">Сведения о сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="15488-103">About the Media Session</span></span>

<span data-ttu-id="15488-104">Сеанс мультимедиа предоставляет интерфейс [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="15488-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="15488-105">Существует два способа создания сеанса мультимедиа в зависимости от того, будет ли приложение поддерживать защищенное содержимое:</span><span class="sxs-lookup"><span data-stu-id="15488-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="15488-106">Если приложение не поддерживает защищенное содержимое, можно создать сеанс мультимедиа, вызвав метод [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span><span class="sxs-lookup"><span data-stu-id="15488-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="15488-107">Эта функция создает сеанс мультимедиа внутри процесса приложения.</span><span class="sxs-lookup"><span data-stu-id="15488-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="15488-108">Для поддержки защищенного содержимого создайте сеанс мультимедиа, вызвав [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="15488-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="15488-109">Эта функция создает сеанс мультимедиа внутри процесса защищенного пути к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="15488-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="15488-110">Приложение получает указатель на прокси-объект, который маршалирует вызовы метода через границу процесса.</span><span class="sxs-lookup"><span data-stu-id="15488-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="15488-111">Обратите внимание, что сеанс PMP Media можно использовать для воспроизведения незашифрованного содержимого, а также защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="15488-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="15488-112">Любое приложение, использующее сеанс мультимедиа, будет выполнять следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="15488-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="15488-113">Создайте топологию.</span><span class="sxs-lookup"><span data-stu-id="15488-113">Create a topology.</span></span>
2.  <span data-ttu-id="15488-114">Постановка топологии в очередь в сеансе мультимедиа путем вызова [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="15488-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="15488-115">Управление потоком данных путем вызова [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)или [**имфмедиасессион:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="15488-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="15488-116">Перед выходом из приложения вызовите метод [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) , чтобы закрыть сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="15488-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="15488-117">Завершите работу всех источников мультимедиа, созданных приложением, вызвав [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="15488-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="15488-118">Завершите сеанс мультимедиа, вызвав [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="15488-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="15488-119">При использовании сеанса мультимедиа приложение не должно запускать, приостанавливать или останавливать источник мультимедиа напрямую.</span><span class="sxs-lookup"><span data-stu-id="15488-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="15488-120">Все изменения состояния должны быть инициированы вызовом методов [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="15488-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="15488-121">Изменения состояния в источнике мультимедиа обрабатываются сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="15488-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="15488-122">Многие другие сведения будут зависеть от конкретных функциональных возможностей приложения.</span><span class="sxs-lookup"><span data-stu-id="15488-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="15488-123">Защищенное содержимое</span><span class="sxs-lookup"><span data-stu-id="15488-123">Protected Content</span></span>

<span data-ttu-id="15488-124">Чтобы воспроизвести защищенное содержимое, необходимо создать сеанс мультимедиа внутри защищенного пути к носителю (PMP), вызвав [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="15488-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="15488-125">Эта функция создает экземпляр сеанса мультимедиа внутри PMP и возвращает указатель на прокси-объект, который маршалирует интерфейсы через границу процесса.</span><span class="sxs-lookup"><span data-stu-id="15488-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="15488-126">В большинстве случаев использование сеанса мультимедиа в PMP является прозрачным для приложения.</span><span class="sxs-lookup"><span data-stu-id="15488-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="15488-127">Однако приложению может потребоваться вызвать определенные действия, которые позволят пользователю воспроизвести содержимое.</span><span class="sxs-lookup"><span data-stu-id="15488-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="15488-128">Например, пользователю может потребоваться получить лицензию DRM.</span><span class="sxs-lookup"><span data-stu-id="15488-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="15488-129">Media Foundation определяет универсальный механизм для этих действий с помощью интерфейса [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="15488-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="15488-130">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="15488-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="15488-131">Путь к защищенному носителю</span><span class="sxs-lookup"><span data-stu-id="15488-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="15488-132">Воспроизведение защищенных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="15488-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="15488-133">Часы представления</span><span class="sxs-lookup"><span data-stu-id="15488-133">Presentation Clock</span></span>

<span data-ttu-id="15488-134">Сеанс мультимедиа управляет всеми аспектами часов представления.</span><span class="sxs-lookup"><span data-stu-id="15488-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="15488-135">Создание часов представления.</span><span class="sxs-lookup"><span data-stu-id="15488-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="15488-136">Выбор источника времени.</span><span class="sxs-lookup"><span data-stu-id="15488-136">Selecting the time source.</span></span>

-   <span data-ttu-id="15488-137">Уведомление приемников мультимедиа о часах</span><span class="sxs-lookup"><span data-stu-id="15488-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="15488-138">Запуск, остановка и приостановка часов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="15488-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="15488-139">Идет завершение работы часов.</span><span class="sxs-lookup"><span data-stu-id="15488-139">Shutting down the clock.</span></span>

<span data-ttu-id="15488-140">Чтобы получить указатель на часы презентации, вызовите [**имфмедиасессион::-Clock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="15488-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="15488-141">Часы презентации не возвращают допустимое время, пока сеанс мультимедиа не отправит событие [месессионтопологистатус](mesessiontopologystatus.md) с помощью флага подключения MF \_ топостатус \_ .</span><span class="sxs-lookup"><span data-stu-id="15488-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="15488-142">До **этого времени функция return возвращает** значение MF E с \_ \_ часами \_ без \_ \_ источника.</span><span class="sxs-lookup"><span data-stu-id="15488-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="15488-143">Приложение, использующее сеанс мультимедиа, никогда не должно запускать, останавливать или приостанавливать часы презентации; изменение частоты часов; или выключите часы.</span><span class="sxs-lookup"><span data-stu-id="15488-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="15488-144">Когда приложение вызывает [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), сеанс мультимедиа запускает презентацию с начальным временем, равным начальной позицией, указанной в методе **Start** .</span><span class="sxs-lookup"><span data-stu-id="15488-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="15488-145">Дополнительные сведения о сеансе мультимедиа см. в разделе [сеанс мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="15488-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15488-146">См. также</span><span class="sxs-lookup"><span data-stu-id="15488-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15488-147">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="15488-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



