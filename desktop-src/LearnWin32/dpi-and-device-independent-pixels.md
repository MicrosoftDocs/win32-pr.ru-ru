---
title: DPI и Device-Independent пикселей
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Дополнительные сведения: DPI и Device-Independent пикселей'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913279"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="5802a-103">DPI и Device-Independent пикселей</span><span class="sxs-lookup"><span data-stu-id="5802a-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="5802a-104">Для эффективной работы с графикой Windows необходимо понимать два связанных понятия:</span><span class="sxs-lookup"><span data-stu-id="5802a-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="5802a-105">Точек на дюйм (DPI)</span><span class="sxs-lookup"><span data-stu-id="5802a-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="5802a-106">Аппаратно-независимый пиксель (DIP).</span><span class="sxs-lookup"><span data-stu-id="5802a-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="5802a-107">Начнем с DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-107">Let's start with DPI.</span></span> <span data-ttu-id="5802a-108">Для этого потребуется краткий обзор типографии.</span><span class="sxs-lookup"><span data-stu-id="5802a-108">This will require a short detour into typography.</span></span> <span data-ttu-id="5802a-109">В типографии размер типа измеряется в единицах, именуемых *points*.</span><span class="sxs-lookup"><span data-stu-id="5802a-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="5802a-110">Одна точка равна 1/72 дюйма.</span><span class="sxs-lookup"><span data-stu-id="5802a-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="5802a-111">1 пт = 1/72 дюйма</span><span class="sxs-lookup"><span data-stu-id="5802a-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="5802a-112">Это определение точки публикации на настольном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5802a-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="5802a-113">Исторически точная мера точки изменилась.</span><span class="sxs-lookup"><span data-stu-id="5802a-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="5802a-114">Например, шрифт 12-точечного шрифта помещается в строку текста 1/6 "(12/72).</span><span class="sxs-lookup"><span data-stu-id="5802a-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="5802a-115">Очевидно, что это не означает, что каждый символ в шрифте ровно 1/6 «высокий».</span><span class="sxs-lookup"><span data-stu-id="5802a-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="5802a-116">На самом деле некоторые символы могут быть больше, чем 1/6.</span><span class="sxs-lookup"><span data-stu-id="5802a-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="5802a-117">Например, во многих шрифтах символ a больше, чем номинальная высота шрифта.</span><span class="sxs-lookup"><span data-stu-id="5802a-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="5802a-118">Для правильного вывода шрифта требуется дополнительное пространство между текстом.</span><span class="sxs-lookup"><span data-stu-id="5802a-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="5802a-119">Это пространство называется *ведущим*.</span><span class="sxs-lookup"><span data-stu-id="5802a-119">This space is called the *leading*.</span></span>

<span data-ttu-id="5802a-120">На следующем рисунке показан шрифт 72-пт.</span><span class="sxs-lookup"><span data-stu-id="5802a-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="5802a-121">В сплошных линиях вокруг текста отображается 1 «ограничивающий прямоугольник».</span><span class="sxs-lookup"><span data-stu-id="5802a-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="5802a-122">Пунктирная линия называется *базовой*.</span><span class="sxs-lookup"><span data-stu-id="5802a-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="5802a-123">Большая часть символов в шрифте, оставшаяся в базовом плане.</span><span class="sxs-lookup"><span data-stu-id="5802a-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="5802a-124">Высота шрифта включает часть, расположенную выше базовой линии ( *восхождение*), и часть, расположенную ниже базовой линии ( *спуск*).</span><span class="sxs-lookup"><span data-stu-id="5802a-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="5802a-125">В показанном здесь шрифте восхождение составляет 56 точек, а спуск — 16 пунктов.</span><span class="sxs-lookup"><span data-stu-id="5802a-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![Иллюстрация, на которой показан шрифт в 72 пт.](images/graphics11.png)

