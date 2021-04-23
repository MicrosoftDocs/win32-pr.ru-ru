---
description: Использование элементов управления отображением видео
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Использование элементов управления отображением видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811519"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="bb706-103">Использование элементов управления отображением видео</span><span class="sxs-lookup"><span data-stu-id="bb706-103">Using the Video Display Controls</span></span>

<span data-ttu-id="bb706-104">Интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) управляет отображением видео в окне приложения с помощью расширенного обработчика видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="bb706-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="bb706-105">Этот интерфейс можно использовать либо в DirectShow, либо в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bb706-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="bb706-106">На внутреннем уровне элементы управления отображением видео предоставляются средством отображения по умолчанию Евр.</span><span class="sxs-lookup"><span data-stu-id="bb706-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="bb706-107">При написании пользовательского Presenter можно предоставить тот же интерфейс или определить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bb706-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="bb706-108">Правильный способ получения указателя на интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) зависит от того, используется ли версия DirectShow Евр или версия Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bb706-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="bb706-109">Для Media Foundation Евр это также зависит от того, используется ли Евр напрямую или с помощью сеанса мультимедиа (что является более типичным).</span><span class="sxs-lookup"><span data-stu-id="bb706-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="bb706-110">Чтобы получить указатель на интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb706-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="bb706-111">Получает указатель на интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="bb706-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="bb706-112">Если используется фильтр Евр DirectShow, вызовите **QueryInterface** в фильтре.</span><span class="sxs-lookup"><span data-stu-id="bb706-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="bb706-113">Если вы используете приемник мультимедиа Евр напрямую, вызовите **QueryInterface** в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bb706-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="bb706-114">Если вы используете сеанс мультимедиа, вызовите **QueryInterface** в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bb706-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="bb706-115">Если вы используете сеанс мультимедиа, подождите, пока сеанс мультимедиа отправит событие [месессионтопологистатус](mesessiontopologystatus.md) со значением status, равным MF \_ топостатус \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="bb706-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="bb706-116">(Пропустите этот шаг в противном случае.)</span><span class="sxs-lookup"><span data-stu-id="bb706-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="bb706-117">Вызовите [**имфжетсервице:: Get Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="bb706-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="bb706-118">Идентификатор службы — это \_ \_ Служба прорисовки видео Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="bb706-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="bb706-119">Интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) можно использовать для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bb706-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="bb706-120">Задайте окно обрезки.</span><span class="sxs-lookup"><span data-stu-id="bb706-120">Set the clipping window.</span></span>

-   <span data-ttu-id="bb706-121">Задайте исходные и конечные прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="bb706-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="bb706-122">Обновление окна видео в ответ на сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="bb706-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="bb706-123">Включает или отключает полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="bb706-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="bb706-124">Окно обрезки</span><span class="sxs-lookup"><span data-stu-id="bb706-124">Clipping Window</span></span>

<span data-ttu-id="bb706-125">Приложение должно предоставить окно, в котором Евр рисует видео.</span><span class="sxs-lookup"><span data-stu-id="bb706-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="bb706-126">Чтобы задать окно обрезки, вызовите [**имфвидеодисплайконтрол:: сетвидеовиндов**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) с помощью маркера в окне приложения.</span><span class="sxs-lookup"><span data-stu-id="bb706-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="bb706-127">Если создать приемник мультимедиа Евр с помощью объекта активации, этот шаг не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bb706-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="bb706-128">Объект активации автоматически вызывает [**сетвидеовиндов**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), используя описатель окна, указанный в функции [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="bb706-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="bb706-129">Исходный и конечный прямоугольники</span><span class="sxs-lookup"><span data-stu-id="bb706-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="bb706-130">Во время воспроизведения выступающий принимает часть составного изображения видео и рисует его в области окна видео.</span><span class="sxs-lookup"><span data-stu-id="bb706-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="bb706-131">Часть составного изображения является *исходным прямоугольником*, а область окна видео — *прямоугольником назначения*.</span><span class="sxs-lookup"><span data-stu-id="bb706-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="bb706-132">Исходный прямоугольник определяется с использованием нормализованных координат, где точка (0,0, 0,0) соответствует левому верхнему углу видео, а (1,0, 1,0) соответствует нижнему правому углу видео.</span><span class="sxs-lookup"><span data-stu-id="bb706-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="bb706-133">Исходный прямоугольник может быть любой областью внутри этого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="bb706-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="bb706-134">Прямоугольник назначения задается в пикселях относительно клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="bb706-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="bb706-135">Исходный прямоугольник по умолчанию — это все изображение, а прямоугольник назначения по умолчанию — пустой прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="bb706-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="bb706-136">Чтобы задать исходный и конечный прямоугольники, вызовите метод [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="bb706-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="bb706-137">Если создать приемник мультимедиа Евр с помощью объекта активации, этот шаг не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bb706-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="bb706-138">Объект активации автоматически задает прямоугольник назначения, равный всей клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="bb706-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="bb706-139">Однако следует вызвать [**сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) , если необходимо изменить исходный прямоугольник или задать другой конечный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="bb706-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="bb706-140">Сообщения окна</span><span class="sxs-lookup"><span data-stu-id="bb706-140">Window Messages</span></span>

<span data-ttu-id="bb706-141">Во время воспроизведения приложение должно отвечать на определенные окна сообщений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bb706-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="bb706-142">WM \_ Paint: вызов [**имфвидеодисплайконтрол:: репаинтвидео**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) для перерисовки видео.</span><span class="sxs-lookup"><span data-stu-id="bb706-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="bb706-143">Кроме того, Избегайте прорисовки прямоугольника назначения во время воспроизведения видео, так как это может вызвать мерцание.</span><span class="sxs-lookup"><span data-stu-id="bb706-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="bb706-144">\_Размер WM: может потребоваться вызвать [**сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) для изменения размера прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="bb706-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="bb706-145">В отличие от фильтра "Микширование видео" (VMR) в DirectShow не нужно уведомлять Евр о получении \_ сообщения ДИСПЛАЙЧАНЖЕ WM.</span><span class="sxs-lookup"><span data-stu-id="bb706-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb706-146">См. также</span><span class="sxs-lookup"><span data-stu-id="bb706-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb706-147">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="bb706-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



