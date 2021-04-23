---
title: 'Функции ввода с помощью мыши '
description: .
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47437458cc8ad2bf85ecfa0d8676af8d26c67b89
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797382"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="87479-103">Функции ввода с помощью мыши </span><span class="sxs-lookup"><span data-stu-id="87479-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="87479-104">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="87479-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87479-105">Раздел</span><span class="sxs-lookup"><span data-stu-id="87479-105">Topic</span></span></th>
<th><span data-ttu-id="87479-106">Описание</span><span class="sxs-lookup"><span data-stu-id="87479-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87479-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-108">Отправляет сообщения, когда указатель мыши покидает окно или наводится на окно в течение заданного промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="87479-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="87479-109">Эта функция вызывает <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEven</strong></a> , если она существует, в противном случае она эмулирует ее.</span><span class="sxs-lookup"><span data-stu-id="87479-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87479-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>драгдетект</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-111">Захватывает мышь и отслеживает ее движение, пока пользователь не отпустит левую кнопку мыши, не нажмет клавишу ESC или не переместит мышь за пределы прямоугольника перетаскивания, в котором находится указанная точка.</span><span class="sxs-lookup"><span data-stu-id="87479-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="87479-112">Ширина и высота прямоугольника перетаскивания задаются <strong>SM_CXDRAG</strong> и <strong>SM_CYDRAG</strong> значениями, возвращаемыми функцией <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>жетсистемметрикс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="87479-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87479-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>Захват</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-114">Извлекает маркер окна (при его наличии), которое захватило мышь.</span><span class="sxs-lookup"><span data-stu-id="87479-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="87479-115">Захват мыши может осуществляться только по одному окну. Это окно получает ввод с помощью мыши независимо от того, находится ли курсор внутри его границ.</span><span class="sxs-lookup"><span data-stu-id="87479-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87479-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>жетдаублекликктиме</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-117">Извлекает текущее время двойного щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="87479-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="87479-118">Двойной щелчок — это последовательность из двух щелчков кнопки мыши, вторая в течение заданного времени после первой.</span><span class="sxs-lookup"><span data-stu-id="87479-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="87479-119">Время двойного щелчка — это максимальное число миллисекунд, которое может произойти между первым и вторым щелчком двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="87479-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="87479-120">Максимальное время двойного щелчка составляет 5000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="87479-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87479-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>жетмаусемовепоинтсекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-122">Извлекает журнал до 64 предыдущих координат мыши или пера.</span><span class="sxs-lookup"><span data-stu-id="87479-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87479-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-124">Функция <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> синтезирования движения мыши и щелчков кнопок.</span><span class="sxs-lookup"><span data-stu-id="87479-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="87479-125">Эта функция была заменена.</span><span class="sxs-lookup"><span data-stu-id="87479-125">This function has been superseded.</span></span> <span data-ttu-id="87479-126">Вместо этого используйте <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="87479-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87479-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>релеасекаптуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-128">Освобождает захват мыши из окна в текущем потоке и восстанавливает нормальную обработку ввода мыши.</span><span class="sxs-lookup"><span data-stu-id="87479-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="87479-129">Окно, захваченное мышью, получает все входные данные мыши независимо от положения курсора, за исключением случаев нажатия кнопки мыши, когда активная активная кнопка находится в окне другого потока.</span><span class="sxs-lookup"><span data-stu-id="87479-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87479-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>сеткаптуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-131">Устанавливает захват мыши в указанное окно, принадлежащее текущему потоку.</span><span class="sxs-lookup"><span data-stu-id="87479-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87479-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>сетдаублекликктиме</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-133">Задает время двойного щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="87479-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="87479-134">Двойной щелчок — это последовательность из двух щелчков кнопки мыши, вторая в течение заданного времени после первой.</span><span class="sxs-lookup"><span data-stu-id="87479-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="87479-135">Время двойного щелчка — это максимальное число миллисекунд, которое может произойти между первым и вторым щелчками двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="87479-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87479-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>свапмаусебуттон</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-137">Изменяет значение левой и правой кнопок мыши на противоположное или восстанавливает его.</span><span class="sxs-lookup"><span data-stu-id="87479-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87479-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEven</strong></a></span><span class="sxs-lookup"><span data-stu-id="87479-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="87479-139">Отправляет сообщения, когда указатель мыши покидает окно или наводится на окно в течение заданного промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="87479-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="87479-140">Функция <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> вызывает <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEven</strong></a> , если она существует, в противном случае <strong>_TrackMouseEvent</strong> эмулирует <strong>TrackMouseEven</strong>.</span><span class="sxs-lookup"><span data-stu-id="87479-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

