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
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443154"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="30fa6-111">Устранение неполадок приложений</span><span class="sxs-lookup"><span data-stu-id="30fa6-111">Troubleshooting Applications</span></span>

<span data-ttu-id="30fa6-112">В этом разделе приводятся решения распространенных проблем.</span><span class="sxs-lookup"><span data-stu-id="30fa6-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="30fa6-113">Общие действия по устранению неполадок</span><span class="sxs-lookup"><span data-stu-id="30fa6-113">General Troubleshooting</span></span>



| <span data-ttu-id="30fa6-114">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-114">Category</span></span> | <span data-ttu-id="30fa6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-116">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-116">Issue</span></span>    | <span data-ttu-id="30fa6-117">Я использую Windows Server 2008, а функции касания Windows не работают.</span><span class="sxs-lookup"><span data-stu-id="30fa6-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="30fa6-118">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-118">Cause</span></span>    | <span data-ttu-id="30fa6-119">Вы не включили возможности рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="30fa6-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="30fa6-120">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-120">Solution</span></span> | <span data-ttu-id="30fa6-121">Откройте средство администрирования диспетчер сервера: нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем щелкните **Диспетчер сервера**.</span><span class="sxs-lookup"><span data-stu-id="30fa6-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="30fa6-122">Щелкните элемент **компоненты** в левом столбце.</span><span class="sxs-lookup"><span data-stu-id="30fa6-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="30fa6-123">Щелкните **Добавить компоненты** в разделе **компоненты** .</span><span class="sxs-lookup"><span data-stu-id="30fa6-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="30fa6-124">Выберите **возможности рабочего стола**, нажмите кнопку **Далее**, а затем — **установить**.</span><span class="sxs-lookup"><span data-stu-id="30fa6-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="30fa6-125">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-125">Category</span></span> | <span data-ttu-id="30fa6-126">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-127">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-127">Issue</span></span>    | <span data-ttu-id="30fa6-128">При быстром перемещении пальца по моему приложению появляется стрелка, а жест или манипуляция не регистрируются правильно.</span><span class="sxs-lookup"><span data-stu-id="30fa6-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="30fa6-129">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-129">Cause</span></span>    | <span data-ttu-id="30fa6-130">Включение жестов, если оно не требуется.</span><span class="sxs-lookup"><span data-stu-id="30fa6-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="30fa6-131">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-131">Solution</span></span> | <span data-ttu-id="30fa6-132">Вы включили жесты, если хотите отключить их.</span><span class="sxs-lookup"><span data-stu-id="30fa6-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="30fa6-133">Сведения об отключении жестов пером см. в статье [устаревшая поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fa6-134">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-134">Issue</span></span></td>
<td><span data-ttu-id="30fa6-135">Не удается различить входные данные мыши и сенсорный ввод Windows.</span><span class="sxs-lookup"><span data-stu-id="30fa6-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fa6-136">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-136">Cause</span></span></td>
<td><span data-ttu-id="30fa6-137">Windows создает сообщения мыши для поддержки устаревшей версии, когда пользователь щелкает на экране.</span><span class="sxs-lookup"><span data-stu-id="30fa6-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fa6-138">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-138">Solution</span></span></td>
<td><span data-ttu-id="30fa6-139">Вы можете вызвать <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">жетмессажеекстраинфо</a> для <strong>WM_LBUTTONDOWN</strong> и <strong>WM_LBUTTONUP</strong> сообщений, чтобы определить источник.</span><span class="sxs-lookup"><span data-stu-id="30fa6-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="30fa6-140">В следующем коде показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="30fa6-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fa6-141">C++</span><span class="sxs-lookup"><span data-stu-id="30fa6-141">C++</span></span></th>
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



 



| <span data-ttu-id="30fa6-142">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-142">Category</span></span> | <span data-ttu-id="30fa6-143">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-144">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-144">Issue</span></span>    | <span data-ttu-id="30fa6-145">Разделы справки запускать приложения Microsoft Пикселсенсе в Windows 7?</span><span class="sxs-lookup"><span data-stu-id="30fa6-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="30fa6-146">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-146">Cause</span></span>    | <span data-ttu-id="30fa6-147">Windows Touch и Microsoft Пикселсенсе несовместимы.</span><span class="sxs-lookup"><span data-stu-id="30fa6-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="30fa6-148">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-148">Solution</span></span> | <span data-ttu-id="30fa6-149">Необходимо ориентироваться на платформу Windows 7 или платформу Microsoft Пикселсенсе.</span><span class="sxs-lookup"><span data-stu-id="30fa6-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="30fa6-150">Устранение неполадок манипуляций и инерции</span><span class="sxs-lookup"><span data-stu-id="30fa6-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="30fa6-151">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-151">Category</span></span> | <span data-ttu-id="30fa6-152">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-153">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-153">Issue</span></span>    | <span data-ttu-id="30fa6-154">Мое приложение заморозить без причины.</span><span class="sxs-lookup"><span data-stu-id="30fa6-154">My application is freezing for no reason.</span></span> <span data-ttu-id="30fa6-155">Я получаю нарушения прав доступа при инициализации интерфейсов объектов.</span><span class="sxs-lookup"><span data-stu-id="30fa6-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="30fa6-156">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-156">Cause</span></span>    | <span data-ttu-id="30fa6-157">Отсутствие вызова **CoInitialize** при использовании интерфейсов [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) или [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="30fa6-158">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-158">Solution</span></span> | <span data-ttu-id="30fa6-159">Это может быть вызвано созданием объектов модели COM Windows Touch без вызова CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="30fa6-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="30fa6-160">Это происходит иногда при преобразовании проектов из использования жестов в использование манипуляций или интерфейсов инерции.</span><span class="sxs-lookup"><span data-stu-id="30fa6-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="30fa6-161">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-161">Category</span></span> | <span data-ttu-id="30fa6-162">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-163">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-163">Issue</span></span>    | <span data-ttu-id="30fa6-164">При переводе объект неверно вращается.</span><span class="sxs-lookup"><span data-stu-id="30fa6-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="30fa6-165">Вращение с одним пальцем работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="30fa6-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="30fa6-166">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-166">Cause</span></span>    | <span data-ttu-id="30fa6-167">Неправильное задание сводных значений для объекта.</span><span class="sxs-lookup"><span data-stu-id="30fa6-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="30fa6-168">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-168">Solution</span></span> | <span data-ttu-id="30fa6-169">Вы не настраиваете точки вращения для манипуляции правильно.</span><span class="sxs-lookup"><span data-stu-id="30fa6-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="30fa6-170">Задайте свойства [**пивотпоинткс**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) и [**пивотпоинти**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) в центре объекта или точки, вокруг которых нужно выполнить поворот, и задайте для свойства [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) значение Радиус объекта.</span><span class="sxs-lookup"><span data-stu-id="30fa6-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="30fa6-171">Устранение неполадок сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="30fa6-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="30fa6-172">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-172">Category</span></span> | <span data-ttu-id="30fa6-173">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-174">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-174">Issue</span></span>    | <span data-ttu-id="30fa6-175">После того как я обработал сообщение [**WM \_ Touch**](wm-touchdown.md) , я прекращаю получать отзывы о границе.</span><span class="sxs-lookup"><span data-stu-id="30fa6-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="30fa6-176">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-176">Cause</span></span>    | <span data-ttu-id="30fa6-177">Использование сообщения [**WM \_ Touch**](wm-touchdown.md) без его обработки.</span><span class="sxs-lookup"><span data-stu-id="30fa6-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="30fa6-178">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-178">Solution</span></span> | <span data-ttu-id="30fa6-179">Возможно, вы используете Windows Touch, не пересылая его в **дефвиндовпрок**, что приведет к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="30fa6-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="30fa6-180">Чтобы получить дополнительные сведения о правильной обработке сообщений [**WM \_ Touch**](wm-touchdown.md) , проверьте [Начало работы с помощью сенсорных сообщений Windows](getting-started-with-multi-touch-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fa6-181">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-181">Issue</span></span></td>
<td><span data-ttu-id="30fa6-182">Я рассматриваю Windows. h, но по-прежнему говорит, что <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> не определена.</span><span class="sxs-lookup"><span data-stu-id="30fa6-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fa6-183">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-183">Cause</span></span></td>
<td><span data-ttu-id="30fa6-184">Неправильная версия Windows в Targetver. h.</span><span class="sxs-lookup"><span data-stu-id="30fa6-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fa6-185">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-185">Solution</span></span></td>
<td><span data-ttu-id="30fa6-186">В проекте не задана правильная версия Windows.</span><span class="sxs-lookup"><span data-stu-id="30fa6-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="30fa6-187">Следующий код иллюстрирует правильную установку версий Windows для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30fa6-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fa6-188">C++</span><span class="sxs-lookup"><span data-stu-id="30fa6-188">C++</span></span></th>
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
<td><span data-ttu-id="30fa6-189">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-189">Issue</span></span></td>
<td><span data-ttu-id="30fa6-190">Недопустимые координаты x-координат и координаты y сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="30fa6-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="30fa6-191">Они имеют либо большие значения, чем ожидания, либо отрицательные значения.</span><span class="sxs-lookup"><span data-stu-id="30fa6-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fa6-192">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-192">Cause</span></span></td>
<td><span data-ttu-id="30fa6-193">Может потребоваться преобразовать сенсорные точки в пиксели или преобразовать экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="30fa6-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fa6-194">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-194">Solution</span></span></td>
<td><span data-ttu-id="30fa6-195">Убедитесь, что вызывается <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> и <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>скринтоклиент</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="30fa6-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="30fa6-196">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="30fa6-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fa6-197">C++</span><span class="sxs-lookup"><span data-stu-id="30fa6-197">C++</span></span></th>
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
<span data-ttu-id="30fa6-198">Чтобы использовать функцию <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>скринтоклиент</strong></a> , в приложении должна быть поддержка высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="30fa6-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="30fa6-199">Дополнительные сведения о поддержке высокого DPI см. в разделе о <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">высоком уровне dpi</a> в MSDN.</span><span class="sxs-lookup"><span data-stu-id="30fa6-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="30fa6-200">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-200">Category</span></span> | <span data-ttu-id="30fa6-201">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-202">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-202">Issue</span></span>    | <span data-ttu-id="30fa6-203">Я не вижу сообщений [**WM \_ Touch**](wm-touchdown.md) , но я знаю, что касание Windows работает, так как я вижу сообщения [**\_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="30fa6-204">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-204">Cause</span></span>    | <span data-ttu-id="30fa6-205">Отсутствует вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="30fa6-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="30fa6-206">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-206">Solution</span></span> | <span data-ttu-id="30fa6-207">[**WM \_ Сообщения жестов сенсорного ввода**](wm-touchdown.md) и [**WM \_**](wm-gesture.md) являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="30fa6-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="30fa6-208">Если не вызвать [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), будут получены только сообщения **\_ жестов WM** .</span><span class="sxs-lookup"><span data-stu-id="30fa6-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="30fa6-209">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-209">Category</span></span> | <span data-ttu-id="30fa6-210">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-211">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-211">Issue</span></span>    | <span data-ttu-id="30fa6-212">Я получаю небольшие задержки со времени, когда я касался пальца до получения входных данных в приложении.</span><span class="sxs-lookup"><span data-stu-id="30fa6-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="30fa6-213">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-213">Cause</span></span>    | <span data-ttu-id="30fa6-214">Отклонение Palm вызывает задержки во входных данных.</span><span class="sxs-lookup"><span data-stu-id="30fa6-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="30fa6-215">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-215">Solution</span></span> | <span data-ttu-id="30fa6-216">Если **ТВФ \_ вантпалм** установлен в вызовах [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), то отклонение Palm включено.</span><span class="sxs-lookup"><span data-stu-id="30fa6-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="30fa6-217">Это вызывает небольшую задержку (100 мс), пока программное обеспечение проверит, поступает ли вход с помощью пальца, пера или карманного компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="30fa6-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="30fa6-218">Отключите отклонение Palm, вызвав **регистертаучвиндов** с установленным флагом **ТВФ \_ вантпалм** .</span><span class="sxs-lookup"><span data-stu-id="30fa6-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="30fa6-219">Устранение неполадок сенсорных жестов Windows</span><span class="sxs-lookup"><span data-stu-id="30fa6-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="30fa6-220">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-220">Category</span></span> | <span data-ttu-id="30fa6-221">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-222">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-222">Issue</span></span>    | <span data-ttu-id="30fa6-223">После обработки сообщения [**\_ жеста WM**](wm-gesture.md) я прекращаю получать отзывы о границе.</span><span class="sxs-lookup"><span data-stu-id="30fa6-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="30fa6-224">Или жест, который работал ранее, сейчас не работает.</span><span class="sxs-lookup"><span data-stu-id="30fa6-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="30fa6-225">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-225">Cause</span></span>    | <span data-ttu-id="30fa6-226">Использование сообщения [**\_ жеста WM**](wm-gesture.md) без его обработки.</span><span class="sxs-lookup"><span data-stu-id="30fa6-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="30fa6-227">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-227">Solution</span></span> | <span data-ttu-id="30fa6-228">Возможно, вы используете Windows Touch, не пересылая его в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca), что приведет к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="30fa6-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="30fa6-229">Дополнительные сведения о правильной обработке сообщений [**\_ жестов WM**](wm-gesture.md) см. в [Начало работы с помощью жестов Windows](getting-started-with-multi-touch-gestures.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="30fa6-230">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-230">Category</span></span> | <span data-ttu-id="30fa6-231">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-232">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-232">Issue</span></span>    | <span data-ttu-id="30fa6-233">Я не вижу сообщения [**\_ жестов WM**](wm-gesture.md) , но я знаю, что касание Windows работает, так как я вижу сообщения [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="30fa6-234">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-234">Cause</span></span>    | <span data-ttu-id="30fa6-235">Вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="30fa6-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="30fa6-236">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-236">Solution</span></span> | <span data-ttu-id="30fa6-237">[**WM \_ Сообщения жестов сенсорного ввода**](wm-touchdown.md) и [**WM \_**](wm-gesture.md) являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="30fa6-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="30fa6-238">При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы не получите сообщения **\_ жестов WM** .</span><span class="sxs-lookup"><span data-stu-id="30fa6-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30fa6-239">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-239">Issue</span></span></td>
<td><span data-ttu-id="30fa6-240">Я вижу не все жесты, которые мне хотелось видеть.</span><span class="sxs-lookup"><span data-stu-id="30fa6-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="30fa6-241">Например, я вижу жесты с идентификатором <strong>GID_PAN</strong> но не <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="30fa6-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30fa6-242">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-242">Cause</span></span></td>
<td><span data-ttu-id="30fa6-243">Некоторые жесты, такие как жест поворота, по умолчанию отключены.</span><span class="sxs-lookup"><span data-stu-id="30fa6-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30fa6-244">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-244">Solution</span></span></td>
<td><span data-ttu-id="30fa6-245">Необходимо вызвать <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>сетжестуреконфиг</strong></a> при получении сообщения <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> , как описано в справочнике по <strong>WM_GESTURENOTIFY</strong> , или необходимо добавить обработчик для сообщения <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="30fa6-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="30fa6-246">В следующем коде показано, как можно реализовать обработчик, чтобы обеспечить поддержку вращения.</span><span class="sxs-lookup"><span data-stu-id="30fa6-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30fa6-247">C++</span><span class="sxs-lookup"><span data-stu-id="30fa6-247">C++</span></span></th>
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

<span data-ttu-id="30fa6-248">Дополнительные примеры типичных конфигураций жестов см. в разделе <strong>сетжестуреконфиг</strong>.</span><span class="sxs-lookup"><span data-stu-id="30fa6-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="30fa6-249">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-249">Category</span></span> | <span data-ttu-id="30fa6-250">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-251">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-251">Issue</span></span>    | <span data-ttu-id="30fa6-252">Пользовательские полосы прокрутки в приложении не прокручивается при выполнении жеста панорамирования.</span><span class="sxs-lookup"><span data-stu-id="30fa6-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="30fa6-253">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-253">Cause</span></span>    | <span data-ttu-id="30fa6-254">Отсутствуют обработчики для правильных \_ \* сообщений прокрутки WM.</span><span class="sxs-lookup"><span data-stu-id="30fa6-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="30fa6-255">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-255">Solution</span></span> | <span data-ttu-id="30fa6-256">Вы не обрабатываете все \_ \* сообщения прокрутки WM в настраиваемых полосах прокрутки.</span><span class="sxs-lookup"><span data-stu-id="30fa6-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="30fa6-257">Рекомендуется работать с сообщением [**\_ жеста WM**](wm-gesture.md) вместо того, чтобы хранить пользовательские функции прокрутки с помощью устаревшей поддержки.</span><span class="sxs-lookup"><span data-stu-id="30fa6-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="30fa6-258">Необходимо поддерживать сообщения, как описано в разделе [поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="30fa6-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="30fa6-259">Категория</span><span class="sxs-lookup"><span data-stu-id="30fa6-259">Category</span></span> | <span data-ttu-id="30fa6-260">Описание</span><span class="sxs-lookup"><span data-stu-id="30fa6-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fa6-261">Проблема</span><span class="sxs-lookup"><span data-stu-id="30fa6-261">Issue</span></span>    | <span data-ttu-id="30fa6-262">Я получаю задержки для жестов.</span><span class="sxs-lookup"><span data-stu-id="30fa6-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="30fa6-263">Причина</span><span class="sxs-lookup"><span data-stu-id="30fa6-263">Cause</span></span>    | <span data-ttu-id="30fa6-264">Жесты могут вызывать задержки для жестов.</span><span class="sxs-lookup"><span data-stu-id="30fa6-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="30fa6-265">Решение</span><span class="sxs-lookup"><span data-stu-id="30fa6-265">Solution</span></span> | <span data-ttu-id="30fa6-266">Жесты могут вызвать задержки в течение времени, затрачиваемого приложением на получение сообщений [**\_ жестов WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="30fa6-267">Сведения об отключении жестов см. в статье [устаревшая поддержка панорамирования с помощью полос прокрутки](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="30fa6-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="30fa6-268">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="30fa6-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30fa6-269">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="30fa6-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 