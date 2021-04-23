---
description: Использование оконного режима
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Использование оконного режима
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663753"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="12cc3-103">Использование оконного режима</span><span class="sxs-lookup"><span data-stu-id="12cc3-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="12cc3-104">Устаревший [Фильтр модуля подготовки отчетов видео](video-renderer-filter.md) всегда использует оконный режим.</span><span class="sxs-lookup"><span data-stu-id="12cc3-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="12cc3-105">Фильтры VMR-7 и VMR-9 используют оконный режим по умолчанию, но также поддерживают режим без окон.</span><span class="sxs-lookup"><span data-stu-id="12cc3-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="12cc3-106">В оконном режиме модуль подготовки отчетов создает собственное окно, в котором он рисует кадры видео.</span><span class="sxs-lookup"><span data-stu-id="12cc3-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="12cc3-107">Если не указано иное, это окно верхнего уровня с собственными границами и заголовком окна.</span><span class="sxs-lookup"><span data-stu-id="12cc3-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="12cc3-108">Однако в большинстве случаев окно видео будет присоединено к окну приложения, чтобы оно было интегрировано в пользовательский интерфейс приложения.</span><span class="sxs-lookup"><span data-stu-id="12cc3-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="12cc3-109">Для этого необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="12cc3-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="12cc3-110">Запрос для **ивидеовиндов**.</span><span class="sxs-lookup"><span data-stu-id="12cc3-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="12cc3-111">Задайте родительское окно.</span><span class="sxs-lookup"><span data-stu-id="12cc3-111">Set the parent window.</span></span>
3.  <span data-ttu-id="12cc3-112">Установить новые стили окна.</span><span class="sxs-lookup"><span data-stu-id="12cc3-112">Set new window styles.</span></span>
4.  <span data-ttu-id="12cc3-113">Расположение окна видео в окне "владелец".</span><span class="sxs-lookup"><span data-stu-id="12cc3-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="12cc3-114">Уведомление окна видео о \_ перемещении сообщений WM.</span><span class="sxs-lookup"><span data-stu-id="12cc3-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="12cc3-115">**Запрос для Ивидеовиндов**</span><span class="sxs-lookup"><span data-stu-id="12cc3-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="12cc3-116">Перед запуском воспроизведения запросите диспетчер графов фильтров для интерфейса **ивидеовиндов** :</span><span class="sxs-lookup"><span data-stu-id="12cc3-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="12cc3-117">**Задание родительского окна**</span><span class="sxs-lookup"><span data-stu-id="12cc3-117">**Set the Parent Window**</span></span>

<span data-ttu-id="12cc3-118">Чтобы задать родительское окно, вызовите метод [**ивидеовиндов::p UT \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) с помощью маркера окна приложения.</span><span class="sxs-lookup"><span data-stu-id="12cc3-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="12cc3-119">Этот метод принимает переменную типа [**оахвнд**](oahwnd.md), поэтому приведите этот обработчик к этому типу:</span><span class="sxs-lookup"><span data-stu-id="12cc3-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="12cc3-120">**Установить новые стили окна**</span><span class="sxs-lookup"><span data-stu-id="12cc3-120">**Set New Window Styles**</span></span>

<span data-ttu-id="12cc3-121">Измените стиль окна видео, вызвав метод [**ивидеовиндов::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :</span><span class="sxs-lookup"><span data-stu-id="12cc3-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="12cc3-122">Флаг WS \_ дочернего окна устанавливает, что окно является дочерним, а \_ флаг WS клипсиблингс предотвращает Рисование окна внутри клиентской области другого дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="12cc3-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="12cc3-123">**Расположение окна видео**</span><span class="sxs-lookup"><span data-stu-id="12cc3-123">**Position the Video Window**</span></span>

<span data-ttu-id="12cc3-124">Чтобы задать расположение видео относительно клиентской области окна приложения, вызовите метод [**ивидеовиндов:: сетвиндовпоситион**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="12cc3-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="12cc3-125">Этот метод принимает прямоугольник, указывающий левую границу, верхнюю границу, ширину и высоту окна видео.</span><span class="sxs-lookup"><span data-stu-id="12cc3-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="12cc3-126">Например, следующий код растягивает окно видео в соответствии со всей клиентской областью родительского окна:</span><span class="sxs-lookup"><span data-stu-id="12cc3-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="12cc3-127">Чтобы получить собственный размер видео, вызовите метод [**ибасиквидео:: жетвидеосизе**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="12cc3-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="12cc3-128">Эти сведения можно использовать для масштабирования видео и сохранения правильных пропорций.</span><span class="sxs-lookup"><span data-stu-id="12cc3-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="12cc3-129">**Реагирование на \_ сообщения о перемещении WM**</span><span class="sxs-lookup"><span data-stu-id="12cc3-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="12cc3-130">Для лучшей производительности следует уведомлять модуль подготовки отчетов каждый раз, когда окно перемещается во время приостановки графа.</span><span class="sxs-lookup"><span data-stu-id="12cc3-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="12cc3-131">Вызовите метод [**ивидеовиндов:: нотифйовнермессаже**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) для пересылки \_ сообщения о перемещении WM:</span><span class="sxs-lookup"><span data-stu-id="12cc3-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="12cc3-132">Если модуль подготовки отчетов использует наложение оборудования, это уведомление приводит к тому, что модуль подготовки отчетов обновляет расположение оверлея.</span><span class="sxs-lookup"><span data-stu-id="12cc3-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="12cc3-133">(VMR-9 не использует наложение, поэтому вам не нужно вызывать этот метод, если вы используете VMR-9.)</span><span class="sxs-lookup"><span data-stu-id="12cc3-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="12cc3-134">**Очистить**</span><span class="sxs-lookup"><span data-stu-id="12cc3-134">**Clean Up**</span></span>

<span data-ttu-id="12cc3-135">Перед выходом из приложения остановите граф и сбросьте владельца видео на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="12cc3-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="12cc3-136">В противном случае сообщения окна могут быть отправлены в неправильное окно, что может вызвать ошибки.</span><span class="sxs-lookup"><span data-stu-id="12cc3-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="12cc3-137">Кроме того, можно скрыть окно видео или на экране мгновенно заметить мерцание изображения:</span><span class="sxs-lookup"><span data-stu-id="12cc3-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="12cc3-138">Если родительский элемент окна видео является дочерним по отношению к главному окну приложения (иными словами, если окно видео является дочерним для дочернего элемента), следует создать видеоокно с помощью **CoCreateInstance** и добавить его к графу, не позволяя диспетчеру графа фильтров добавлять модуль подготовки видео во время [интеллектуального подключения](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="12cc3-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="12cc3-139">Это гарантирует, что окно видео и его дочернее окно будут перерисовываться в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="12cc3-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="12cc3-140">В противном случае дочернее окно может перерисовываться через окно видео.</span><span class="sxs-lookup"><span data-stu-id="12cc3-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="12cc3-141">См. также</span><span class="sxs-lookup"><span data-stu-id="12cc3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12cc3-142">Рендеринг видео</span><span class="sxs-lookup"><span data-stu-id="12cc3-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



