---
title: Разработка приложений WPF для мониторов с поддержкой определения DPI
description: Примечание. на этой странице рассматривается устаревшая разработка WPF для Windows 8.1. Если вы разрабатываете приложения WPF для Windows 10, ознакомьтесь с последней документацией на сайте GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Пользовательский интерфейс Windows, приложения, поддерживающие DPI
- Пользовательский интерфейс Windows, высокое разрешение DPI
- Приложения, поддерживающие DPI
- высокое разрешение DPI
- Написание приложений Win32 с поддержкой DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133874"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="a8164-110">Разработка приложений WPF для мониторов с поддержкой определения DPI</span><span class="sxs-lookup"><span data-stu-id="a8164-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="a8164-111">**Важные API**</span><span class="sxs-lookup"><span data-stu-id="a8164-111">**Important APIs**</span></span>

-   [<span data-ttu-id="a8164-112">**сетпроцессдпиаваренесс**</span><span class="sxs-lookup"><span data-stu-id="a8164-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="a8164-113">**жетпроцессдпиаваренесс**</span><span class="sxs-lookup"><span data-stu-id="a8164-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="a8164-114">**жетдпиформонитор**</span><span class="sxs-lookup"><span data-stu-id="a8164-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="a8164-115">**На этой странице рассматривается устаревшая разработка WPF для Windows 8.1.**</span><span class="sxs-lookup"><span data-stu-id="a8164-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="a8164-116">Если вы разрабатываете приложения WPF для Windows 10, ознакомьтесь с <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">последней документацией на сайте GitHub.</a></span><span class="sxs-lookup"><span data-stu-id="a8164-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="a8164-117">Windows 8.1 предоставляет разработчикам новые функции для создания настольных приложений, учитывающих разрешение DPI для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="a8164-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="a8164-118">Чтобы воспользоваться преимуществами этой функции, приложение с поддержкой DPI для каждого монитора должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a8164-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="a8164-119">Изменение размеров окна для поддержания физического размера, который отображается единообразно на любом дисплее</span><span class="sxs-lookup"><span data-stu-id="a8164-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="a8164-120">Повторное создание макета и повторное отображение графики для нового размера окна</span><span class="sxs-lookup"><span data-stu-id="a8164-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="a8164-121">Выберите шрифты, которые будут масштабироваться соответствующим образом для уровня DPI</span><span class="sxs-lookup"><span data-stu-id="a8164-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="a8164-122">Выбор и загрузка ресурсов точечного рисунка, адаптированных для уровня DPI</span><span class="sxs-lookup"><span data-stu-id="a8164-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="a8164-123">Чтобы упростить создание приложения с поддержкой DPI для каждого монитора, Windows 8.1 предоставляет следующие возможности Microsoft Win32APIs:</span><span class="sxs-lookup"><span data-stu-id="a8164-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="a8164-124">[**Сетпроцессдпиаваренесс**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (или запись манифеста DPI) задает для процесса указанный уровень осведомленности относительно dpi, который затем определяет, как Windows масштабирует пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a8164-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="a8164-125">Это заменяет [**сетпроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="a8164-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="a8164-126">[**Жетпроцессдпиаваренесс**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) возвращает уровень осведомленности о dpi.</span><span class="sxs-lookup"><span data-stu-id="a8164-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="a8164-127">Это заменяет [**испроцессдпиаваре**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="a8164-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="a8164-128">[**Жетдпиформонитор**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) ВОЗВРАЩАЕТ значение dpi для монитора.</span><span class="sxs-lookup"><span data-stu-id="a8164-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="a8164-129">Уведомление окна [**WM \_ DPICHANGED**](wm-dpichanged.md) отправляется в приложения с поддержкой dpi для каждого монитора при изменении положения окна таким, что большая часть области пересекает монитор с dpi, отличным от dpi до изменения положения, или когда пользователь перемещает ползунок отображения.</span><span class="sxs-lookup"><span data-stu-id="a8164-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="a8164-130">Чтобы создать приложение, которое изменяет размер и отображает его при перемещении пользователя на другой экран, используйте это уведомление.</span><span class="sxs-lookup"><span data-stu-id="a8164-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="a8164-131">Дополнительные сведения о различных уровнях определения DPI, поддерживаемых для настольных приложений, в Windows 8.1 см. в разделе [написание DPI-Aware приложений для настольных систем и Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="a8164-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="a8164-132">Масштабирование DPI и WPF</span><span class="sxs-lookup"><span data-stu-id="a8164-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="a8164-133">Приложения Windows Presentation Foundation (WPF) по умолчанию отслеживаются по DPI.</span><span class="sxs-lookup"><span data-stu-id="a8164-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="a8164-134">Определения различных уровней осведомленности относительно DPI см. в разделе [написание DPI-Aware приложений для настольных систем и Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="a8164-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="a8164-135">Графическая система WPF использует аппаратно-независимые единицы, чтобы обеспечить независимость от разрешения и устройства.</span><span class="sxs-lookup"><span data-stu-id="a8164-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="a8164-136">WPF масштабирует каждый независимый от устройства пиксель автоматически на основе текущего DPI системы.</span><span class="sxs-lookup"><span data-stu-id="a8164-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="a8164-137">Это позволяет приложениям WPF масштабироваться автоматически, если значение DPI монитора, на котором находится окно, равно значению DPI системы.</span><span class="sxs-lookup"><span data-stu-id="a8164-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="a8164-138">Однако, так как приложения WPF учитывают контроль dpi системы, приложение будет масштабироваться операционной системой при перемещении приложения на монитор с другим разрешением или при использовании ползунка на панели управления для изменения DPI.</span><span class="sxs-lookup"><span data-stu-id="a8164-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="a8164-139">Масштабирование в операционной системе может привести к тому, что приложения WPF будут выглядеть размытыми, особенно если масштабирование не является неотъемлемой частью.</span><span class="sxs-lookup"><span data-stu-id="a8164-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="a8164-140">Чтобы избежать масштабирования приложений WPF, их необходимо обновить, чтобы они были ориентированы на контроль DPI.</span><span class="sxs-lookup"><span data-stu-id="a8164-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="a8164-141">Пример пошагового руководства WPF на уровне мониторинга</span><span class="sxs-lookup"><span data-stu-id="a8164-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="a8164-142">[Пример WPF, поддерживающий мониторинг](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) , — это пример приложения WPF, который обновляется в соответствии с отслеживанием dpi.</span><span class="sxs-lookup"><span data-stu-id="a8164-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="a8164-143">Пример состоит из двух проектов:</span><span class="sxs-lookup"><span data-stu-id="a8164-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="a8164-144">Нативехелперс. vcxproj — это собственный вспомогательный проект, реализующий основные функции для создания приложения WPF в качестве уровня DPI для каждого монитора с использованием Win32APIs выше.</span><span class="sxs-lookup"><span data-stu-id="a8164-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="a8164-145">Проект содержит два класса:</span><span class="sxs-lookup"><span data-stu-id="a8164-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="a8164-146">Пермондпихелперс: класс, предоставляющий вспомогательные функции для операций, связанных с DPI, таких как получение текущего значения DPI активного монитора, установка процесса в соответствии с DPI и т. д.</span><span class="sxs-lookup"><span data-stu-id="a8164-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="a8164-147">Пермонитордпивиндов: базовый класс, производный от **System. Windows. Window** , который реализует функциональные возможности для того, чтобы окно приложения WPF было ориентировано на контроль dpi.</span><span class="sxs-lookup"><span data-stu-id="a8164-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="a8164-148">Корректирует размер окна, размер отрисовки графики и размер шрифта на основе DPI монитора, а не DPI на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="a8164-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="a8164-149">Впфаппликатион. csproj: пример приложения WPF, использующего Пермонитордпивиндов (Пермонитордпивиндов), и демонстрируется изменение размера окна приложения и его отрисовки при перемещении окна на монитор с другим DPI или при использовании ползунка на панели управления "дисплей" для изменения DPI.</span><span class="sxs-lookup"><span data-stu-id="a8164-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="a8164-150">Чтобы запустить пример, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a8164-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="a8164-151">Загрузка и распаковка [примера для WPF с поддержкой мониторинга](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span><span class="sxs-lookup"><span data-stu-id="a8164-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="a8164-152">Запустите Microsoft Visual Studio и выберите **файл > открыть > проект или решение** .</span><span class="sxs-lookup"><span data-stu-id="a8164-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="a8164-153">Перейдите в каталог, содержащий Распакованный пример.</span><span class="sxs-lookup"><span data-stu-id="a8164-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="a8164-154">Перейдите в каталог с именем для примера и дважды щелкните файл решения Visual Studio (SLN).</span><span class="sxs-lookup"><span data-stu-id="a8164-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="a8164-155">Нажмите клавишу F7 или используйте **build > Build Solution** для создания примера</span><span class="sxs-lookup"><span data-stu-id="a8164-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="a8164-156">Нажмите клавиши CTRL + F5 или используйте **отладку > запуск без отладки** , чтобы запустить пример</span><span class="sxs-lookup"><span data-stu-id="a8164-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="a8164-157">Чтобы увидеть влияние изменения DPI на приложение WPF, которое обновляется с учетом DPI для каждого монитора, используя базовый класс в примере, переместите окно приложения в и из отображения, которые имеют разные dpi.</span><span class="sxs-lookup"><span data-stu-id="a8164-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="a8164-158">При перемещении окна между мониторами размер окна и масштаб пользовательского интерфейса обновляются на основе DPI на дисплее с помощью масштабируемой графической системы WPF, а не при масштабировании операционной системой.</span><span class="sxs-lookup"><span data-stu-id="a8164-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="a8164-159">Пользовательский интерфейс приложения отображается в собственном виде и не выглядит размытым.</span><span class="sxs-lookup"><span data-stu-id="a8164-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="a8164-160">Если у вас нет двух дисплеев с разными DPI, измените значение DPI, изменив ползунок на панели управления экрана.</span><span class="sxs-lookup"><span data-stu-id="a8164-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="a8164-161">Изменение ползунка и нажатие кнопки **Применить** приведет к изменению размера окна приложения и автоматическому обновлению масштаба пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8164-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="a8164-162">Обновление существующего приложения WPF с учетом уровня dpi для каждого монитора с помощью вспомогательного проекта в примере WPF</span><span class="sxs-lookup"><span data-stu-id="a8164-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="a8164-163">Если у вас есть существующее приложение WPF и вы хотите использовать вспомогательный проект DPI из примера, чтобы обеспечить отслеживание DPI, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8164-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="a8164-164">Загрузка и распаковка примера для WPF с поддержкой мониторинга</span><span class="sxs-lookup"><span data-stu-id="a8164-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="a8164-165">Запустите Visual Studio и выберите **файл > открыть > проект или решение** .</span><span class="sxs-lookup"><span data-stu-id="a8164-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="a8164-166">Перейдите к каталогу, содержащему существующее приложение WPF, и дважды щелкните файл решения Visual Studio (SLN).</span><span class="sxs-lookup"><span data-stu-id="a8164-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="a8164-167">Щелкните правой кнопкой мыши **решение > добавить > существующий проект** ![ — снимок экрана, иллюстрирующий выбор пункта меню Добавить: существующий проект.](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="a8164-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="a8164-168">В диалоговом окне выбора файлов перейдите к каталогу, содержащему пример несжатого архива.</span><span class="sxs-lookup"><span data-stu-id="a8164-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="a8164-169">Откройте каталог с именем для примера, перейдите в папку "Нативехелперс", выберите файл проекта Visual C++ "Нативехелперс. vcxproj" и нажмите кнопку " **ОК** ".</span><span class="sxs-lookup"><span data-stu-id="a8164-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="a8164-170">Щелкните правой кнопкой мыши проект Нативехелперс и выберите **Build (сборка**).</span><span class="sxs-lookup"><span data-stu-id="a8164-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="a8164-171">Будет создан NativeHelpers.dll, который будет добавлен в качестве ссылки на приложение WPF на следующем шаге. ![ снимок экрана, иллюстрирующий выбор в меню "сборка"](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="a8164-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="a8164-172">Добавьте ссылку на NativeHelpers.dll из приложения WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="a8164-173">Разверните проект приложения WPF, щелкните **ссылки** правой кнопкой мыши и выберите команду **Добавить ссылку...**</span><span class="sxs-lookup"><span data-stu-id="a8164-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="a8164-174">В открывшемся диалоговом окне разверните раздел **решение** .</span><span class="sxs-lookup"><span data-stu-id="a8164-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="a8164-175">В разделе **проекты** выберите нативехелперс и нажмите кнопку **ОК** ![ на снимке экрана, иллюстрирующий диалоговое окно диспетчера ресурсов.](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="a8164-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="a8164-176">Разверните проект приложения WPF, разверните узел **Свойства** и откройте **AssemblyInfo. CS**.</span><span class="sxs-lookup"><span data-stu-id="a8164-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="a8164-177">Внесите следующие дополнения в AssemblyInfo. cs.</span><span class="sxs-lookup"><span data-stu-id="a8164-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="a8164-178">Добавьте ссылку на System. Windows. Media в разделе справки (с помощью System. Windows. Media;).</span><span class="sxs-lookup"><span data-stu-id="a8164-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="a8164-179">Добавьте атрибут Дисабледпиаваренесс ( `[assembly: DisableDpiAwareness]` ).</span><span class="sxs-lookup"><span data-stu-id="a8164-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![снимок экрана, иллюстрирующий дополнительные свойства](images/scrvs-image4.png)
10. <span data-ttu-id="a8164-181">Наследовать основной класс окна WPF от базового класса Пермонитордпивиндов</span><span class="sxs-lookup"><span data-stu-id="a8164-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="a8164-182">Обновление файла CS главного окна WPF для наследования от базового класса Пермонитордпивиндов</span><span class="sxs-lookup"><span data-stu-id="a8164-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="a8164-183">Добавьте ссылку на Нативехелперс в разделе Reference, добавив строку `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="a8164-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="a8164-184">Наследовать класс главного окна от класса Пермонитордпивиндов</span><span class="sxs-lookup"><span data-stu-id="a8164-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![снимок экрана, иллюстрирующий Справочник по c++](images/scrvs-image5.png)
    -   <span data-ttu-id="a8164-186">Обновление файла XAML главного окна WPF для наследования от базового класса Пермонитордпивиндов</span><span class="sxs-lookup"><span data-stu-id="a8164-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="a8164-187">Добавьте ссылку на Нативехелперс в разделе Reference, добавив строку `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="a8164-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="a8164-188">Наследовать класс главного окна от класса Пермонитордпивиндов</span><span class="sxs-lookup"><span data-stu-id="a8164-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![снимок экрана, иллюстрирующий Добавление ссылки на XAML](images/scrvs-image6.png)
11. <span data-ttu-id="a8164-190">Нажмите клавишу F7 или используйте **build > Build Solution** для создания примера</span><span class="sxs-lookup"><span data-stu-id="a8164-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="a8164-191">Нажмите клавиши CTRL + F5 или используйте **отладку > запуск без отладки** , чтобы запустить пример</span><span class="sxs-lookup"><span data-stu-id="a8164-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="a8164-192">[Пример приложения WPF с поддержкой отслеживания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) на уровне мониторинга показывает, как можно обновить приложение WPF, чтобы оно отвечало на контроль dpi, реагируя на уведомление окна [**WM \_ DPICHANGED**](wm-dpichanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a8164-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="a8164-193">В ответ на уведомление окна пример обновляет преобразование масштабирования, используемое WPF на основе текущего DPI монитора, на котором находится окно.</span><span class="sxs-lookup"><span data-stu-id="a8164-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="a8164-194">Параметр *wParam* уведомления окна содержит новое значение dpi в параметре *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a8164-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="a8164-195">*LParam* содержит прямоугольник с размером и положением нового рекомендуемого окна, который масштабируется для новых точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="a8164-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="a8164-196">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a8164-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="a8164-197">Поскольку этот пример перезаписывает размер окна и преобразование масштабирования корневого узла окна WPF, разработчику приложения может потребоваться дополнительная работа, если:</span><span class="sxs-lookup"><span data-stu-id="a8164-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="a8164-198">Размер окна влияет на другие части приложения, такие как это окно WPF, размещенное в другом приложении.</span><span class="sxs-lookup"><span data-stu-id="a8164-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="a8164-199">Приложение WPF, расширяющее этот класс, задает другое преобразование в корневом визуальном элементе; образец может перезаписать другое преобразование, которое применяется самим приложением WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="a8164-200">Общие сведения о вспомогательном проекте в примере WPF</span><span class="sxs-lookup"><span data-stu-id="a8164-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="a8164-201">Чтобы создать существующее приложение WPF на уровне DPI для каждого монитора, Библиотека Нативехелперс предоставляет следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="a8164-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="a8164-202">**Помечает приложение WPF как понитор dpi с учетом количества точек на дюйм:** Приложение WPF помечается как ориентированное на контроль DPI путем вызова [**сетпроцессдпиаваренесс**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="a8164-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="a8164-203">Пометка приложения как учитывающего DPI для каждого монитора обеспечит</span><span class="sxs-lookup"><span data-stu-id="a8164-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="a8164-204">ОПЕРАЦИОННАЯ система не масштабирует приложение, если DPI системы не соответствует текущему значению DPI монитора, в котором находится окно приложения.</span><span class="sxs-lookup"><span data-stu-id="a8164-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="a8164-205">Сообщение [**WM \_ DPICHANGED**](wm-dpichanged.md) отправляется при каждом изменении dpi окна</span><span class="sxs-lookup"><span data-stu-id="a8164-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="a8164-206">**Корректирует размер окна, перекомпоновку и повторное отображение содержимого графики и выбор шрифтов на основе начального DPI монитора, на котором находится окно:** После того как приложение помечается как ориентированное на контроль DPI, WPF по-прежнему будет масштабировать размер окна, графику и размер шрифта на основе DPI на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="a8164-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="a8164-207">Так как при запуске приложения не гарантируется, что DPI на уровне системы будет таким же, как и у монитора, на котором запускается окно, Библиотека корректирует эти значения после загрузки окна.</span><span class="sxs-lookup"><span data-stu-id="a8164-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="a8164-208">Базовый класс **пермонитордпивиндов** обновляет эти данные в обработчике **OnLoaded ()** .</span><span class="sxs-lookup"><span data-stu-id="a8164-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="a8164-209">Размер окна обновляется путем изменения свойств **Width** и **Height** окна.</span><span class="sxs-lookup"><span data-stu-id="a8164-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="a8164-210">Макет и размер обновляются путем применения соответствующего преобразования масштаба к корневому узлу окна WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="a8164-211">**Реагирует на WM \_ DPICHANGED Window Notification:** обновление размера окна, графики и размера шрифта на основе значений dpi, переданных в окне уведомления.</span><span class="sxs-lookup"><span data-stu-id="a8164-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="a8164-212">Базовый класс **пермонитордпивиндов** обрабатывает уведомление окна в методе **хандлемессажес ()** .</span><span class="sxs-lookup"><span data-stu-id="a8164-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="a8164-213">Размер окна обновляется путем вызова **SetWindowPos** с использованием информации, передаваемой в параметре *lParam* сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="a8164-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="a8164-214">Размер макета и графики обновляется путем применения соответствующего преобразования масштаба к корневому узлу окна WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="a8164-215">Коэффициент масштабирования вычисляется с помощью параметра DPI, переданного в параметре *wParam* окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8164-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="a8164-216">Обработка изменения DPI для активов, например изображений</span><span class="sxs-lookup"><span data-stu-id="a8164-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="a8164-217">Для обновления графического содержимого пример приложения WPF применяет преобразование масштабирования к корневому узлу приложения WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="a8164-218">Хотя это хорошо подходит для содержимого, отображаемого изначально WPF (прямоугольник, текст и т. д.), это подразумевает, что ресурсы точечного рисунка, такие как изображения, масштабируются WPF.</span><span class="sxs-lookup"><span data-stu-id="a8164-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="a8164-219">Чтобы избежать размытых растровых изображений, вызванных масштабированием, разработчик приложения WPF может написать настраиваемый элемент управления Image, который выбирает другой ресурс на основе текущего DPI монитора, на котором находится окно.</span><span class="sxs-lookup"><span data-stu-id="a8164-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="a8164-220">Элемент управления "изображение" может полагаться на событие **DPIChanged ()** , которое срабатывает для окна WPF, использующего **пермонитордпивиндов**, при изменении dpi.</span><span class="sxs-lookup"><span data-stu-id="a8164-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="a8164-221">Элемент управления "изображение" также должен выбрать нужный элемент управления во время запуска приложения в обработчике событий окна " **загружено ()** WPF".</span><span class="sxs-lookup"><span data-stu-id="a8164-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 