<span data-ttu-id="5802a-127">Однако, когда дело доходит до экрана компьютера, измерение размера текста является проблематичным, так как в пикселях используется не тот же размер.</span><span class="sxs-lookup"><span data-stu-id="5802a-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="5802a-128">Размер пикселя зависит от двух факторов: разрешения экрана и физического размера монитора.</span><span class="sxs-lookup"><span data-stu-id="5802a-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="5802a-129">Таким образом, физические дюймы не являются полезной мерой, так как нет фиксированной связи между физическими дюймами и пикселями.</span><span class="sxs-lookup"><span data-stu-id="5802a-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="5802a-130">Шрифты измеряются в *логических* единицах.</span><span class="sxs-lookup"><span data-stu-id="5802a-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="5802a-131">Шрифт в 72 пт определяется как один логический дюйм в высоту.</span><span class="sxs-lookup"><span data-stu-id="5802a-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="5802a-132">Затем логические дюймы преобразуются в пиксели.</span><span class="sxs-lookup"><span data-stu-id="5802a-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="5802a-133">В течение многих лет в Windows использовалось следующее преобразование: один логический дюйм равен 96 пикселов.</span><span class="sxs-lookup"><span data-stu-id="5802a-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="5802a-134">При использовании этого коэффициента масштабирования шрифт 72-пт выводится в высоту 96 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5802a-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="5802a-135">Высота 12-точечного шрифта составляет 16 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5802a-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="5802a-136">12 точек = 12/72 логический дюйм = 1/6 логический дюйм = 96/6 пикселей = 16 пикселей</span><span class="sxs-lookup"><span data-stu-id="5802a-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="5802a-137">Этот коэффициент масштабирования описан как 96 точек на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="5802a-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="5802a-138">Термин точки наследуется от печати, где на бумаге помещаются физические точки рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="5802a-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="5802a-139">Для дисплеев на компьютере было бы более точным, например, 96 пикселей на логический дюйм, но в этом случае это означает, что точка DPI была задержана.</span><span class="sxs-lookup"><span data-stu-id="5802a-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="5802a-140">Так как фактические размеры пикселей различаются, текст, который может быть прочитан на одном мониторе, на другом мониторе могут быть слишком маленьким.</span><span class="sxs-lookup"><span data-stu-id="5802a-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="5802a-141">Кроме того, люди имеют разные предпочтения — некоторые люди предпочитают текст больше.</span><span class="sxs-lookup"><span data-stu-id="5802a-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="5802a-142">По этой причине Windows позволяет пользователю изменить параметр DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="5802a-143">Например, если пользователь устанавливает для дисплея значение 144 DPI, то шрифт 72-пт составляет 144 пикселей в высоту.</span><span class="sxs-lookup"><span data-stu-id="5802a-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="5802a-144">Параметры стандартного DPI: 100% (96 точек на дюйм), 125% (120 DPI) и 150% (144 DPI).</span><span class="sxs-lookup"><span data-stu-id="5802a-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="5802a-145">Пользователь может также применить настраиваемый параметр.</span><span class="sxs-lookup"><span data-stu-id="5802a-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="5802a-146">Начиная с Windows 7 DPI — это параметр для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5802a-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="5802a-147">Масштабирование DWM</span><span class="sxs-lookup"><span data-stu-id="5802a-147">DWM Scaling</span></span>

<span data-ttu-id="5802a-148">Если программа не учитывает DPI, то следующие дефекты могут быть очевидны при высоком уровне DPI:</span><span class="sxs-lookup"><span data-stu-id="5802a-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="5802a-149">Обрезанные элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5802a-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="5802a-150">Неверный макет.</span><span class="sxs-lookup"><span data-stu-id="5802a-150">Incorrect layout.</span></span>
-   <span data-ttu-id="5802a-151">Пикселизованным точечные рисунки и значки.</span><span class="sxs-lookup"><span data-stu-id="5802a-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="5802a-152">Неверные координаты указателя мыши, которые могут повлиять на проверку попадания, перетаскивание и т. д.</span><span class="sxs-lookup"><span data-stu-id="5802a-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="5802a-153">Чтобы обеспечить работу старых программ в параметрах с высоким разрешением, DWM реализует полезную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="5802a-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="5802a-154">Если программа не помечена как учитывающая DPI, DWM будет масштабировать весь пользовательский интерфейс в соответствии с параметром DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="5802a-155">Например, при 144 DPI пользовательский интерфейс масштабируется по 150%, включая текст, графику, элементы управления и размеры окон.</span><span class="sxs-lookup"><span data-stu-id="5802a-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="5802a-156">Если программа создает окно 500 × 500, окно отображается как 750 × 750 пикселей, а содержимое окна масштабируется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="5802a-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="5802a-157">Такое поведение означает, что старые программы работают только в параметрах с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="5802a-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="5802a-158">Однако масштабирование также приводит к частично размытому внешнему виду, так как масштабирование применяется после прорисовки окна.</span><span class="sxs-lookup"><span data-stu-id="5802a-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="5802a-159">DPI-Aware приложения</span><span class="sxs-lookup"><span data-stu-id="5802a-159">DPI-Aware Applications</span></span>

