---
title: Установка изображения курсора
description: Установка изображения курсора
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487609"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="5ebaa-103">Установка изображения курсора</span><span class="sxs-lookup"><span data-stu-id="5ebaa-103">Setting the Cursor Image</span></span>

<span data-ttu-id="5ebaa-104">*Курсор* является небольшим изображением, которое показывает расположение мыши или другого указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="5ebaa-105">Многие приложения изменяют изображение курсора для предоставления пользователю обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="5ebaa-106">Хотя это и не является обязательным, оно добавляет к вашему приложению хороший набор польскостей.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="5ebaa-107">Windows предоставляет набор стандартных изображений курсоров, называемых *системными курсорами*.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="5ebaa-108">К ним относятся стрелка, рука, I-образный, Песочные часы (теперь это вращающийся круг) и другие.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="5ebaa-109">В этом разделе описывается использование системных курсоров.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="5ebaa-110">Для более сложных задач, таких как создание пользовательских курсоров, см. раздел [курсоры](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="5ebaa-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="5ebaa-111">Курсор можно связать с классом окна, задав элемент **хкурсор** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) или [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .</span><span class="sxs-lookup"><span data-stu-id="5ebaa-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="5ebaa-112">В противном случае курсором по умолчанию является стрелка.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="5ebaa-113">Когда указатель мыши перемещается над окном, окно получает сообщение [**WM \_ сеткурсор**](/windows/desktop/menurc/wm-setcursor) (если мышь не захвачена другим окном).</span><span class="sxs-lookup"><span data-stu-id="5ebaa-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="5ebaa-114">На этом этапе происходит одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="5ebaa-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="5ebaa-115">Приложение задает курсор, а процедура окна возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="5ebaa-116">Приложение не выполняет никаких действий и [**передает \_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="5ebaa-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="5ebaa-117">Чтобы установить курсор, программа выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5ebaa-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="5ebaa-118">Вызывает [**лоадкурсор**](/windows/desktop/api/winuser/nf-winuser-loadcursora) для загрузки курсора в память.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="5ebaa-119">Эта функция возвращает маркер в курсор.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="5ebaa-120">Вызывает [**сеткурсор**](/windows/desktop/api/winuser/nf-winuser-setcursor) и передает маркеру курсора.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="5ebaa-121">В противном случае, если приложение передает [**WM \_ Сеткурсор**](/windows/desktop/menurc/wm-setcursor) в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), функция **дефвиндовпрок** использует следующий алгоритм для задания изображения курсора:</span><span class="sxs-lookup"><span data-stu-id="5ebaa-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="5ebaa-122">Если окно имеет родителя, перешлите сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) в родительский объект, чтобы он обрабатывал.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="5ebaa-123">В противном случае, если окно содержит курсор класса, установите курсор на курсор класса.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="5ebaa-124">Если курсор класса отсутствует, установите курсор на курсор со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="5ebaa-125">Функция [**лоадкурсор**](/windows/desktop/api/winuser/nf-winuser-loadcursora) может загрузить пользовательский курсор из ресурса или одного из системных курсоров.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="5ebaa-126">В следующем примере показано, как установить курсор на курсор системы.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="5ebaa-127">При изменении курсора изображение курсора сбрасывается при следующем перемещении мыши, если только вы не перехватите сообщение [**\_ сеткурсор WM**](/windows/desktop/menurc/wm-setcursor) и не настроите курсор снова.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="5ebaa-128">В следующем коде показано, как работать с **WM \_ сеткурсор**.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="5ebaa-129">Этот код сначала проверяет младшие 16 бит *lParam*.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="5ebaa-130">Если `LOWORD(lParam)` равно **хтклиент**, то это означает, что курсор находится над клиентской областью окна.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="5ebaa-131">В противном случае курсор находится над неклиентской областью.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="5ebaa-132">Как правило, курсор должен устанавливаться только для клиентской области, а Windows может устанавливать курсор для неклиентской области.</span><span class="sxs-lookup"><span data-stu-id="5ebaa-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="5ebaa-133">Следующая</span><span class="sxs-lookup"><span data-stu-id="5ebaa-133">Next</span></span>

[<span data-ttu-id="5ebaa-134">Ввод данных пользователем: Расширенный пример</span><span class="sxs-lookup"><span data-stu-id="5ebaa-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 