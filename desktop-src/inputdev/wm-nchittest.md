---
title: Сообщение WM_NCHITTEST (Winuser. h)
description: Отправляется в окно, чтобы определить, какая часть окна соответствует определенной координате экрана.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691804"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="49f75-104">\_Сообщение НЧИТТЕСТ WM</span><span class="sxs-lookup"><span data-stu-id="49f75-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="49f75-105">Отправляется в окно, чтобы определить, какая часть окна соответствует определенной координате экрана.</span><span class="sxs-lookup"><span data-stu-id="49f75-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="49f75-106">Это может произойти, например, при перемещении курсора, при нажатии или отпускании кнопки мыши или в ответ на вызов функции, такой как [**виндовфромпоинт**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="49f75-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="49f75-107">Если мышь не захвачена, сообщение отправляется в окно под курсором.</span><span class="sxs-lookup"><span data-stu-id="49f75-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="49f75-108">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="49f75-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="49f75-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49f75-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="49f75-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="49f75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49f75-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49f75-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49f75-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="49f75-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="49f75-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49f75-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49f75-114">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="49f75-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="49f75-115">Координата задается относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="49f75-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="49f75-116">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="49f75-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="49f75-117">Координата задается относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="49f75-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49f75-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49f75-118">Return value</span></span>

<span data-ttu-id="49f75-119">Возвращаемое значение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) является одним из следующих значений, указывающим позицию курсора в горячей точке.</span><span class="sxs-lookup"><span data-stu-id="49f75-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="49f75-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="49f75-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="49f75-121">Описание</span><span class="sxs-lookup"><span data-stu-id="49f75-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49f75-122"><dt>**Хтбордер**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="49f75-123">В границах окна, у которых нет границы изменения размера.</span><span class="sxs-lookup"><span data-stu-id="49f75-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="49f75-124"><dt>**Хтботтом**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="49f75-125">В нижней горизонтальной границе окна изменяемого размера (пользователь может щелкнуть мышью, чтобы изменить размер окна по вертикали).</span><span class="sxs-lookup"><span data-stu-id="49f75-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="49f75-126"><dt>**Хтботтомлефт**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="49f75-127">В левом нижнем углу границы окна изменяемого размера (пользователь может щелкнуть мышью, чтобы изменить размер окна по диагонали).</span><span class="sxs-lookup"><span data-stu-id="49f75-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="49f75-128"><dt>**Хтботтомригхт**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="49f75-129">В правом нижнем углу границы окна изменяемого размера (пользователь может щелкнуть мышью, чтобы изменить размер окна по диагонали).</span><span class="sxs-lookup"><span data-stu-id="49f75-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="49f75-130"><dt>**Хткаптион**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="49f75-131">В заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="49f75-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="49f75-132"><dt>**Хтклиент**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="49f75-133">В клиентской области.</span><span class="sxs-lookup"><span data-stu-id="49f75-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="49f75-134"><dt>**Хтклосе**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="49f75-135">В кнопке **Закрыть** .</span><span class="sxs-lookup"><span data-stu-id="49f75-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="49f75-136"><dt>**Хтеррор**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="49f75-137">На фоне экрана или на разделительной линии между окнами (то же, что и **хтновхере**, за исключением того, что функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выдает системный сигнал для указания на ошибку).</span><span class="sxs-lookup"><span data-stu-id="49f75-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="49f75-138"><dt>**Хтгровбокс**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="49f75-139">В поле размера (то же, что и **хтсизе**).</span><span class="sxs-lookup"><span data-stu-id="49f75-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="49f75-140"><dt>**Хселп**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="49f75-141">В кнопке **справки** .</span><span class="sxs-lookup"><span data-stu-id="49f75-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="49f75-142"><dt>**Хсскролл**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="49f75-143">В горизонтальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="49f75-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="49f75-144"><dt>**Хтлефт**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="49f75-145">В левой границе окна изменяемого размера (пользователь может щелкнуть мышью, чтобы изменить размер окна по горизонтали).</span><span class="sxs-lookup"><span data-stu-id="49f75-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="49f75-146"><dt>**Хтмену**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="49f75-147">В меню.</span><span class="sxs-lookup"><span data-stu-id="49f75-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="49f75-148"><dt>**Хтмаксбуттон**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="49f75-149">В кнопке **развертывания** .</span><span class="sxs-lookup"><span data-stu-id="49f75-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="49f75-150"><dt>**Хтминбуттон**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="49f75-151">В кнопке **сворачивания** .</span><span class="sxs-lookup"><span data-stu-id="49f75-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="49f75-152"><dt>**Хтновхере**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="49f75-153">На фоне экрана или на разделительной линии между окнами.</span><span class="sxs-lookup"><span data-stu-id="49f75-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="49f75-154"><dt>**Хтредуце**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="49f75-155">В кнопке **сворачивания** .</span><span class="sxs-lookup"><span data-stu-id="49f75-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="49f75-156"><dt>**Хтригхт**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="49f75-157">В правой границе окна изменяемого размера (пользователь может щелкнуть мышью, чтобы изменить размер окна по горизонтали).</span><span class="sxs-lookup"><span data-stu-id="49f75-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="49f75-158"><dt>**Хтсизе**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="49f75-159">В поле размера (то же, что и **хтгровбокс**).</span><span class="sxs-lookup"><span data-stu-id="49f75-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="49f75-160"><dt>**Хтсисмену**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="49f75-161">В меню окна или в кнопке **закрытия** дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="49f75-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="49f75-162"><dt>**Хттоп**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="49f75-163">В верхней горизонтальной границе окна.</span><span class="sxs-lookup"><span data-stu-id="49f75-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="49f75-164"><dt>**Хттоплефт**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="49f75-165">В левом верхнем углу границы окна.</span><span class="sxs-lookup"><span data-stu-id="49f75-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="49f75-166"><dt>**Хттопригхт**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="49f75-167">В правом верхнем углу границы окна.</span><span class="sxs-lookup"><span data-stu-id="49f75-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="49f75-168"><dt>**Хттранспарент**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="49f75-169">В окне, которое в настоящий момент покрывается другим окном в том же потоке (сообщение будет отправлено в базовые окна в том же потоке, пока один из них не вернет код, который не **хттранспарент**).</span><span class="sxs-lookup"><span data-stu-id="49f75-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="49f75-170"><dt>**Хтвскролл**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="49f75-171">На вертикальной полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="49f75-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="49f75-172"><dt>**Хтзум**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="49f75-173">В кнопке **развертывания** .</span><span class="sxs-lookup"><span data-stu-id="49f75-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="49f75-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49f75-174">Remarks</span></span>

