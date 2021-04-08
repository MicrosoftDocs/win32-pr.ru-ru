---
title: Устранение неполадок приложений
description: В этом разделе приводятся решения распространенных проблем.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch, устранение неполадок приложений
- Windows Touch, отклонение Palm
- отклонение Palm
- Windows Touch, поддержка прежних версий
- Устранение неполадок Windows Touch
- инерция, устранение неполадок приложений
- манипуляции, устранение неполадок приложений
- жесты, устранение неполадок приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000034"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="11326-111">Устранение неполадок приложений</span><span class="sxs-lookup"><span data-stu-id="11326-111">Troubleshooting Applications</span></span>

<span data-ttu-id="11326-112">В этом разделе приводятся решения распространенных проблем.</span><span class="sxs-lookup"><span data-stu-id="11326-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="11326-113">Общие действия по устранению неполадок</span><span class="sxs-lookup"><span data-stu-id="11326-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-114">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-114">Issue</span></span>    | <span data-ttu-id="11326-115">Я использую Windows Server 2008, а функции касания Windows не работают.</span><span class="sxs-lookup"><span data-stu-id="11326-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="11326-116">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-116">Cause</span></span>    | <span data-ttu-id="11326-117">Вы не включили возможности рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="11326-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="11326-118">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-118">Solution</span></span> | <span data-ttu-id="11326-119">Откройте средство администрирования диспетчер сервера: нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем щелкните **Диспетчер сервера**.</span><span class="sxs-lookup"><span data-stu-id="11326-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="11326-120">Щелкните элемент **компоненты** в левом столбце.</span><span class="sxs-lookup"><span data-stu-id="11326-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="11326-121">Щелкните **Добавить компоненты** в разделе **компоненты** .</span><span class="sxs-lookup"><span data-stu-id="11326-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="11326-122">Выберите **возможности рабочего стола**, нажмите кнопку **Далее**, а затем — **установить**.</span><span class="sxs-lookup"><span data-stu-id="11326-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-123">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-123">Issue</span></span>    | <span data-ttu-id="11326-124">При быстром перемещении пальца по моему приложению появляется стрелка, а жест или манипуляция не регистрируются правильно.</span><span class="sxs-lookup"><span data-stu-id="11326-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="11326-125">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-125">Cause</span></span>    | <span data-ttu-id="11326-126">Включение жестов, если оно не требуется.</span><span class="sxs-lookup"><span data-stu-id="11326-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="11326-127">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-127">Solution</span></span> | <span data-ttu-id="11326-128">Вы включили жесты, если хотите отключить их.</span><span class="sxs-lookup"><span data-stu-id="11326-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="11326-129">Сведения об отключении жестов пером см. в статье [устаревшая поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11326-130">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-130">Issue</span></span></td>
<td><span data-ttu-id="11326-131">Не удается различить входные данные мыши и сенсорный ввод Windows.</span><span class="sxs-lookup"><span data-stu-id="11326-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11326-132">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-132">Cause</span></span></td>
<td><span data-ttu-id="11326-133">Windows создает сообщения мыши для поддержки устаревшей версии, когда пользователь щелкает на экране.</span><span class="sxs-lookup"><span data-stu-id="11326-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11326-134">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-134">Solution</span></span></td>
<td><span data-ttu-id="11326-135">Вы можете вызвать <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">жетмессажеекстраинфо</a> для <strong>WM_LBUTTONDOWN</strong> и <strong>WM_LBUTTONUP</strong> сообщений, чтобы определить источник.</span><span class="sxs-lookup"><span data-stu-id="11326-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="11326-136">В следующем коде показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="11326-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11326-137">C++</span><span class="sxs-lookup"><span data-stu-id="11326-137">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-138">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-138">Issue</span></span>    | <span data-ttu-id="11326-139">Разделы справки запускать приложения Microsoft Пикселсенсе в Windows 7?</span><span class="sxs-lookup"><span data-stu-id="11326-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="11326-140">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-140">Cause</span></span>    | <span data-ttu-id="11326-141">Windows Touch и Microsoft Пикселсенсе несовместимы.</span><span class="sxs-lookup"><span data-stu-id="11326-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="11326-142">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-142">Solution</span></span> | <span data-ttu-id="11326-143">Необходимо ориентироваться на платформу Windows 7 или платформу Microsoft Пикселсенсе.</span><span class="sxs-lookup"><span data-stu-id="11326-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="11326-144">Устранение неполадок манипуляций и инерции</span><span class="sxs-lookup"><span data-stu-id="11326-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-145">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-145">Issue</span></span>    | <span data-ttu-id="11326-146">Мое приложение заморозить без причины.</span><span class="sxs-lookup"><span data-stu-id="11326-146">My application is freezing for no reason.</span></span> <span data-ttu-id="11326-147">Я получаю нарушения прав доступа при инициализации интерфейсов объектов.</span><span class="sxs-lookup"><span data-stu-id="11326-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="11326-148">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-148">Cause</span></span>    | <span data-ttu-id="11326-149">Отсутствие вызова **CoInitialize** при использовании интерфейсов [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) или [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="11326-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="11326-150">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-150">Solution</span></span> | <span data-ttu-id="11326-151">Это может быть вызвано созданием объектов модели COM Windows Touch без вызова CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="11326-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="11326-152">Это происходит иногда при преобразовании проектов из использования жестов в использование манипуляций или интерфейсов инерции.</span><span class="sxs-lookup"><span data-stu-id="11326-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-153">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-153">Issue</span></span>    | <span data-ttu-id="11326-154">При переводе объект неверно вращается.</span><span class="sxs-lookup"><span data-stu-id="11326-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="11326-155">Вращение с одним пальцем работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="11326-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="11326-156">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-156">Cause</span></span>    | <span data-ttu-id="11326-157">Неправильное задание сводных значений для объекта.</span><span class="sxs-lookup"><span data-stu-id="11326-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="11326-158">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-158">Solution</span></span> | <span data-ttu-id="11326-159">Вы не настраиваете точки вращения для манипуляции правильно.</span><span class="sxs-lookup"><span data-stu-id="11326-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="11326-160">Задайте свойства [**пивотпоинткс**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) и [**пивотпоинти**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) в центре объекта или точки, вокруг которых нужно выполнить поворот, и задайте для свойства [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) значение Радиус объекта.</span><span class="sxs-lookup"><span data-stu-id="11326-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="11326-161">Устранение неполадок сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="11326-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-162">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-162">Issue</span></span>    | <span data-ttu-id="11326-163">После того как я обработал сообщение [**WM \_ Touch**](wm-touchdown.md) , я прекращаю получать отзывы о границе.</span><span class="sxs-lookup"><span data-stu-id="11326-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="11326-164">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-164">Cause</span></span>    | <span data-ttu-id="11326-165">Использование сообщения [**WM \_ Touch**](wm-touchdown.md) без его обработки.</span><span class="sxs-lookup"><span data-stu-id="11326-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="11326-166">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-166">Solution</span></span> | <span data-ttu-id="11326-167">Возможно, вы используете Windows Touch, не пересылая его в **дефвиндовпрок**, что приведет к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="11326-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="11326-168">Чтобы получить дополнительные сведения о правильной обработке сообщений [**WM \_ Touch**](wm-touchdown.md) , проверьте [Начало работы с помощью сенсорных сообщений Windows](getting-started-with-multi-touch-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11326-169">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-169">Issue</span></span></td>
<td><span data-ttu-id="11326-170">Я рассматриваю Windows. h, но по-прежнему говорит, что <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> не определена.</span><span class="sxs-lookup"><span data-stu-id="11326-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11326-171">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-171">Cause</span></span></td>
<td><span data-ttu-id="11326-172">Неправильная версия Windows в Targetver. h.</span><span class="sxs-lookup"><span data-stu-id="11326-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11326-173">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-173">Solution</span></span></td>
<td><span data-ttu-id="11326-174">В проекте не задана правильная версия Windows.</span><span class="sxs-lookup"><span data-stu-id="11326-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="11326-175">Следующий код иллюстрирует правильную установку версий Windows для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11326-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11326-176">C++</span><span class="sxs-lookup"><span data-stu-id="11326-176">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11326-177">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-177">Issue</span></span></td>
<td><span data-ttu-id="11326-178">Недопустимые координаты x-координат и координаты y сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="11326-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="11326-179">Они имеют либо большие значения, чем ожидания, либо отрицательные значения.</span><span class="sxs-lookup"><span data-stu-id="11326-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11326-180">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-180">Cause</span></span></td>
<td><span data-ttu-id="11326-181">Может потребоваться преобразовать сенсорные точки в пиксели или преобразовать экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="11326-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11326-182">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-182">Solution</span></span></td>
<td><span data-ttu-id="11326-183">Убедитесь, что вызывается <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> и <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>скринтоклиент</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="11326-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="11326-184">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="11326-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11326-185">C++</span><span class="sxs-lookup"><span data-stu-id="11326-185">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="11326-186">Чтобы использовать функцию <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>скринтоклиент</strong></a> , в приложении должна быть поддержка высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="11326-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="11326-187">Дополнительные сведения о поддержке высокого DPI см. в разделе о <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">высоком уровне dpi</a> в MSDN.</span><span class="sxs-lookup"><span data-stu-id="11326-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-188">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-188">Issue</span></span>    | <span data-ttu-id="11326-189">Я не вижу сообщений [**WM \_ Touch**](wm-touchdown.md) , но я знаю, что касание Windows работает, так как я вижу сообщения [**\_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="11326-190">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-190">Cause</span></span>    | <span data-ttu-id="11326-191">Отсутствует вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="11326-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="11326-192">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-192">Solution</span></span> | <span data-ttu-id="11326-193">[**WM \_ Сообщения жестов сенсорного ввода**](wm-touchdown.md) и [**WM \_**](wm-gesture.md) являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="11326-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="11326-194">Если не вызвать [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), будут получены только сообщения **\_ жестов WM** .</span><span class="sxs-lookup"><span data-stu-id="11326-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-195">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-195">Issue</span></span>    | <span data-ttu-id="11326-196">Я получаю небольшие задержки со времени, когда я касался пальца до получения входных данных в приложении.</span><span class="sxs-lookup"><span data-stu-id="11326-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="11326-197">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-197">Cause</span></span>    | <span data-ttu-id="11326-198">Отклонение Palm вызывает задержки во входных данных.</span><span class="sxs-lookup"><span data-stu-id="11326-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="11326-199">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-199">Solution</span></span> | <span data-ttu-id="11326-200">Если **ТВФ \_ вантпалм** установлен в вызовах [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), то отклонение Palm включено.</span><span class="sxs-lookup"><span data-stu-id="11326-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="11326-201">Это вызывает небольшую задержку (100 мс), пока программное обеспечение проверит, поступает ли вход с помощью пальца, пера или карманного компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="11326-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="11326-202">Отключите отклонение Palm, вызвав **регистертаучвиндов** с установленным флагом **ТВФ \_ вантпалм** .</span><span class="sxs-lookup"><span data-stu-id="11326-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="11326-203">Устранение неполадок сенсорных жестов Windows</span><span class="sxs-lookup"><span data-stu-id="11326-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-204">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-204">Issue</span></span>    | <span data-ttu-id="11326-205">После обработки сообщения [**\_ жеста WM**](wm-gesture.md) я прекращаю получать отзывы о границе.</span><span class="sxs-lookup"><span data-stu-id="11326-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="11326-206">Или жест, который работал ранее, сейчас не работает.</span><span class="sxs-lookup"><span data-stu-id="11326-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="11326-207">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-207">Cause</span></span>    | <span data-ttu-id="11326-208">Использование сообщения [**\_ жеста WM**](wm-gesture.md) без его обработки.</span><span class="sxs-lookup"><span data-stu-id="11326-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="11326-209">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-209">Solution</span></span> | <span data-ttu-id="11326-210">Возможно, вы используете Windows Touch, не пересылая его в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca), что приведет к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="11326-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="11326-211">Дополнительные сведения о правильной обработке сообщений [**\_ жестов WM**](wm-gesture.md) см. в [Начало работы с помощью жестов Windows](getting-started-with-multi-touch-gestures.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-212">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-212">Issue</span></span>    | <span data-ttu-id="11326-213">Я не вижу сообщения [**\_ жестов WM**](wm-gesture.md) , но я знаю, что касание Windows работает, так как я вижу сообщения [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="11326-214">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-214">Cause</span></span>    | <span data-ttu-id="11326-215">Вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="11326-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="11326-216">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-216">Solution</span></span> | <span data-ttu-id="11326-217">[**WM \_ Сообщения жестов сенсорного ввода**](wm-touchdown.md) и [**WM \_**](wm-gesture.md) являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="11326-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="11326-218">При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы не получите сообщения **\_ жестов WM** .</span><span class="sxs-lookup"><span data-stu-id="11326-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11326-219">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-219">Issue</span></span></td>
<td><span data-ttu-id="11326-220">Я вижу не все жесты, которые мне хотелось видеть.</span><span class="sxs-lookup"><span data-stu-id="11326-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="11326-221">Например, я вижу жесты с идентификатором <strong>GID_PAN</strong> но не <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="11326-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11326-222">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-222">Cause</span></span></td>
<td><span data-ttu-id="11326-223">Некоторые жесты, такие как жест поворота, по умолчанию отключены.</span><span class="sxs-lookup"><span data-stu-id="11326-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11326-224">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-224">Solution</span></span></td>
<td><span data-ttu-id="11326-225">Необходимо вызвать <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>сетжестуреконфиг</strong></a> при получении сообщения <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> , как описано в справочнике по <strong>WM_GESTURENOTIFY</strong> , или необходимо добавить обработчик для сообщения <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="11326-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="11326-226">В следующем коде показано, как можно реализовать обработчик, чтобы обеспечить поддержку вращения.</span><span class="sxs-lookup"><span data-stu-id="11326-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11326-227">C++</span><span class="sxs-lookup"><span data-stu-id="11326-227">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="11326-228">Дополнительные примеры типичных конфигураций жестов см. в разделе <strong>сетжестуреконфиг</strong>.</span><span class="sxs-lookup"><span data-stu-id="11326-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-229">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-229">Issue</span></span>    | <span data-ttu-id="11326-230">Пользовательские полосы прокрутки в приложении не прокручивается при выполнении жеста панорамирования.</span><span class="sxs-lookup"><span data-stu-id="11326-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="11326-231">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-231">Cause</span></span>    | <span data-ttu-id="11326-232">Отсутствуют обработчики для правильных \_ \* сообщений прокрутки WM.</span><span class="sxs-lookup"><span data-stu-id="11326-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="11326-233">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-233">Solution</span></span> | <span data-ttu-id="11326-234">Вы не обрабатываете все \_ \* сообщения прокрутки WM в настраиваемых полосах прокрутки.</span><span class="sxs-lookup"><span data-stu-id="11326-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="11326-235">Рекомендуется работать с сообщением [**\_ жеста WM**](wm-gesture.md) вместо того, чтобы хранить пользовательские функции прокрутки с помощью устаревшей поддержки.</span><span class="sxs-lookup"><span data-stu-id="11326-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="11326-236">Необходимо поддерживать сообщения, как описано в разделе [поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="11326-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11326-237">Проблема</span><span class="sxs-lookup"><span data-stu-id="11326-237">Issue</span></span>    | <span data-ttu-id="11326-238">Я получаю задержки для жестов.</span><span class="sxs-lookup"><span data-stu-id="11326-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="11326-239">Причина</span><span class="sxs-lookup"><span data-stu-id="11326-239">Cause</span></span>    | <span data-ttu-id="11326-240">Жесты могут вызывать задержки для жестов.</span><span class="sxs-lookup"><span data-stu-id="11326-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="11326-241">Решение</span><span class="sxs-lookup"><span data-stu-id="11326-241">Solution</span></span> | <span data-ttu-id="11326-242">Жесты могут вызвать задержки в течение времени, затрачиваемого приложением на получение сообщений [**\_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="11326-243">Сведения об отключении жестов см. в статье [устаревшая поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="11326-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="11326-244">См. также</span><span class="sxs-lookup"><span data-stu-id="11326-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11326-245">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="11326-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 