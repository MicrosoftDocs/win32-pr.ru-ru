---
title: Рисование окна
description: Вы создали окно. Теперь нужно отобразить что-то в нем. В терминологии Windows это называется рисованием окна. Чтобы смешивать метафоры, окно — это пустой холст, ожидающий его заполнения.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104553083"
---
# <a name="painting-the-window"></a><span data-ttu-id="825ba-106">Рисование окна</span><span class="sxs-lookup"><span data-stu-id="825ba-106">Painting the Window</span></span>

<span data-ttu-id="825ba-107">Вы создали окно.</span><span class="sxs-lookup"><span data-stu-id="825ba-107">You've created your window.</span></span> <span data-ttu-id="825ba-108">Теперь нужно отобразить что-то в нем.</span><span class="sxs-lookup"><span data-stu-id="825ba-108">Now you want to show something inside it.</span></span> <span data-ttu-id="825ba-109">В терминологии Windows это называется рисованием окна.</span><span class="sxs-lookup"><span data-stu-id="825ba-109">In Windows terminology, this is called painting the window.</span></span> <span data-ttu-id="825ba-110">Чтобы смешивать метафоры, окно — это пустой холст, ожидающий его заполнения.</span><span class="sxs-lookup"><span data-stu-id="825ba-110">To mix metaphors, a window is a blank canvas, waiting for you to fill it.</span></span>

<span data-ttu-id="825ba-111">Иногда программа запустит Рисование для обновления внешнего вида окна.</span><span class="sxs-lookup"><span data-stu-id="825ba-111">Sometimes your program will initiate painting to update the appearance of the window.</span></span> <span data-ttu-id="825ba-112">В других случаях операционная система сообщит вам, что необходимо перекрасить часть окна.</span><span class="sxs-lookup"><span data-stu-id="825ba-112">At other times, the operating system will notify you that you must repaint a portion of the window.</span></span> <span data-ttu-id="825ba-113">В этом случае операционная система отправляет окну сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="825ba-113">When this occurs, the operating system sends the window a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="825ba-114">Часть окна, которая должна быть окрашена, называется *областью обновления*.</span><span class="sxs-lookup"><span data-stu-id="825ba-114">The portion of the window that must be painted is called the *update region*.</span></span>