<span data-ttu-id="5802a-160">Чтобы избежать масштабирования, программа может пометить себя как поддерживающую DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="5802a-161">Это говорит о том, что DWM не будет выполнять автоматическое масштабирование DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="5802a-162">Все новые приложения должны быть спроектированы с учетом DPI, так как осведомленность о DPI улучшает внешний вид параметров пользовательского интерфейса при высоком уровне DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="5802a-163">Программа объявляет свое разрешение с учетом DPI через манифест приложения.</span><span class="sxs-lookup"><span data-stu-id="5802a-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="5802a-164">*Манифест* — это просто XML-файл, ОПИСЫВАЮЩИЙ библиотеку DLL или приложение.</span><span class="sxs-lookup"><span data-stu-id="5802a-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="5802a-165">Манифест обычно внедряется в исполняемый файл, хотя он может быть предоставлен в виде отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="5802a-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="5802a-166">Манифест содержит такие сведения, как зависимости библиотек DLL, требуемый уровень привилегий и версия Windows, для которой была разработана программа.</span><span class="sxs-lookup"><span data-stu-id="5802a-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="5802a-167">Чтобы объявить, что программа учитывает DPI, включите в манифест следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="5802a-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="5802a-168">Приведенный здесь список является только частичным манифестом, но компоновщик Visual Studio автоматически создает остальную часть манифеста.</span><span class="sxs-lookup"><span data-stu-id="5802a-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="5802a-169">Чтобы включить в проект частичный манифест, выполните следующие действия в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5802a-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="5802a-170">В меню **проект** выберите пункт **свойство**.</span><span class="sxs-lookup"><span data-stu-id="5802a-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="5802a-171">В левой области разверните узел **Свойства конфигурации**, разверните **инструмент манифест**, а затем щелкните **Вход и выход**.</span><span class="sxs-lookup"><span data-stu-id="5802a-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="5802a-172">В текстовом поле **Дополнительные файлы манифеста** введите имя файла манифеста и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5802a-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="5802a-173">Пометив программу как учитывающую DPI, вы сообщаете DWM, что окно приложения не масштабируется.</span><span class="sxs-lookup"><span data-stu-id="5802a-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="5802a-174">Теперь при создании окна 500 × 500 окно будет занимать 500 × 500 пикселей, независимо от значения DPI пользователя.</span><span class="sxs-lookup"><span data-stu-id="5802a-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="5802a-175">GDI и DPI</span><span class="sxs-lookup"><span data-stu-id="5802a-175">GDI and DPI</span></span>

<span data-ttu-id="5802a-176">Рисование GDI измеряется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5802a-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="5802a-177">Это означает, что если программа помечена как совместимая с DPI, и вы запрашиваете GDI для рисования прямоугольника 200 × 100, полученный прямоугольник будет состоять из 200 пикселей в ширину и 100 пикселей в высоту на экране.</span><span class="sxs-lookup"><span data-stu-id="5802a-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="5802a-178">Однако размеры шрифтов GDI масштабируются до текущего значения DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="5802a-179">Иными словами, если вы создадите шрифт 72, размер шрифта будет составлять 96 пикселей в 96 DPI, а 144 пикселей — в 144 DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="5802a-180">Ниже приведен шрифт точки 72, отображаемый в 144 DPI с помощью GDI.</span><span class="sxs-lookup"><span data-stu-id="5802a-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![Диаграмма, показывающая масштабирование шрифтов dpi в GDI.](images/graphics12.png)

<span data-ttu-id="5802a-182">Если в приложении учитывается DPI и для рисования используется GDI, масштабировать все координаты рисования в соответствии с DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="5802a-183">Direct2D и DPI</span><span class="sxs-lookup"><span data-stu-id="5802a-183">Direct2D and DPI</span></span>