<span data-ttu-id="49f75-175">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="49f75-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="49f75-176">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="49f75-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="49f75-177">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="49f75-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="49f75-178">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="49f75-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49f75-179">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="49f75-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="49f75-180">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="49f75-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="49f75-181">**Windows Vista:** При создании пользовательских фреймов, содержащих стандартные кнопки заголовков, это сообщение сначала должно быть передано функции [**двмдефвиндовпрок**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="49f75-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="49f75-182">Это позволяет диспетчер окон рабочего стола (DWM) обеспечивать проверку попадания для кнопок субтитров.</span><span class="sxs-lookup"><span data-stu-id="49f75-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="49f75-183">Если **двмдефвиндовпрок** не обрабатывает это сообщение, может потребоваться дополнительная обработка **WM \_ нчиттест** .</span><span class="sxs-lookup"><span data-stu-id="49f75-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f75-184">Требования</span><span class="sxs-lookup"><span data-stu-id="49f75-184">Requirements</span></span>



| <span data-ttu-id="49f75-185">Требование</span><span class="sxs-lookup"><span data-stu-id="49f75-185">Requirement</span></span> | <span data-ttu-id="49f75-186">Значение</span><span class="sxs-lookup"><span data-stu-id="49f75-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f75-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49f75-187">Minimum supported client</span></span><br/> | <span data-ttu-id="49f75-188">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49f75-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49f75-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49f75-189">Minimum supported server</span></span><br/> | <span data-ttu-id="49f75-190">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49f75-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49f75-191">Заголовок</span><span class="sxs-lookup"><span data-stu-id="49f75-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="49f75-192"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49f75-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f75-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49f75-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="49f75-194">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="49f75-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49f75-195">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="49f75-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="49f75-196">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="49f75-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="49f75-197">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="49f75-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="49f75-198">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="49f75-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="49f75-199">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="49f75-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="49f75-200">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="49f75-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="49f75-201">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="49f75-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="49f75-202">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49f75-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

