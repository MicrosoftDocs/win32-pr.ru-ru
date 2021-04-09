---
title: Настраиваемая рамка окна с помощью DWM
description: В этом разделе показано, как использовать интерфейсы API диспетчер окон рабочего стола (DWM) для создания пользовательских рамок окон для приложения.
ms.assetid: 7f7dc902-40d3-44e9-adc2-05a39c634eb3
keywords:
- Диспетчер окон рабочего стола (DWM), пользовательские рамки окон
- DWM (диспетчер окон рабочего стола), пользовательские рамки окон
- Пользовательские рамки окон
- Удаление стандартных кадров
- Расширение клиентских рамок
- Диспетчер окон рабочего стола (DWM), расширение кадров клиента
- DWM (диспетчер окон рабочего стола), расширение кадров клиента
- Диспетчер окон рабочего стола (DWM), удаление стандартных кадров
- DWM (диспетчер окон рабочего стола), удаление стандартных кадров
- Диспетчер окон рабочего стола (DWM), рисование в расширенных кадрах
- DWM (диспетчер окон рабочего стола), рисование в расширенных кадрах
- Рисование в расширенных кадрах
- проверка нажатия
- Диспетчер окон рабочего стола (DWM), проверка нажатия
- DWM (диспетчер окон рабочего стола), проверка нажатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a27a9b71dd2dd91cb000a352ef039de2a71cd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070589"
---
# <a name="custom-window-frame-using-dwm"></a><span data-ttu-id="62a01-118">Настраиваемая рамка окна с помощью DWM</span><span class="sxs-lookup"><span data-stu-id="62a01-118">Custom Window Frame Using DWM</span></span>

<span data-ttu-id="62a01-119">В этом разделе показано, как использовать интерфейсы API диспетчер окон рабочего стола (DWM) для создания пользовательских рамок окон для приложения.</span><span class="sxs-lookup"><span data-stu-id="62a01-119">This topic demonstrates how to use the Desktop Window Manager (DWM) APIs to create custom window frames for your application.</span></span>