<span data-ttu-id="825ba-115">При первом отображении окна вся клиентская область окна должна быть окрашена.</span><span class="sxs-lookup"><span data-stu-id="825ba-115">The first time a window is shown, the entire client area of the window must be painted.</span></span> <span data-ttu-id="825ba-116">Поэтому при отображении окна всегда будет отображаться по крайней мере одно сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="825ba-116">Therefore, you will always receive at least one [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message when you show a window.</span></span>

![Иллюстрация, показывающая область обновления окна](images/painting01.png)

<span data-ttu-id="825ba-118">Вы несете ответственность за рисование клиентской области.</span><span class="sxs-lookup"><span data-stu-id="825ba-118">You are only responsible for painting the client area.</span></span> <span data-ttu-id="825ba-119">Окружающий фрейм, включая заголовок окна, автоматически зарисовывается операционной системой.</span><span class="sxs-lookup"><span data-stu-id="825ba-119">The surrounding frame, including the title bar, is automatically painted by the operating system.</span></span> <span data-ttu-id="825ba-120">После завершения заполнения клиентской области очищается регион обновления, который сообщает операционной системе, что ей не нужно отсылать другое сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , пока что не изменится.</span><span class="sxs-lookup"><span data-stu-id="825ba-120">After you finish painting the client area, you clear the update region, which tells the operating system that it does not need to send another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message until something changes.</span></span>

<span data-ttu-id="825ba-121">Теперь предположим, что пользователь перемещает другое окно, чтобы оно скрывало часть окна.</span><span class="sxs-lookup"><span data-stu-id="825ba-121">Now suppose the user moves another window so that it obscures a portion of your window.</span></span> <span data-ttu-id="825ba-122">Когда скрытая часть снова становится видимой, эта часть добавляется в область обновления, и окно получает другое сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="825ba-122">When the obscured portion becomes visible again, that portion is added to the update region, and your window receives another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

![Иллюстрация изменения региона обновления при перекрытии двух окон](images/painting02.png)

<span data-ttu-id="825ba-124">Регион обновления также изменяется, если пользователь растягивает окно.</span><span class="sxs-lookup"><span data-stu-id="825ba-124">The update region also changes if the user stretches the window.</span></span> <span data-ttu-id="825ba-125">На следующей схеме пользователь растягивает окно вправо.</span><span class="sxs-lookup"><span data-stu-id="825ba-125">In the following diagram, the user stretches the window to the right.</span></span> <span data-ttu-id="825ba-126">Новая развернутая область в правой части окна добавляется в область обновления:</span><span class="sxs-lookup"><span data-stu-id="825ba-126">The newly exposed area on the right side of the window is added to the update region:</span></span>

![Иллюстрация изменения области обновления при изменении размера окна](images/painting03.png)

<span data-ttu-id="825ba-128">В нашем первом примере программы подпрограмма рисования очень проста.</span><span class="sxs-lookup"><span data-stu-id="825ba-128">In our first example program, the painting routine is very simple.</span></span> <span data-ttu-id="825ba-129">Он просто заполняет всю клиентскую область сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="825ba-129">It just fills the entire client area with a solid color.</span></span> <span data-ttu-id="825ba-130">Тем не менее, этот пример достаточно для демонстрации некоторых важных концепций.</span><span class="sxs-lookup"><span data-stu-id="825ba-130">Still, this example is enough to demonstrate some of the important concepts.</span></span>

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

<span data-ttu-id="825ba-131">Запустите операцию рисования, вызвав функцию [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="825ba-131">Start the painting operation by calling the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span> <span data-ttu-id="825ba-132">Эта функция заполняет структуру [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) сведениями о запросе на перерисовку.</span><span class="sxs-lookup"><span data-stu-id="825ba-132">This function fills in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure with information on the repaint request.</span></span> <span data-ttu-id="825ba-133">Текущий регион обновления указывается в элементе **члене rcpaint структуры** элемента **PAINTSTRUCT**.</span><span class="sxs-lookup"><span data-stu-id="825ba-133">The current update region is given in the **rcPaint** member of **PAINTSTRUCT**.</span></span> <span data-ttu-id="825ba-134">Этот регион обновления определяется относительно клиентской области:</span><span class="sxs-lookup"><span data-stu-id="825ba-134">This update region is defined relative to the client area:</span></span>

![Иллюстрация, показывающая происхождение клиентской области](images/painting04.png)

<span data-ttu-id="825ba-136">В коде рисования есть два основных варианта:</span><span class="sxs-lookup"><span data-stu-id="825ba-136">In your painting code, you have two basic options:</span></span>

- <span data-ttu-id="825ba-137">Заполните всю клиентскую область независимо от размера области обновления.</span><span class="sxs-lookup"><span data-stu-id="825ba-137">Paint the entire client area, regardless of the size of the update region.</span></span> <span data-ttu-id="825ba-138">Все, что находится за пределами области обновления, обрезается.</span><span class="sxs-lookup"><span data-stu-id="825ba-138">Anything that falls outside of the update region is clipped.</span></span> <span data-ttu-id="825ba-139">То есть операционная система пропускает ее.</span><span class="sxs-lookup"><span data-stu-id="825ba-139">That is, the operating system ignores it.</span></span>
- <span data-ttu-id="825ba-140">Оптимизируйте, рисуя только часть окна внутри области обновления.</span><span class="sxs-lookup"><span data-stu-id="825ba-140">Optimize by painting just the portion of the window inside the update region.</span></span>

<span data-ttu-id="825ba-141">Если вы всегда рисуете всю клиентскую область, код будет проще.</span><span class="sxs-lookup"><span data-stu-id="825ba-141">If you always paint the entire client area, the code will be simpler.</span></span> <span data-ttu-id="825ba-142">Однако при наличии сложной логики рисования может быть более эффективным пропускать области за пределами области обновления.</span><span class="sxs-lookup"><span data-stu-id="825ba-142">If you have complicated painting logic, however, it can be more efficient to skip the areas outside of the update region.</span></span>

<span data-ttu-id="825ba-143">Следующая строка кода заполняет область обновления одним цветом, используя определенный системой цвет фона окна (**\_ окно цвета**).</span><span class="sxs-lookup"><span data-stu-id="825ba-143">The following line of code fills the update region with a single color, using the system-defined window background color (**COLOR\_WINDOW**).</span></span> <span data-ttu-id="825ba-144">Фактический цвет, указанный **в \_ окне цвета** , зависит от текущей цветовой схемы пользователя.</span><span class="sxs-lookup"><span data-stu-id="825ba-144">The actual color indicated by **COLOR\_WINDOW** depends on the user's current color scheme.</span></span>

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

<span data-ttu-id="825ba-145">Сведения о [**филлрект**](/windows/desktop/api/winuser/nf-winuser-fillrect) не важны для этого примера, но второй параметр дает координаты прямоугольника для заполнения.</span><span class="sxs-lookup"><span data-stu-id="825ba-145">The details of [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) are not important for this example, but the second parameter gives the coordinates of the rectangle to fill.</span></span> <span data-ttu-id="825ba-146">В этом случае мы передаем весь регион обновления (член **члене rcpaint структуры** объекта [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)).</span><span class="sxs-lookup"><span data-stu-id="825ba-146">In this case, we pass in the entire update region (the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)).</span></span> <span data-ttu-id="825ba-147">В первом сообщении [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) вся клиентская область должна быть окрашена, поэтому **члене rcpaint структуры** будет содержать всю клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="825ba-147">On the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, the entire client area needs to be painted, so **rcPaint** will contain the entire client area.</span></span> <span data-ttu-id="825ba-148">В последующих сообщениях **WM \_ Paint** **члене rcpaint структуры** может содержать прямоугольник меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="825ba-148">On subsequent **WM\_PAINT** messages, **rcPaint** might contain a smaller rectangle.</span></span>

<span data-ttu-id="825ba-149">Функция [**филлрект**](/windows/desktop/api/winuser/nf-winuser-fillrect) является частью интерфейс графических устройств (GDI), которая имеет встроенную графику Windows в течение очень долгого времени.</span><span class="sxs-lookup"><span data-stu-id="825ba-149">The [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) function is part of the Graphics Device Interface (GDI), which has powered Windows graphics for a very long time.</span></span> <span data-ttu-id="825ba-150">В Windows 7 Корпорация Майкрософт представила новый графический механизм с именем Direct2D, который поддерживает высокопроизводительные графические операции, такие как аппаратное ускорение.</span><span class="sxs-lookup"><span data-stu-id="825ba-150">In Windows 7, Microsoft introduced a new graphics engine, named Direct2D, which supports high-performance graphics operations, such as hardware acceleration.</span></span> <span data-ttu-id="825ba-151">Direct2D также доступен для Windows Vista через [обновление платформы для Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) и для windows Server 2008 с помощью обновления платформы для windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="825ba-151">Direct2D is also available for Windows Vista through the [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) and for Windows Server 2008 through the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="825ba-152">(GDI по-прежнему полностью поддерживается.)</span><span class="sxs-lookup"><span data-stu-id="825ba-152">(GDI is still fully supported.)</span></span>

<span data-ttu-id="825ba-153">Завершив рисование, вызовите функцию [**ендпаинт**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="825ba-153">After you are done painting, call the [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) function.</span></span> <span data-ttu-id="825ba-154">Эта функция очищает регион обновления, который сообщает Windows, что окно завершило свою прорисовку.</span><span class="sxs-lookup"><span data-stu-id="825ba-154">This function clears the update region, which signals to Windows that the window has completed painting itself.</span></span>

## <a name="next"></a><span data-ttu-id="825ba-155">Следующая</span><span class="sxs-lookup"><span data-stu-id="825ba-155">Next</span></span>

[<span data-ttu-id="825ba-156">Закрытие окна</span><span class="sxs-lookup"><span data-stu-id="825ba-156">Closing the Window</span></span>](closing-the-window.md)