<span data-ttu-id="5802a-184">Direct2D автоматически выполняет масштабирование в соответствии с параметром DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="5802a-185">В Direct2D координаты измеряются в единицах, называемых аппаратно *-независимыми пикселями* (DIP).</span><span class="sxs-lookup"><span data-stu-id="5802a-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="5802a-186">DIP определяется как 1 или 1/96 *логического* дюйма.</span><span class="sxs-lookup"><span data-stu-id="5802a-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="5802a-187">В Direct2D все операции рисования задаются в DIP, а затем масштабируются до текущего параметра DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="5802a-188">Масштаб</span><span class="sxs-lookup"><span data-stu-id="5802a-188">DPI setting</span></span> | <span data-ttu-id="5802a-189">Размер DIP</span><span class="sxs-lookup"><span data-stu-id="5802a-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="5802a-190">96</span><span class="sxs-lookup"><span data-stu-id="5802a-190">96</span></span>          | <span data-ttu-id="5802a-191">1 пиксель</span><span class="sxs-lookup"><span data-stu-id="5802a-191">1 pixel</span></span>     |
| <span data-ttu-id="5802a-192">120</span><span class="sxs-lookup"><span data-stu-id="5802a-192">120</span></span>         | <span data-ttu-id="5802a-193">1,25 пикселей</span><span class="sxs-lookup"><span data-stu-id="5802a-193">1.25 pixels</span></span> |
| <span data-ttu-id="5802a-194">144</span><span class="sxs-lookup"><span data-stu-id="5802a-194">144</span></span>         | <span data-ttu-id="5802a-195">1,5 пикселей</span><span class="sxs-lookup"><span data-stu-id="5802a-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="5802a-196">Например, если значение DPI для пользователя равно 144 DPI, и вы запрашиваете Direct2D для прорисовки прямоугольника размером 200 × 100, прямоугольник будет состоять из 300 × 150 физических пикселей.</span><span class="sxs-lookup"><span data-stu-id="5802a-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="5802a-197">Кроме того, DirectWrite измеряет размеры шрифтов в DIP, а не на точках.</span><span class="sxs-lookup"><span data-stu-id="5802a-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="5802a-198">Чтобы создать шрифт размером 12 пунктов, укажите 16 DIP (12 точек = 1/6 логический дюйм = 96/6 DIP).</span><span class="sxs-lookup"><span data-stu-id="5802a-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="5802a-199">Когда текст отображается на экране, Direct2D преобразует DIP в физические Пиксели.</span><span class="sxs-lookup"><span data-stu-id="5802a-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="5802a-200">Преимуществом этой системы является то, что единицы измерения согласуются как для текста, так и для рисования, независимо от текущего значения DPI.</span><span class="sxs-lookup"><span data-stu-id="5802a-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="5802a-201">Предупреждение: координаты мыши и окна по-прежнему задаются в физических пикселях, а не DIP.</span><span class="sxs-lookup"><span data-stu-id="5802a-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="5802a-202">Например, если обрабатывается сообщение [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) , то кнопка мыши задается в физических пикселях.</span><span class="sxs-lookup"><span data-stu-id="5802a-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="5802a-203">Чтобы нарисовать точку в этой позиции, необходимо преобразовать координаты пикселей в DIP.</span><span class="sxs-lookup"><span data-stu-id="5802a-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="5802a-204">Преобразование физических пикселей в DIP</span><span class="sxs-lookup"><span data-stu-id="5802a-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="5802a-205">Преобразование из физических пикселей в DIP использует следующую формулу.</span><span class="sxs-lookup"><span data-stu-id="5802a-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="5802a-206">DIP = Пиксели/(DPI/96.0)</span><span class="sxs-lookup"><span data-stu-id="5802a-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="5802a-207">Чтобы получить значение DPI, вызовите метод [**ID2D1Factory:: жетдесктопдпи**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="5802a-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="5802a-208">Значение DPI возвращается в виде двух значений с плавающей запятой: одно для оси x, а другое для оси y.</span><span class="sxs-lookup"><span data-stu-id="5802a-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="5802a-209">Теоретически эти значения могут различаться.</span><span class="sxs-lookup"><span data-stu-id="5802a-209">In theory, these values can differ.</span></span> <span data-ttu-id="5802a-210">Вычислите отдельный коэффициент масштабирования для каждой оси.</span><span class="sxs-lookup"><span data-stu-id="5802a-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="5802a-211">Ниже приведен альтернативный способ получения значения DPI, если вы не используете Direct2D:</span><span class="sxs-lookup"><span data-stu-id="5802a-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="5802a-212">В Windows 10 версия 1903,  [**ID2D1Factory:: жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) является устаревшей, а рекомендация — [**DisplayInformation:: Логикалдпи**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) для приложений Магазина Windows или [**жетдпифорвиндов**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="5802a-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="5802a-213">Если вы по-прежнему хотите использовать его, отключите сообщение об ошибке компилятора, записав строку [**#pragma warning (подавлять: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) непосредственно перед вызовом [**ID2D1Factory:: жетдесктопдпи**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="5802a-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="5802a-214">Хотя это не рекомендуется, по умолчанию можно задать поддержку по DPI с помощью [**сетпроцессдпиаваренессконтекст**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span><span class="sxs-lookup"><span data-stu-id="5802a-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="5802a-215">После создания окна (HWND) в процессе изменение режима поддержки DPI больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5802a-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="5802a-216">Если вы устанавливаете режим поддержки по умолчанию для обработки точек на дюйм как программно, необходимо вызвать соответствующий API перед созданием дескрипторов HWND.</span><span class="sxs-lookup"><span data-stu-id="5802a-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="5802a-217">Дополнительные сведения см. [в разделе Настройка отслеживания количества точек на дюйм по умолчанию для процесса](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="5802a-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="5802a-218">Изменение размера целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="5802a-218">Resizing the Render Target</span></span>

<span data-ttu-id="5802a-219">Если размер окна изменяется, необходимо изменить размер целевого объекта рендеринга для соответствия.</span><span class="sxs-lookup"><span data-stu-id="5802a-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="5802a-220">В большинстве случаев также потребуется обновить макет и перекрасить окно.</span><span class="sxs-lookup"><span data-stu-id="5802a-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="5802a-221">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5802a-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="5802a-222">Функция [**жетклиентрект**](/windows/desktop/api/winuser/nf-winuser-getclientrect) получает новый размер клиентской области в физических пикселях (не DIP).</span><span class="sxs-lookup"><span data-stu-id="5802a-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="5802a-223">Метод [**ID2D1HwndRenderTarget:: resize**](../direct2d/id2d1hwndrendertarget-resize.md) обновляет размер целевого объекта рендеринга, также заданный в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5802a-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="5802a-224">Функция [**инвалидатерект**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) принудительно выполняет перерисовку, добавляя всю клиентскую область в область обновления окна.</span><span class="sxs-lookup"><span data-stu-id="5802a-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="5802a-225">(См. раздел [Рисование окна](painting-the-window.md)в модуле 1.)</span><span class="sxs-lookup"><span data-stu-id="5802a-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="5802a-226">По мере увеличения или уменьшения размера окна, как правило, необходимо повторно вычислить расположение рисуемых объектов.</span><span class="sxs-lookup"><span data-stu-id="5802a-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="5802a-227">Например, в программе Circle необходимо обновить радиус и центральную точку:</span><span class="sxs-lookup"><span data-stu-id="5802a-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="5802a-228">Метод [**ID2D1RenderTarget:: resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) возвращает размер целевого объекта отрисовки в DIP (не в пикселях), который является подходящим блоком для вычисления макета.</span><span class="sxs-lookup"><span data-stu-id="5802a-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="5802a-229">Существует тесно связанный метод [**ID2D1RenderTarget:: жетпикселсизе**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), который возвращает размер в физических пикселях.</span><span class="sxs-lookup"><span data-stu-id="5802a-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="5802a-230">Для целевого объекта прорисовки **HWND** это значение соответствует размеру, возвращенному [**жетклиентрект**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span><span class="sxs-lookup"><span data-stu-id="5802a-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="5802a-231">Но помните, что рисование выполняется в DIP, а не в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5802a-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="5802a-232">Следующая</span><span class="sxs-lookup"><span data-stu-id="5802a-232">Next</span></span>

[<span data-ttu-id="5802a-233">Использование цвета в Direct2D</span><span class="sxs-lookup"><span data-stu-id="5802a-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