-   [<span data-ttu-id="62a01-120">Введение</span><span class="sxs-lookup"><span data-stu-id="62a01-120">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="62a01-121">Расширение клиентского фрейма</span><span class="sxs-lookup"><span data-stu-id="62a01-121">Extending the Client Frame</span></span>](#extending-the-client-frame)
-   [<span data-ttu-id="62a01-122">Удаление стандартного кадра</span><span class="sxs-lookup"><span data-stu-id="62a01-122">Removing the Standard Frame</span></span>](#removing-the-standard-frame)
-   [<span data-ttu-id="62a01-123">Рисование в окне расширенного фрейма</span><span class="sxs-lookup"><span data-stu-id="62a01-123">Drawing in the Extended Frame Window</span></span>](#drawing-in-the-extended-frame-window)
-   [<span data-ttu-id="62a01-124">Включение проверки нажатия для пользовательского кадра</span><span class="sxs-lookup"><span data-stu-id="62a01-124">Enabling Hit Testing for the Custom Frame</span></span>](#enabling-hit-testing-for-the-custom-frame)
-   [<span data-ttu-id="62a01-125">Приложение а. Процедура примера окна</span><span class="sxs-lookup"><span data-stu-id="62a01-125">Appendix A: Sample Window Procedure</span></span>](#appendix-a-sample-window-procedure)
-   [<span data-ttu-id="62a01-126">Приложение б. Рисование заголовка подписи</span><span class="sxs-lookup"><span data-stu-id="62a01-126">Appendix B: Painting the Caption Title</span></span>](#appendix-b-painting-the-caption-title)
-   [<span data-ttu-id="62a01-127">Приложение в. функция Хиттестнка</span><span class="sxs-lookup"><span data-stu-id="62a01-127">Appendix C: HitTestNCA Function</span></span>](#appendix-c-hittestnca-function)
-   [<span data-ttu-id="62a01-128">См. также</span><span class="sxs-lookup"><span data-stu-id="62a01-128">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="62a01-129">Введение</span><span class="sxs-lookup"><span data-stu-id="62a01-129">Introduction</span></span>

<span data-ttu-id="62a01-130">В Windows Vista и более поздних версиях внешний вид неклиентской области окон приложений (строки заголовка, значка, границы окна и кнопки заголовка) управляется DWM.</span><span class="sxs-lookup"><span data-stu-id="62a01-130">In Windows Vista and later, the appearance of the non-client areas of application windows (the title bar, icon, window border, and caption buttons) is controlled by the DWM.</span></span> <span data-ttu-id="62a01-131">С помощью интерфейсов API DWM можно изменить способ отрисовки кадра окон DWM.</span><span class="sxs-lookup"><span data-stu-id="62a01-131">Using the DWM APIs, you can change the way the DWM renders a window's frame.</span></span>

<span data-ttu-id="62a01-132">Одной из функций API DWM является возможность расширения фрейма приложения в клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="62a01-132">One feature of the DWM APIs is the ability to extend the application frame into the client area.</span></span> <span data-ttu-id="62a01-133">Это позволяет интегрировать элемент пользовательского интерфейса клиента (например, панель инструментов) в рамку, предоставляя пользовательскому интерфейсу возможность управлять более заметным местом в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="62a01-133">This enables you to integrate a client UI element—such as a toolbar—into the frame, giving the UI controls a more prominent place in the application UI.</span></span> <span data-ttu-id="62a01-134">Например, Windows Internet Explorer 7 в Windows Vista интегрирует панель навигации в рамку окна, расширяя верхнюю часть рамки, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="62a01-134">For example, Windows Internet Explorer 7 on Windows Vista integrates the navigation bar into the window frame by extending the top of the frame as shown in the following screen shot.</span></span>

![панель навигации, интегрированная в рамку окна.](images/ie7-extendedborder-boxed.png)

<span data-ttu-id="62a01-136">Возможность расширения рамки окна также позволяет создавать пользовательские фреймы, сохраняя внешний вид окна.</span><span class="sxs-lookup"><span data-stu-id="62a01-136">The ability to extend the window frame also enables you to create custom frames while maintaining the window's look and feel.</span></span> <span data-ttu-id="62a01-137">Например, Microsoft Office Word 2007 рисует кнопку Office и панель быстрого доступа внутри пользовательского фрейма, предоставляя стандартные кнопки сворачивания, развертывания и закрытия, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="62a01-137">For example, Microsoft Office Word 2007 draws the Office button and the Quick Access toolbar inside the custom frame while providing the standard Minimize, Maximize, and Close caption buttons, as shown in the following screen shot.</span></span>

![Кнопка Office и панель быстрого доступа в Word 2007](images/word2007-customborder-boxed.png)

## <a name="extending-the-client-frame"></a><span data-ttu-id="62a01-139">Расширение клиентского фрейма</span><span class="sxs-lookup"><span data-stu-id="62a01-139">Extending the Client Frame</span></span>

<span data-ttu-id="62a01-140">Функциональные возможности расширения рамки в клиентской области предоставляются функцией [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="62a01-140">The functionality to extend the frame into the client area is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="62a01-141">Чтобы расширить рамку, передайте маркер целевого окна вместе со значениями отступов полей в **DwmExtendFrameIntoClientArea**.</span><span class="sxs-lookup"><span data-stu-id="62a01-141">To extend the frame, pass the handle of the target window together with the margin inset values to **DwmExtendFrameIntoClientArea**.</span></span> <span data-ttu-id="62a01-142">Значения отступа полей определяют, насколько далеко можно расширять рамку на четырех сторонах окна.</span><span class="sxs-lookup"><span data-stu-id="62a01-142">The margin inset values determine how far to extend the frame on the four sides of the window.</span></span>

<span data-ttu-id="62a01-143">В следующем коде показано использование [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) для расширения рамки.</span><span class="sxs-lookup"><span data-stu-id="62a01-143">The following code demonstrates the use of [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to extend the frame.</span></span>


```
// Handle the window activation.
if (message == WM_ACTIVATE)
{
    // Extend the frame into the client area.
    MARGINS margins;

    margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
    margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
    margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
    margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

    hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

    if (!SUCCEEDED(hr))
    {
        // Handle the error.
    }

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="62a01-144">Обратите внимание, что расширение Frame выполняется в [**сообщении \_ активации WM**](/windows/desktop/inputdev/wm-activate) , а не в сообщении [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="62a01-144">Note that the frame extension is done within the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message rather than the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="62a01-145">Это гарантирует, что расширение кадра будет правильно обрабатываться, если размер окна по умолчанию и когда он развернут.</span><span class="sxs-lookup"><span data-stu-id="62a01-145">This ensures that frame extension is handled properly when the window is at its default size and when it is maximized.</span></span>

<span data-ttu-id="62a01-146">На следующем рисунке показана стандартная рамка окна (слева) и та же самая Расширенная рамка окна (справа).</span><span class="sxs-lookup"><span data-stu-id="62a01-146">The following image shows a standard window frame (on the left) and the same window frame extended (on the right).</span></span> <span data-ttu-id="62a01-147">Фрейм расширяется с помощью предыдущего примера кода и по умолчанию Microsoft Visual Studio [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) / [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) фон ( \_ окно цвета + 1).</span><span class="sxs-lookup"><span data-stu-id="62a01-147">The frame is extended using the previous code example and the default Microsoft Visual Studio [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)/[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) background (COLOR\_WINDOW +1).</span></span>

![снимок экрана со стандартной (левой) и расширенной рамкой (справа) с белым фоном](images/white-sidebyside.png)

<span data-ttu-id="62a01-149">Визуальное различие между этими двумя окнами очень незаметно.</span><span class="sxs-lookup"><span data-stu-id="62a01-149">The visual difference between these two windows is very subtle.</span></span> <span data-ttu-id="62a01-150">Единственное различие между ними заключается в том, что тонкая черная граница области клиента в окне слева отсутствует в окне справа.</span><span class="sxs-lookup"><span data-stu-id="62a01-150">The only difference between the two is that the thin black line border of the client region in the window on the left is missing from the window on the right.</span></span> <span data-ttu-id="62a01-151">Причиной этой отсутствующей границы является то, что она включена в расширенный кадр, а остальная часть клиентской области — нет.</span><span class="sxs-lookup"><span data-stu-id="62a01-151">The reason for this missing border is that it is incorporated into the extended frame, but the rest of the client area is not.</span></span> <span data-ttu-id="62a01-152">Для отображения расширенных кадров области, лежащие в основе каждой стороны расширенного кадра, должны иметь точечные данные с альфа-значением 0.</span><span class="sxs-lookup"><span data-stu-id="62a01-152">For the extended frames to be visible, the regions underlying each of the extended frame's sides must have pixel data with an alpha value of 0.</span></span> <span data-ttu-id="62a01-153">Черная граница вокруг области клиента содержит данные пикселей, в которых все цветовые значения (красный, зеленый, синий и альфа) имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="62a01-153">The black border around the client region has pixel data in which all color values (red, green, blue, and alpha) are set to 0.</span></span> <span data-ttu-id="62a01-154">В остальной части фона значение альфа не равно 0, поэтому остальная часть расширенного кадра не отображается.</span><span class="sxs-lookup"><span data-stu-id="62a01-154">The rest of the background does not have the alpha value set to 0, so the rest of the extended frame is not visible.</span></span>

<span data-ttu-id="62a01-155">Самый простой способ убедиться в том, что расширенные кадры видимы, — это сделать весь клиентский регион черным.</span><span class="sxs-lookup"><span data-stu-id="62a01-155">The easiest way to ensure that the extended frames are visible is to paint the entire client region black.</span></span> <span data-ttu-id="62a01-156">Для этого инициализируйте элемент *хбрбаккграунд* структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) или [**вндклассекс**](/windows/win32/api/winuser/ns-winuser-wndclassexa) в дескрипторе черной \_ кисти.</span><span class="sxs-lookup"><span data-stu-id="62a01-156">To accomplish this, initialize the *hbrBackground* member of your [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to the handle of the stock BLACK\_BRUSH.</span></span> <span data-ttu-id="62a01-157">На следующем рисунке показан один и тот же стандартный фрейм (слева) и расширенный фрейм (справа), показанные ранее.</span><span class="sxs-lookup"><span data-stu-id="62a01-157">The following image shows the same standard frame (left) and extended frame (right) shown previously.</span></span> <span data-ttu-id="62a01-158">Однако на этот раз для *хбрбаккграунд* ЗАДАН маркер черной кисти, \_ полученный из функции [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="62a01-158">This time, however, *hbrBackground* is set to the BLACK\_BRUSH handle obtained from the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) function.</span></span>

![снимок экрана: Стандартная (слева) и расширенная рамка (справа) с черным фоном](images/standard-extended-sidebyside.png)

## <a name="removing-the-standard-frame"></a><span data-ttu-id="62a01-160">Удаление стандартного кадра</span><span class="sxs-lookup"><span data-stu-id="62a01-160">Removing the Standard Frame</span></span>

<span data-ttu-id="62a01-161">После того как вы расширили фрейм приложения и сделали его видимым, можно удалить стандартный фрейм.</span><span class="sxs-lookup"><span data-stu-id="62a01-161">After you have extended the frame of your application and made it visible, you can remove the standard frame.</span></span> <span data-ttu-id="62a01-162">Удаление стандартного кадра позволяет управлять шириной каждой стороны рамки, а не просто расширением стандартного фрейма.</span><span class="sxs-lookup"><span data-stu-id="62a01-162">Removing the standard frame enables you to control the width of each side of the frame rather than simply extending the standard frame.</span></span>

<span data-ttu-id="62a01-163">Чтобы удалить стандартный фрейм окна, необходимо выполнить обработку сообщения [**WM \_ нккалксизе**](/windows/desktop/winmsg/wm-nccalcsize) , в частности, если его значение *wParam* равно **true** , а возвращаемое значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="62a01-163">To remove the standard window frame, you must handle the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message, specifically when its *wParam* value is **TRUE** and the return value is 0.</span></span> <span data-ttu-id="62a01-164">При этом приложение использует всю область окна в качестве клиентской области, удаляя стандартный фрейм.</span><span class="sxs-lookup"><span data-stu-id="62a01-164">By doing so, your application uses the entire window region as the client area, removing the standard frame.</span></span>

<span data-ttu-id="62a01-165">Результаты обработки сообщения [**WM \_ нккалксизе**](/windows/desktop/winmsg/wm-nccalcsize) не видны, пока не потребуется изменить размер региона клиента.</span><span class="sxs-lookup"><span data-stu-id="62a01-165">The results of handling the [**WM\_NCCALCSIZE**](/windows/desktop/winmsg/wm-nccalcsize) message are not visible until the client region needs to be resized.</span></span> <span data-ttu-id="62a01-166">До этого времени начальное представление окна отображается со стандартным фреймом и расширенными границами.</span><span class="sxs-lookup"><span data-stu-id="62a01-166">Until that time, the initial view of the window appears with the standard frame and extended borders.</span></span> <span data-ttu-id="62a01-167">Чтобы преодолеть это, необходимо либо изменить размер окна, либо выполнить действие, запускающее сообщение **WM \_ нккалксизе** во время создания окна.</span><span class="sxs-lookup"><span data-stu-id="62a01-167">To overcome this, you must either resize your window or perform an action that initiates a **WM\_NCCALCSIZE** message at the time of window creation.</span></span> <span data-ttu-id="62a01-168">Это можно сделать с помощью функции [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) , чтобы переместить окно и изменить его размер.</span><span class="sxs-lookup"><span data-stu-id="62a01-168">This can be accomplished by using the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move your window and resize it.</span></span> <span data-ttu-id="62a01-169">В следующем примере кода демонстрируется вызов **SetWindowPos** , который вызывает отправку сообщения **WM \_ нккалксизе** с помощью атрибутов прямоугольника окна и \_ флага СВП фрамечанжед.</span><span class="sxs-lookup"><span data-stu-id="62a01-169">The following code demonstrates a call to **SetWindowPos** that forces a **WM\_NCCALCSIZE** message to be sent using the current window rectangle attributes and the SWP\_FRAMECHANGED flag.</span></span>


```
// Handle window creation.
if (message == WM_CREATE)
{
    RECT rcClient;
    GetWindowRect(hWnd, &rcClient);

    // Inform the application of the frame change.
    SetWindowPos(hWnd, 
                 NULL, 
                 rcClient.left, rcClient.top,
                 RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                 SWP_FRAMECHANGED);

    fCallDWP = true;
    lRet = 0;
}
```



<span data-ttu-id="62a01-170">На следующем рисунке показан стандартный фрейм (слева) и новый расширенный кадр без стандартного кадра (справа).</span><span class="sxs-lookup"><span data-stu-id="62a01-170">The following image shows the standard frame (left) and the newly extended frame without the standard frame (right).</span></span>

![снимок экрана: Стандартный кадр (слева) и настраиваемый кадр (справа)](images/standard-custom-sidebyside.png)

## <a name="drawing-in-the-extended-frame-window"></a><span data-ttu-id="62a01-172">Рисование в окне расширенного фрейма</span><span class="sxs-lookup"><span data-stu-id="62a01-172">Drawing in the Extended Frame Window</span></span>

<span data-ttu-id="62a01-173">При удалении стандартного кадра теряется автоматическое рисование значка и названия приложения.</span><span class="sxs-lookup"><span data-stu-id="62a01-173">By removing the standard frame, you lose the automatic drawing of the application icon and title.</span></span> <span data-ttu-id="62a01-174">Чтобы добавить их обратно в приложение, необходимо нарисовать их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="62a01-174">To add these back to your application, you must draw them yourself.</span></span> <span data-ttu-id="62a01-175">Для этого сначала просмотрите изменения, которые произошли в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="62a01-175">To do this, first look at the change that has occurred to your client area.</span></span>

<span data-ttu-id="62a01-176">После удаления стандартного кадра клиентская область теперь состоит из всего окна, включая расширенный кадр.</span><span class="sxs-lookup"><span data-stu-id="62a01-176">With the removal of the standard frame, your client area now consists of the entire window, including the extended frame.</span></span> <span data-ttu-id="62a01-177">Сюда входит область, в которой рисуются кнопки заголовка.</span><span class="sxs-lookup"><span data-stu-id="62a01-177">This includes the region where the caption buttons are drawn.</span></span> <span data-ttu-id="62a01-178">В следующем параллельном сравнении клиентская область для стандартного кадра и пользовательского расширенного кадра выделяется красным цветом.</span><span class="sxs-lookup"><span data-stu-id="62a01-178">In the following side-by-side comparison, the client area for both the standard frame and the custom extended frame is highlighted in red.</span></span> <span data-ttu-id="62a01-179">Область клиента для стандартного окна фрейма (слева) — это черная область.</span><span class="sxs-lookup"><span data-stu-id="62a01-179">The client area for the standard frame window (left) is the black region.</span></span> <span data-ttu-id="62a01-180">В расширенном окне фрейма (справа) клиентская область — это все окно.</span><span class="sxs-lookup"><span data-stu-id="62a01-180">On the extended frame window (right), the client area is the entire window.</span></span>

![снимок экрана с красной выделенной областью клиента на стандартном и настраиваемом кадре](images/clientarea-sidebyside.png)

<span data-ttu-id="62a01-182">Так как все окно является клиентской областью, можно просто нарисовать нужные объекты в расширенном кадре.</span><span class="sxs-lookup"><span data-stu-id="62a01-182">Because the entire window is your client area, you can simply draw what you want in the extended frame.</span></span> <span data-ttu-id="62a01-183">Чтобы добавить заголовок в приложение, просто выведите текст в соответствующем регионе.</span><span class="sxs-lookup"><span data-stu-id="62a01-183">To add a title to your application, just draw text in the appropriate region.</span></span> <span data-ttu-id="62a01-184">На следующем рисунке показан текст темы, нарисованный в пользовательском фрейме заголовка.</span><span class="sxs-lookup"><span data-stu-id="62a01-184">The following image shows themed text drawn on the custom caption frame.</span></span> <span data-ttu-id="62a01-185">Заголовок рисуется с помощью функции [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="62a01-185">The title is drawn using the [**DrawThemeTextEx**](/windows/win32/api/uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="62a01-186">Чтобы просмотреть код, рисующий заголовок, см. [приложение б. закраска заголовка](#appendix-b-painting-the-caption-title).</span><span class="sxs-lookup"><span data-stu-id="62a01-186">To view the code that paints the title, see [Appendix B: Painting the Caption Title](#appendix-b-painting-the-caption-title).</span></span>

![снимок экрана с пользовательской рамкой с заголовком](images/custom-caption-title.png)

> [!Note]  
> <span data-ttu-id="62a01-188">При рисовании в пользовательском фрейме Будьте внимательны при размещении элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="62a01-188">When drawing in your custom frame, be careful when placing UI controls.</span></span> <span data-ttu-id="62a01-189">Так как все окно является регионом клиента, необходимо настроить размещение элементов управления пользовательского интерфейса для каждой ширины кадра, если они не должны отображаться в или в расширенном фрейме.</span><span class="sxs-lookup"><span data-stu-id="62a01-189">Because the entire window is your client region, you must adjust your UI control placement for each frame width if you do not want them to appear on or in the extended frame.</span></span>

 

## <a name="enabling-hit-testing-for-the-custom-frame"></a><span data-ttu-id="62a01-190">Включение проверки нажатия для пользовательского кадра</span><span class="sxs-lookup"><span data-stu-id="62a01-190">Enabling Hit Testing for the Custom Frame</span></span>

<span data-ttu-id="62a01-191">Побочным результатом удаления стандартного фрейма является утрата поведения изменения размера и перемещения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62a01-191">A side effect of removing the standard frame is the loss of the default resizing and moving behavior.</span></span> <span data-ttu-id="62a01-192">Чтобы приложение правильно эмулировать поведение стандартного окна, необходимо реализовать логику обработки проверки нажатия кнопки "заголовок" и изменения размера или перемещения кадра.</span><span class="sxs-lookup"><span data-stu-id="62a01-192">For your application to properly emulate standard window behavior, you will need to implement logic to handle caption button hit testing and frame resizing/moving.</span></span>

<span data-ttu-id="62a01-193">Для проверки нажатия кнопки субтитров DWM предоставляет функцию [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="62a01-193">For caption button hit testing, DWM provides the [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="62a01-194">Для правильной проверки нажатия кнопок субтитров в сценариях с пользовательскими кадрами сообщения должны быть передаваться в **двмдефвиндовпрок** для обработки.</span><span class="sxs-lookup"><span data-stu-id="62a01-194">To properly hit test the caption buttons in custom frame scenarios, messages should first be passed to **DwmDefWindowProc** for handling.</span></span> <span data-ttu-id="62a01-195">**Двмдефвиндовпрок** возвращает **значение true** , если сообщение обрабатывается, и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="62a01-195">**DwmDefWindowProc** returns **TRUE** if a message is handled and **FALSE** if it is not.</span></span> <span data-ttu-id="62a01-196">Если сообщение не обрабатывается **двмдефвиндовпрок**, приложение должно обработать само сообщение или передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="62a01-196">If the message is not handled by **DwmDefWindowProc**, your application should handle the message itself or pass the message onto [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="62a01-197">Для изменения размера и перемещения фрейма приложение должно предоставить логику проверки попадания и обработку сообщений проверки нажатия кадра.</span><span class="sxs-lookup"><span data-stu-id="62a01-197">For frame resizing and moving, your application must provide the hit testing logic and handle frame hit test messages.</span></span> <span data-ttu-id="62a01-198">Сообщения проверки нажатия фрейма отправляются вам через сообщение [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , даже если приложение создает пользовательский фрейм без стандартного кадра.</span><span class="sxs-lookup"><span data-stu-id="62a01-198">Frame hit test messages are sent to you through the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message, even if your application creates a custom frame without the standard frame.</span></span> <span data-ttu-id="62a01-199">Следующий код демонстрирует обработку сообщения **WM \_ нчиттест** , когда [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) не обрабатывает его.</span><span class="sxs-lookup"><span data-stu-id="62a01-199">The following code demonstrates handling the **WM\_NCHITTEST** message when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle it.</span></span> <span data-ttu-id="62a01-200">Код вызываемой `HitTestNCA` функции см. в [приложении C: хиттестнка Function](#appendix-c-hittestnca-function).</span><span class="sxs-lookup"><span data-stu-id="62a01-200">To see the code of the called `HitTestNCA` function, see [Appendix C: HitTestNCA Function](#appendix-c-hittestnca-function).</span></span>


```
// Handle hit testing in the NCA if not handled by DwmDefWindowProc.
if ((message == WM_NCHITTEST) && (lRet == 0))
{
    lRet = HitTestNCA(hWnd, wParam, lParam);

    if (lRet != HTNOWHERE)
    {
        fCallDWP = false;
    }
}
```



## <a name="appendix-a-sample-window-procedure"></a><span data-ttu-id="62a01-201">Приложение а. Процедура примера окна</span><span class="sxs-lookup"><span data-stu-id="62a01-201">Appendix A: Sample Window Procedure</span></span>

<span data-ttu-id="62a01-202">В следующем примере кода демонстрируется процедура окна и вспомогательные функции, которые используются для создания пользовательского приложения с фреймами.</span><span class="sxs-lookup"><span data-stu-id="62a01-202">The following code sample demonstrates a window procedure and its supporting worker functions used to create a custom frame application.</span></span>


```
//
//  Main WinProc.
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    bool fCallDWP = true;
    BOOL fDwmEnabled = FALSE;
    LRESULT lRet = 0;
    HRESULT hr = S_OK;

    // Winproc worker for custom frame issues.
    hr = DwmIsCompositionEnabled(&fDwmEnabled);
    if (SUCCEEDED(hr))
    {
        lRet = CustomCaptionProc(hWnd, message, wParam, lParam, &fCallDWP);
    }

    // Winproc worker for the rest of the application.
    if (fCallDWP)
    {
        lRet = AppWinProc(hWnd, message, wParam, lParam);
    }
    return lRet;
}

//
// Message handler for handling the custom caption messages.
//
LRESULT CustomCaptionProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam, bool* pfCallDWP)
{
    LRESULT lRet = 0;
    HRESULT hr = S_OK;
    bool fCallDWP = true; // Pass on to DefWindowProc?

    fCallDWP = !DwmDefWindowProc(hWnd, message, wParam, lParam, &lRet);

    // Handle window creation.
    if (message == WM_CREATE)
    {
        RECT rcClient;
        GetWindowRect(hWnd, &rcClient);

        // Inform application of the frame change.
        SetWindowPos(hWnd, 
                     NULL, 
                     rcClient.left, rcClient.top,
                     RECTWIDTH(rcClient), RECTHEIGHT(rcClient),
                     SWP_FRAMECHANGED);

        fCallDWP = true;
        lRet = 0;
    }

    // Handle window activation.
    if (message == WM_ACTIVATE)
    {
        // Extend the frame into the client area.
        MARGINS margins;

        margins.cxLeftWidth = LEFTEXTENDWIDTH;      // 8
        margins.cxRightWidth = RIGHTEXTENDWIDTH;    // 8
        margins.cyBottomHeight = BOTTOMEXTENDWIDTH; // 20
        margins.cyTopHeight = TOPEXTENDWIDTH;       // 27

        hr = DwmExtendFrameIntoClientArea(hWnd, &margins);

        if (!SUCCEEDED(hr))
        {
            // Handle error.
        }

        fCallDWP = true;
        lRet = 0;
    }

    if (message == WM_PAINT)
    {
        HDC hdc;
        {
            PAINTSTRUCT ps;
            hdc = BeginPaint(hWnd, &ps);
            PaintCustomCaption(hWnd, hdc);
            EndPaint(hWnd, &ps);
        }

        fCallDWP = true;
        lRet = 0;
    }

    // Handle the non-client size message.
    if ((message == WM_NCCALCSIZE) && (wParam == TRUE))
    {
        // Calculate new NCCALCSIZE_PARAMS based on custom NCA inset.
        NCCALCSIZE_PARAMS *pncsp = reinterpret_cast<NCCALCSIZE_PARAMS*>(lParam);

        pncsp->rgrc[0].left   = pncsp->rgrc[0].left   + 0;
        pncsp->rgrc[0].top    = pncsp->rgrc[0].top    + 0;
        pncsp->rgrc[0].right  = pncsp->rgrc[0].right  - 0;
        pncsp->rgrc[0].bottom = pncsp->rgrc[0].bottom - 0;

        lRet = 0;
        
        // No need to pass the message on to the DefWindowProc.
        fCallDWP = false;
    }

    // Handle hit testing in the NCA if not handled by DwmDefWindowProc.
    if ((message == WM_NCHITTEST) && (lRet == 0))
    {
        lRet = HitTestNCA(hWnd, wParam, lParam);

        if (lRet != HTNOWHERE)
        {
            fCallDWP = false;
        }
    }

    *pfCallDWP = fCallDWP;

    return lRet;
}

//
// Message handler for the application.
//
LRESULT AppWinProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    HRESULT hr; 
    LRESULT result = 0;

    switch (message)
    {
        case WM_CREATE:
            {}
            break;
        case WM_COMMAND:
            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            // Parse the menu selections:
            switch (wmId)
            {
                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            {
                hdc = BeginPaint(hWnd, &ps);
                PaintCustomCaption(hWnd, hdc);
                
                // Add any drawing code here...
    
                EndPaint(hWnd, &ps);
            }
            break;
        case WM_DESTROY:
            PostQuitMessage(0);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



## <a name="appendix-b-painting-the-caption-title"></a><span data-ttu-id="62a01-203">Приложение б. Рисование заголовка подписи</span><span class="sxs-lookup"><span data-stu-id="62a01-203">Appendix B: Painting the Caption Title</span></span>

<span data-ttu-id="62a01-204">В следующем коде показано, как закрасить заголовок заголовка в расширенном кадре.</span><span class="sxs-lookup"><span data-stu-id="62a01-204">The following code demonstrates how to paint a caption title on the extended frame.</span></span> <span data-ttu-id="62a01-205">Эта функция должна вызываться из вызовов [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="62a01-205">This function must be called from within the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) calls.</span></span>


```
// Paint the title on the custom frame.
void PaintCustomCaption(HWND hWnd, HDC hdc)
{
    RECT rcClient;
    GetClientRect(hWnd, &rcClient);

    HTHEME hTheme = OpenThemeData(NULL, L"CompositedWindow::Window");
    if (hTheme)
    {
        HDC hdcPaint = CreateCompatibleDC(hdc);
        if (hdcPaint)
        {
            int cx = RECTWIDTH(rcClient);
            int cy = RECTHEIGHT(rcClient);

            // Define the BITMAPINFO structure used to draw text.
            // Note that biHeight is negative. This is done because
            // DrawThemeTextEx() needs the bitmap to be in top-to-bottom
            // order.
            BITMAPINFO dib = { 0 };
            dib.bmiHeader.biSize            = sizeof(BITMAPINFOHEADER);
            dib.bmiHeader.biWidth           = cx;
            dib.bmiHeader.biHeight          = -cy;
            dib.bmiHeader.biPlanes          = 1;
            dib.bmiHeader.biBitCount        = BIT_COUNT;
            dib.bmiHeader.biCompression     = BI_RGB;

            HBITMAP hbm = CreateDIBSection(hdc, &dib, DIB_RGB_COLORS, NULL, NULL, 0);
            if (hbm)
            {
                HBITMAP hbmOld = (HBITMAP)SelectObject(hdcPaint, hbm);

                // Setup the theme drawing options.
                DTTOPTS DttOpts = {sizeof(DTTOPTS)};
                DttOpts.dwFlags = DTT_COMPOSITED | DTT_GLOWSIZE;
                DttOpts.iGlowSize = 15;

                // Select a font.
                LOGFONT lgFont;
                HFONT hFontOld = NULL;
                if (SUCCEEDED(GetThemeSysFont(hTheme, TMT_CAPTIONFONT, &lgFont)))
                {
                    HFONT hFont = CreateFontIndirect(&lgFont);
                    hFontOld = (HFONT) SelectObject(hdcPaint, hFont);
                }

                // Draw the title.
                RECT rcPaint = rcClient;
                rcPaint.top += 8;
                rcPaint.right -= 125;
                rcPaint.left += 8;
                rcPaint.bottom = 50;
                DrawThemeTextEx(hTheme, 
                                hdcPaint, 
                                0, 0, 
                                szTitle, 
                                -1, 
                                DT_LEFT | DT_WORD_ELLIPSIS, 
                                &rcPaint, 
                                &DttOpts);

                // Blit text to the frame.
                BitBlt(hdc, 0, 0, cx, cy, hdcPaint, 0, 0, SRCCOPY);

                SelectObject(hdcPaint, hbmOld);
                if (hFontOld)
                {
                    SelectObject(hdcPaint, hFontOld);
                }
                DeleteObject(hbm);
            }
            DeleteDC(hdcPaint);
        }
        CloseThemeData(hTheme);
    }
}
```



## <a name="appendix-c-hittestnca-function"></a><span data-ttu-id="62a01-206">Приложение в. функция Хиттестнка</span><span class="sxs-lookup"><span data-stu-id="62a01-206">Appendix C: HitTestNCA Function</span></span>

<span data-ttu-id="62a01-207">В следующем коде показана `HitTestNCA` функция, используемая при [проверке нажатия для пользовательского фрейма](#enabling-hit-testing-for-the-custom-frame).</span><span class="sxs-lookup"><span data-stu-id="62a01-207">The following code shows the `HitTestNCA` function used in [Enabling Hit Testing for the Custom Frame](#enabling-hit-testing-for-the-custom-frame).</span></span> <span data-ttu-id="62a01-208">Эта функция обрабатывает логику проверки попадания для [**WM \_ нчиттест**](/windows/desktop/inputdev/wm-nchittest) , когда [**двмдефвиндовпрок**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) не обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="62a01-208">This function handles the hit testing logic for the [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) when [**DwmDefWindowProc**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc) does not handle the message.</span></span>


```
// Hit test the frame for resizing and moving.
LRESULT HitTestNCA(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    // Get the point coordinates for the hit test.
    POINT ptMouse = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam)};

    // Get the window rectangle.
    RECT rcWindow;
    GetWindowRect(hWnd, &rcWindow);

    // Get the frame rectangle, adjusted for the style without a caption.
    RECT rcFrame = { 0 };
    AdjustWindowRectEx(&rcFrame, WS_OVERLAPPEDWINDOW & ~WS_CAPTION, FALSE, NULL);

    // Determine if the hit test is for resizing. Default middle (1,1).
    USHORT uRow = 1;
    USHORT uCol = 1;
    bool fOnResizeBorder = false;

    // Determine if the point is at the top or bottom of the window.
    if (ptMouse.y >= rcWindow.top && ptMouse.y < rcWindow.top + TOPEXTENDWIDTH)
    {
        fOnResizeBorder = (ptMouse.y < (rcWindow.top - rcFrame.top));
        uRow = 0;
    }
    else if (ptMouse.y < rcWindow.bottom && ptMouse.y >= rcWindow.bottom - BOTTOMEXTENDWIDTH)
    {
        uRow = 2;
    }

    // Determine if the point is at the left or right of the window.
    if (ptMouse.x >= rcWindow.left && ptMouse.x < rcWindow.left + LEFTEXTENDWIDTH)
    {
        uCol = 0; // left side
    }
    else if (ptMouse.x < rcWindow.right && ptMouse.x >= rcWindow.right - RIGHTEXTENDWIDTH)
    {
        uCol = 2; // right side
    }

    // Hit test (HTTOPLEFT, ... HTBOTTOMRIGHT)
    LRESULT hitTests[3][3] = 
    {
        { HTTOPLEFT,    fOnResizeBorder ? HTTOP : HTCAPTION,    HTTOPRIGHT },
        { HTLEFT,       HTNOWHERE,     HTRIGHT },
        { HTBOTTOMLEFT, HTBOTTOM, HTBOTTOMRIGHT },
    };

    return hitTests[uRow][uCol];
}
```



## <a name="related-topics"></a><span data-ttu-id="62a01-209">См. также</span><span class="sxs-lookup"><span data-stu-id="62a01-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62a01-210">Общие сведения о диспетчере окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="62a01-210">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> </dl>

 

 