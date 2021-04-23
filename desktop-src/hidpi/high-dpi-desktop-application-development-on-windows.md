---
title: Разработка приложений с высоким разрешением для настольных систем в Windows
description: Это содержимое предназначено для разработчиков, желающих обновить классические приложения для обработки динамического масштабирования экрана (то есть
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104134719"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="20e3b-103">Разработка приложений с высоким разрешением для настольных систем в Windows</span><span class="sxs-lookup"><span data-stu-id="20e3b-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="20e3b-104">Это содержимое предназначено для разработчиков, желающих обновлять настольные приложения с динамическим изменением масштаба отображения (в точках на дюйм или DPI), что позволяет приложениям быть четкими на отображаемых им дисплеях.</span><span class="sxs-lookup"><span data-stu-id="20e3b-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="20e3b-105">Для начала, если вы создаете новое приложение Windows с нуля, настоятельно рекомендуется создать приложение [универсальная платформа Windows (UWP)](/windows/uwp/get-started/whats-a-uwp) .</span><span class="sxs-lookup"><span data-stu-id="20e3b-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="20e3b-106">Приложения UWP автоматически &mdash; и динамически &mdash; масштабируются для каждого дисплея, на котором они выполняются.</span><span class="sxs-lookup"><span data-stu-id="20e3b-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="20e3b-107">Классические приложения, использующие старые технологии программирования Windows (необработанное программирование Win32, Windows Forms, Windows Presentation Framework (WPF) и т. д.), не могут автоматически управлять масштабированием DPI без дополнительной работы разработчика.</span><span class="sxs-lookup"><span data-stu-id="20e3b-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="20e3b-108">Без такой работы приложения будут выглядеть неразмытыми или неправильными по размеру во многих распространенных сценариях использования.</span><span class="sxs-lookup"><span data-stu-id="20e3b-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="20e3b-109">Этот документ содержит контекст и сведения о том, что происходит при обновлении настольного приложения для корректной визуализации.</span><span class="sxs-lookup"><span data-stu-id="20e3b-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="20e3b-110">Коэффициент масштабирования экрана & DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="20e3b-111">По мере продвижения технологии экранов изготовитель панели монитора упаковывает увеличивающееся число пикселей в каждую единицу физического пространства на своих панелях.</span><span class="sxs-lookup"><span data-stu-id="20e3b-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="20e3b-112">Это привело к тому, что количество точек на дюйм (DPI) современных панелей отображаются намного выше, чем в прошлом.</span><span class="sxs-lookup"><span data-stu-id="20e3b-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="20e3b-113">В прошлом для большинства дисплеев было 96 пикселей на линейный дюйм физического пространства (96 точек на дюйм); в 2017 отображается с почти 300 DPI или выше.</span><span class="sxs-lookup"><span data-stu-id="20e3b-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="20e3b-114">В большинстве устаревших платформ пользовательского интерфейса имеются встроенные предположения о том, что отображаемое значение DPI не изменится в течение времени существования процесса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="20e3b-115">Это предположение больше не имеет значения true, при этом dpi дисплея часто изменяется несколько раз в течение всего времени существования процесса приложения.</span><span class="sxs-lookup"><span data-stu-id="20e3b-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="20e3b-116">Ниже приведены некоторые распространенные сценарии, в которых изменяется коэффициент масштабирования экрана или масштаб DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="20e3b-117">Несколько мониторов настройки, в которых каждый дисплей имеет разный коэффициент масштабирования, и приложение перемещается из одного экрана в другое (например, 4 КБ и 1080p).</span><span class="sxs-lookup"><span data-stu-id="20e3b-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="20e3b-118">Закрепление и Отстыковка ноутбука с высоким DPI и внешним дисплеем с низким разрешением (или наоборот)</span><span class="sxs-lookup"><span data-stu-id="20e3b-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="20e3b-119">Подключение через удаленный рабочий стол с переносным компьютером с высоким разрешением или планшетом к устройству с низким разрешением (или наоборот)</span><span class="sxs-lookup"><span data-stu-id="20e3b-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="20e3b-120">Изменение параметров масштабирования экрана во время выполнения приложений</span><span class="sxs-lookup"><span data-stu-id="20e3b-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="20e3b-121">В этих сценариях приложения UWP автоматически перерисуются для новых точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="20e3b-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="20e3b-122">По умолчанию, и без дополнительных действий разработчика, настольные приложения не работают.</span><span class="sxs-lookup"><span data-stu-id="20e3b-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="20e3b-123">Настольные приложения, которые не выполняют эту лишнюю работу для реагирования на изменения DPI, могут выглядеть неразмытыми или неправильными по размеру пользователю.</span><span class="sxs-lookup"><span data-stu-id="20e3b-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="20e3b-124">Режим поддержки DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-124">DPI Awareness Mode</span></span>

<span data-ttu-id="20e3b-125">Классические приложения должны сообщать Windows, если они поддерживают масштабирование DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="20e3b-126">По умолчанию система считает системные приложения неосведомленными и точечными рисунками, растягивает их окна.</span><span class="sxs-lookup"><span data-stu-id="20e3b-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="20e3b-127">Установив один из следующих доступных режимов определения DPI, приложения могут явно указать Windows, как они хотят управлять масштабированием DPI:</span><span class="sxs-lookup"><span data-stu-id="20e3b-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="20e3b-128">Неосведомленность DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-128">DPI Unaware</span></span>

<span data-ttu-id="20e3b-129">Независимые от DPI приложения отправляются по фиксированному значению DPI, равному 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="20e3b-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="20e3b-130">Когда эти приложения выполняются на экране с масштабом отображения более 96 DPI, Windows растягивает точечный рисунок приложения на ожидаемый физический размер.</span><span class="sxs-lookup"><span data-stu-id="20e3b-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="20e3b-131">В результате приложение поменяет размытые.</span><span class="sxs-lookup"><span data-stu-id="20e3b-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="20e3b-132">Осведомленность о DPI системы</span><span class="sxs-lookup"><span data-stu-id="20e3b-132">System DPI Awareness</span></span>

<span data-ttu-id="20e3b-133">Настольные приложения, для которых учитывается контроль использования систем, обычно получают DPI основного подключенного монитора на момент входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="20e3b-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="20e3b-134">Во время инициализации они размечают пользовательский интерфейс соответствующим образом (размеры элементов управления, выбор размера шрифтов, загрузка ресурсов и т. д.), используя значение DPI системы.</span><span class="sxs-lookup"><span data-stu-id="20e3b-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="20e3b-135">Таким образом, для приложений, поддерживающих DPI, масштабирование не масштабируется (точечный рисунок растягивается) в Windows при отображении с одним DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="20e3b-136">При перемещении приложения на дисплей с другим коэффициентом масштабирования или при изменении коэффициента масштабирования изображения Windows будет масштабировать окна приложения, делая их нечеткими.</span><span class="sxs-lookup"><span data-stu-id="20e3b-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="20e3b-137">Фактически, системные приложения, поддерживающие DPI, разрабатываются только в одном масштабе экрана, поэтому при каждом изменении DPI становится размытым.</span><span class="sxs-lookup"><span data-stu-id="20e3b-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="20e3b-138">Поддержка Per-Monitor и Per-Monitor (v2) DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="20e3b-139">Рекомендуется, чтобы настольные приложения были обновлены для использования режима отслеживания DPI для каждого монитора, что позволяет им правильно визуализироваться при изменении DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="20e3b-140">Когда приложение сообщает Windows, что оно требуется для работы в этом режиме, Windows не будет растягивать приложение при изменении DPI, вместо этого отправляя [WM \_ DPICHANGED](wm-dpichanged.md) в окно приложения.</span><span class="sxs-lookup"><span data-stu-id="20e3b-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="20e3b-141">После этого выполняется полная ответственность приложения по изменению размера для нового DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="20e3b-142">Большинство платформ пользовательского интерфейса, используемых для классических приложений (общие элементы управления Windows (Comctl32), Windows Forms, Windows Presentation Framework и т. д.), не поддерживают автоматическое масштабирование DPI, поэтому разработчикам нужно изменять размер и расположение содержимого своих окон.</span><span class="sxs-lookup"><span data-stu-id="20e3b-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="20e3b-143">Существует две версии Per-Monitor осведомленности о том, что приложение может зарегистрировать себя как: версии 1 и версии 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="20e3b-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="20e3b-144">Регистрация процесса, выполняемого в режиме PMv2 осведомленности, приводит к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="20e3b-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="20e3b-145">Приложение получает уведомления при изменении DPI (как для верхнего уровня, так и для дочернего HWND)</span><span class="sxs-lookup"><span data-stu-id="20e3b-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="20e3b-146">Приложение видит необработанные пиксели каждого дисплея</span><span class="sxs-lookup"><span data-stu-id="20e3b-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="20e3b-147">Приложение не масштабируется с помощью точечного рисунка Windows</span><span class="sxs-lookup"><span data-stu-id="20e3b-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="20e3b-148">Автоматическая неклиентская область (заголовок окна, полосы прокрутки и т. д.) Масштабирование DPI по Windows</span><span class="sxs-lookup"><span data-stu-id="20e3b-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="20e3b-149">Диалоговые окна Win32 (от [креатедиалог](/windows/desktop/api/winuser/nf-winuser-createdialogw)) автоматически масштабируются по Windows</span><span class="sxs-lookup"><span data-stu-id="20e3b-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="20e3b-150">Графические ресурсы, отображаемые темой в стандартных элементах управления (флажки, фон кнопки и т. д.), автоматически подготавливаются в соответствии с коэффициентом масштабирования DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="20e3b-151">При работе в режиме поддержки Per-Monitor v2 приложения уведомляются при изменении их DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="20e3b-152">Если приложение не изменяет размер для нового DPI, Пользовательский интерфейс приложения будет отображаться слишком маленьким или слишком большим (в зависимости от различий в предыдущем и новом значениях DPI).</span><span class="sxs-lookup"><span data-stu-id="20e3b-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="20e3b-153">Поддержка Per-Monitor v1 (PMv1) очень ограничена.</span><span class="sxs-lookup"><span data-stu-id="20e3b-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="20e3b-154">Рекомендуется, чтобы приложения использовали PMv2.</span><span class="sxs-lookup"><span data-stu-id="20e3b-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="20e3b-155">В следующей таблице показано, как приложения будут отображаться в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="20e3b-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20e3b-156">Режим поддержки DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="20e3b-157">Появившаяся версия Windows</span><span class="sxs-lookup"><span data-stu-id="20e3b-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="20e3b-158">Представление DPI приложения</span><span class="sxs-lookup"><span data-stu-id="20e3b-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="20e3b-159">Поведение при изменении DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20e3b-160">Связан</span><span class="sxs-lookup"><span data-stu-id="20e3b-160">Unaware</span></span></td>
<td><span data-ttu-id="20e3b-161">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-161">N/A</span></span></td>
<td><span data-ttu-id="20e3b-162">Все дисплеи имеют 96 точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="20e3b-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="20e3b-163">Точечный рисунок-растяжение (размытые)</span><span class="sxs-lookup"><span data-stu-id="20e3b-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20e3b-164">Система</span><span class="sxs-lookup"><span data-stu-id="20e3b-164">System</span></span></td>
<td><span data-ttu-id="20e3b-165">Vista</span><span class="sxs-lookup"><span data-stu-id="20e3b-165">Vista</span></span></td>
<td><span data-ttu-id="20e3b-166">Все дисплеи имеют одинаковое разрешение DPI (DPI основного отображения на момент запуска текущего сеанса пользователя).</span><span class="sxs-lookup"><span data-stu-id="20e3b-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="20e3b-167">Точечный рисунок-растяжение (размытые)</span><span class="sxs-lookup"><span data-stu-id="20e3b-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20e3b-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="20e3b-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="20e3b-169">8.1</span><span class="sxs-lookup"><span data-stu-id="20e3b-169">8.1</span></span></td>
<td><span data-ttu-id="20e3b-170">DPI дисплея, на котором в основном находится окно приложения</span><span class="sxs-lookup"><span data-stu-id="20e3b-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="20e3b-171">HWND верхнего уровня уведомляется об изменении DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="20e3b-172">Масштабирование элементов пользовательского интерфейса без разрешения.</span><span class="sxs-lookup"><span data-stu-id="20e3b-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20e3b-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="20e3b-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="20e3b-174">Обновление Windows 10 для дизайнеров (1703)</span><span class="sxs-lookup"><span data-stu-id="20e3b-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="20e3b-175">DPI дисплея, на котором в основном находится окно приложения</span><span class="sxs-lookup"><span data-stu-id="20e3b-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="20e3b-176">Дескрипторы HWND верхнего уровня <span class="underline">и</span> дочерние окна получают уведомления об изменении dpi</span><span class="sxs-lookup"><span data-stu-id="20e3b-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="20e3b-177"><span class="underline">Автоматическое масштабирование в масштабе:</span>
</span><span class="sxs-lookup"><span data-stu-id="20e3b-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="20e3b-178">Неклиентская область</span><span class="sxs-lookup"><span data-stu-id="20e3b-178">Non-client area</span></span></li>
<li><span data-ttu-id="20e3b-179">Отображаемые в теме точечные рисунки в общих элементах управления (Comctl32 V6)</span><span class="sxs-lookup"><span data-stu-id="20e3b-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="20e3b-180">Диалоговые окна (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">креатедиалог</a>)</span><span class="sxs-lookup"><span data-stu-id="20e3b-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="20e3b-181">Отслеживание количества точек на дюйм (v1)</span><span class="sxs-lookup"><span data-stu-id="20e3b-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="20e3b-182">Режим поддержки Per-Monitor v1 DPI (PMv1) появился в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="20e3b-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="20e3b-183">Этот режим поддержки DPI очень ограничен и предлагает только перечисленные ниже функции.</span><span class="sxs-lookup"><span data-stu-id="20e3b-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="20e3b-184">Рекомендуется, чтобы классические приложения использовали режим поддержки Per-Monitor v2, поддерживаемый в Windows 10 1703 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="20e3b-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="20e3b-185">Начальная поддержка, предоставляемая для каждого монитора, предоставляет только следующие приложения:</span><span class="sxs-lookup"><span data-stu-id="20e3b-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="20e3b-186">HWND верхнего уровня получают уведомления об изменении DPI и предоставили новый предлагаемый размер.</span><span class="sxs-lookup"><span data-stu-id="20e3b-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="20e3b-187">Windows не будет растягивать пользовательский интерфейс приложения</span><span class="sxs-lookup"><span data-stu-id="20e3b-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="20e3b-188">Приложение видит все экраны в физических точках (см. виртуализацию).</span><span class="sxs-lookup"><span data-stu-id="20e3b-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="20e3b-189">В Windows 10 1607 или более поздних версиях PMv1 приложения могут также вызвать [енабленонклиентдпискалинг](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) во время \_ работы WM нккреате, чтобы запросить правильное масштабирование Windows в неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="20e3b-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="20e3b-190">Поддержка масштабирования DPI на уровне по платформам и технологиям пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="20e3b-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="20e3b-191">В таблице ниже показан уровень поддержки DPI для каждого монитора, предлагаемый различными платформами пользовательского интерфейса Windows на основе Windows 10 1703:</span><span class="sxs-lookup"><span data-stu-id="20e3b-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20e3b-192">Платформа и технология</span><span class="sxs-lookup"><span data-stu-id="20e3b-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="20e3b-193">Поддержка</span><span class="sxs-lookup"><span data-stu-id="20e3b-193">Support</span></span></th>
<th><span data-ttu-id="20e3b-194">Сценарий</span><span class="sxs-lookup"><span data-stu-id="20e3b-194">OS Version</span></span></th>
<th><span data-ttu-id="20e3b-195">Масштабирование DPI, обрабатываемое</span><span class="sxs-lookup"><span data-stu-id="20e3b-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="20e3b-196">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="20e3b-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20e3b-197">Универсальная платформа Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="20e3b-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="20e3b-198">Полное</span><span class="sxs-lookup"><span data-stu-id="20e3b-198">Full</span></span></td>
<td><span data-ttu-id="20e3b-199">1607</span><span class="sxs-lookup"><span data-stu-id="20e3b-199">1607</span></span></td>
<td><span data-ttu-id="20e3b-200">Платформа пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="20e3b-200">UI framework</span></span></td>
<td><span data-ttu-id="20e3b-201"><a href="/windows/uwp/get-started/whats-a-uwp">Универсальная платформа Windows (UWP)</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20e3b-202">Необработанные элементы управления Win32/Common Controls V6 (comctl32.dll)</span><span class="sxs-lookup"><span data-stu-id="20e3b-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="20e3b-203">Уведомления об изменении DPI, отправленные всем дескрипторам HWND</span><span class="sxs-lookup"><span data-stu-id="20e3b-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="20e3b-204">Графические ресурсы, рисуемые темами, правильно отображаются в общих элементах управления</span><span class="sxs-lookup"><span data-stu-id="20e3b-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="20e3b-205">Автоматическое масштабирование точек на дюйм для диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="20e3b-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="20e3b-206">1703</span><span class="sxs-lookup"><span data-stu-id="20e3b-206">1703</span></span></td>
<td><span data-ttu-id="20e3b-207">Приложение</span><span class="sxs-lookup"><span data-stu-id="20e3b-207">Application</span></span></td>
<td><span data-ttu-id="20e3b-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Пример GitHub</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20e3b-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="20e3b-209">Windows Forms</span></span></td>
<td><span data-ttu-id="20e3b-210">Для некоторых элементов управления ограничено автоматическое масштабирование DPI для каждого монитора</span><span class="sxs-lookup"><span data-stu-id="20e3b-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="20e3b-211">1703</span><span class="sxs-lookup"><span data-stu-id="20e3b-211">1703</span></span></td>
<td><span data-ttu-id="20e3b-212">Платформа пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="20e3b-212">UI framework</span></span></td>
<td><span data-ttu-id="20e3b-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Поддержка высокого DPI в Windows Forms</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20e3b-214">Windows Presentation Foundation (WPF)</span><span class="sxs-lookup"><span data-stu-id="20e3b-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="20e3b-215">В собственных приложениях WPF масштабирование WPF, размещенное в других платформах, и другие платформы, размещенные в WPF, не масштабируются автоматически</span><span class="sxs-lookup"><span data-stu-id="20e3b-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="20e3b-216">1607</span><span class="sxs-lookup"><span data-stu-id="20e3b-216">1607</span></span></td>
<td><span data-ttu-id="20e3b-217">Платформа пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="20e3b-217">UI framework</span></span></td>
<td><span data-ttu-id="20e3b-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Пример GitHub</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20e3b-219">GDI</span><span class="sxs-lookup"><span data-stu-id="20e3b-219">GDI</span></span></td>
<td><span data-ttu-id="20e3b-220">Нет</span><span class="sxs-lookup"><span data-stu-id="20e3b-220">None</span></span></td>
<td><span data-ttu-id="20e3b-221">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-221">N/A</span></span></td>
<td><span data-ttu-id="20e3b-222">Приложение</span><span class="sxs-lookup"><span data-stu-id="20e3b-222">Application</span></span></td>
<td><span data-ttu-id="20e3b-223">См. раздел <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">масштабирование с высоким разрешением GDI</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20e3b-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="20e3b-224">GDI+</span></span></td>
<td><span data-ttu-id="20e3b-225">Нет</span><span class="sxs-lookup"><span data-stu-id="20e3b-225">None</span></span></td>
<td><span data-ttu-id="20e3b-226">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-226">N/A</span></span></td>
<td><span data-ttu-id="20e3b-227">Приложение</span><span class="sxs-lookup"><span data-stu-id="20e3b-227">Application</span></span></td>
<td><span data-ttu-id="20e3b-228">См. раздел <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">масштабирование с высоким разрешением GDI</a></span><span class="sxs-lookup"><span data-stu-id="20e3b-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20e3b-229">MFC</span><span class="sxs-lookup"><span data-stu-id="20e3b-229">MFC</span></span></td>
<td><span data-ttu-id="20e3b-230">Нет</span><span class="sxs-lookup"><span data-stu-id="20e3b-230">None</span></span></td>
<td><span data-ttu-id="20e3b-231">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-231">N/A</span></span></td>
<td><span data-ttu-id="20e3b-232">Приложение</span><span class="sxs-lookup"><span data-stu-id="20e3b-232">Application</span></span></td>
<td><span data-ttu-id="20e3b-233">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="20e3b-234">Обновление существующих приложений</span><span class="sxs-lookup"><span data-stu-id="20e3b-234">Updating Existing Applications</span></span>

<span data-ttu-id="20e3b-235">Чтобы обновить существующее настольное приложение для правильной обработки масштабирования DPI, необходимо обновить таким образом, что, как минимум, важные части его пользовательского интерфейса обновляются для реагирования на изменения DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="20e3b-236">Большинство настольных приложений выполняются в режиме поддержки DPI системы.</span><span class="sxs-lookup"><span data-stu-id="20e3b-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="20e3b-237">Приложения, поддерживающие DPI, обычно масштабируются до точек на дюйм основного дисплея (экран, на котором была размещена системная область на момент запуска сеанса Windows).</span><span class="sxs-lookup"><span data-stu-id="20e3b-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="20e3b-238">При изменении DPI Windows будет растягивать пользовательский интерфейс этих приложений, что часто приводит к неразмытости.</span><span class="sxs-lookup"><span data-stu-id="20e3b-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="20e3b-239">При обновлении приложения, поддерживающего разрешение на уровне системы, для того, чтобы иметь возможность учитывать разрешение на контроль DPI, код, обрабатывающий макет пользовательского интерфейса, должен быть обновлен таким, что он выполняется не только во время инициализации приложения, но и при каждом получении уведомления об изменении DPI ([WM \_ DPICHANGED](wm-dpichanged.md) в случае Win32).</span><span class="sxs-lookup"><span data-stu-id="20e3b-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="20e3b-240">Обычно это подразумевает повторное посещение любых допущений в коде, которые необходимо масштабировать в пользовательском интерфейсе только один раз.</span><span class="sxs-lookup"><span data-stu-id="20e3b-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="20e3b-241">Кроме того, в случае программирования на Win32 многие API-интерфейсы Win32 не имеют разрешения на разрешение или контекст отображения, поэтому они будут возвращать только значения, относящиеся к DPI системы.</span><span class="sxs-lookup"><span data-stu-id="20e3b-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="20e3b-242">Можно использовать grep в коде для поиска некоторых из этих API и замены их вариантами, поддерживающими DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="20e3b-243">Ниже перечислены некоторые из распространенных API-интерфейсов с поддержкой DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="20e3b-244">Версия с одним DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-244">Single DPI version</span></span>   | <span data-ttu-id="20e3b-245">Версия Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="20e3b-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="20e3b-246">жетсистемметрикс</span><span class="sxs-lookup"><span data-stu-id="20e3b-246">GetSystemMetrics</span></span>     | <span data-ttu-id="20e3b-247">жетсистемметриксфордпи</span><span class="sxs-lookup"><span data-stu-id="20e3b-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="20e3b-248">аджуствиндовректекс</span><span class="sxs-lookup"><span data-stu-id="20e3b-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="20e3b-249">аджуствиндовректексфордпи</span><span class="sxs-lookup"><span data-stu-id="20e3b-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="20e3b-250">системпараметерсинфо</span><span class="sxs-lookup"><span data-stu-id="20e3b-250">SystemParametersInfo</span></span> | <span data-ttu-id="20e3b-251">системпараметерсинфофордпи</span><span class="sxs-lookup"><span data-stu-id="20e3b-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="20e3b-252">жетдпиформонитор</span><span class="sxs-lookup"><span data-stu-id="20e3b-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="20e3b-253">жетдпифорвиндов</span><span class="sxs-lookup"><span data-stu-id="20e3b-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="20e3b-254">Также рекомендуется искать жестко закодированные размеры в базе кода, которые предполагают постоянное разрешение DPI, заменяя их кодом, который правильно задается для масштабирования DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="20e3b-255">Ниже приведен пример, включающий все эти рекомендации:</span><span class="sxs-lookup"><span data-stu-id="20e3b-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="20e3b-256">Пример.</span><span class="sxs-lookup"><span data-stu-id="20e3b-256">Example:</span></span>

<span data-ttu-id="20e3b-257">В примере ниже показан упрощенный вариант Win32 для создания дочернего HWND.</span><span class="sxs-lookup"><span data-stu-id="20e3b-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="20e3b-258">При вызове CreateWindow предполагается, что приложение выполняется в 96 DPI, и ни размер кнопки, ни ее расположение не будут правильными на более высоком DPI:</span><span class="sxs-lookup"><span data-stu-id="20e3b-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="20e3b-259">В обновленном коде показано следующее:</span><span class="sxs-lookup"><span data-stu-id="20e3b-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="20e3b-260">Значение DPI для кода при создании окна. масштабирование расположения и размера дочернего HWND для DPI родительского окна</span><span class="sxs-lookup"><span data-stu-id="20e3b-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="20e3b-261">Реагирование на изменение DPI путем изменения расположения и изменения размера дочернего HWND</span><span class="sxs-lookup"><span data-stu-id="20e3b-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="20e3b-262">Жестко запрограммированные размеры удалены и заменены кодом, который реагирует на изменения DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="20e3b-263">При обновлении приложения, поддерживающего DPI, необходимо выполнить следующие общие действия.</span><span class="sxs-lookup"><span data-stu-id="20e3b-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="20e3b-264">Пометьте процесс как учитывающий DPI для каждого монитора (v2) с помощью манифеста приложения (или другого метода в зависимости от используемых платформ пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="20e3b-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="20e3b-265">Сделать логику макета пользовательского интерфейса повторно используемой и переместить ее из кода инициализации приложения таким, что ее можно использовать повторно при изменении DPI (WM \_ DPICHANGED в случае программирования Windows (Win32)).</span><span class="sxs-lookup"><span data-stu-id="20e3b-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="20e3b-266">Делает недействительным код, который предполагает, что данные, учитывающие значение DPI (DPI/шрифты/размер и т. д.), не нуждаются в обновлении.</span><span class="sxs-lookup"><span data-stu-id="20e3b-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="20e3b-267">Очень часто рекомендуется кэшировать размеры шрифтов и значения DPI при инициализации процесса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="20e3b-268">При обновлении приложения для отслеживания DPI для каждого монитора данные, учитывающие DPI, необходимо переоценивать при каждом обнаружении нового DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="20e3b-269">Когда происходит изменение DPI, перезагрузите (или восстановите) все ресурсы растрового изображения для нового DPI или, при необходимости, растягивание выделенных ресурсов до нужного размера.</span><span class="sxs-lookup"><span data-stu-id="20e3b-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="20e3b-270">Grep для API, которые не Per-Monitor учитывать DPI и заменяют Per-Monitor API-интерфейсами, поддерживающими DPI (где применимо).</span><span class="sxs-lookup"><span data-stu-id="20e3b-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="20e3b-271">Пример. Замените Жетсистемметрикс на Жетсистемметриксфордпи.</span><span class="sxs-lookup"><span data-stu-id="20e3b-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="20e3b-272">Протестируйте приложение в системе с множественным отображением или с несколькими DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="20e3b-273">Для всех окон верхнего уровня в приложении, которые не удается обновить до масштабного масштабирования, используйте масштабирование в смешанном режиме (как описано ниже), чтобы разрешить растягивание этих окон верхнего уровня системой.</span><span class="sxs-lookup"><span data-stu-id="20e3b-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="20e3b-274">Масштабирование Mixed-Mode DPI (масштабирование для дочерних процессов)</span><span class="sxs-lookup"><span data-stu-id="20e3b-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="20e3b-275">При обновлении приложения для поддержки отслеживания DPI на уровне отдельных мониторов иногда может стать непрактичным или невозможно обновить каждое окно в приложении в течение одного пути.</span><span class="sxs-lookup"><span data-stu-id="20e3b-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="20e3b-276">Это может быть просто из-за времени и усилий, необходимых для обновления и тестирования любого пользовательского интерфейса, или потому, что вы не владеете кодом пользовательского интерфейса, который необходимо запустить (если приложение может загружать сторонний пользовательский интерфейс).</span><span class="sxs-lookup"><span data-stu-id="20e3b-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="20e3b-277">В таких ситуациях Windows предлагает способ для упрощения поддержки каждого монитора, позволяя запускать некоторые из окон приложений (только на верхнем уровне) в первоначальном режиме с отслеживанием DPI, в то время как вы хотите сосредоточиться на времени и энергопотреблении, обновив более важные части пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="20e3b-278">Ниже показано, как это может выглядеть. вы обновляете пользовательский интерфейс основного приложения ("главное окно" на рисунке), чтобы запускать с отслеживанием DPI для каждого монитора во время работы других окон в существующем режиме ("дополнительное окно").</span><span class="sxs-lookup"><span data-stu-id="20e3b-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![различия в масштабировании dpi между режимами осведомленности](images/hub-page-illustrations.png)

<span data-ttu-id="20e3b-280">До наступления годовщины Windows 10 (1607) режим поддержки DPI для процесса был свойством на уровне всего процесса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="20e3b-281">Начиная с годовщины Windows 10, это свойство теперь можно установить для каждого окна **верхнего уровня** .</span><span class="sxs-lookup"><span data-stu-id="20e3b-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="20e3b-282">(**Дочерние** окна должны по-прежнему соответствовать размеру масштабирования своего родителя.) Окно верхнего уровня определяется как окно без родителя.</span><span class="sxs-lookup"><span data-stu-id="20e3b-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="20e3b-283">Обычно это «обычное» окно с кнопками сворачивания, развертывания и закрытия.</span><span class="sxs-lookup"><span data-stu-id="20e3b-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="20e3b-284">Сценарий, для которого предназначена подсистема отслеживания DPI, предназначен для того, чтобы использовать вторичный пользовательский интерфейс, масштабируемый по Windows (растянутый точечный рисунок), чтобы сосредоточиться на времени и ресурсах по обновлению основного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="20e3b-285">Чтобы включить осведомленность о МАСШТАБе подпроцессов, вызовите [**сетсреаддпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) до и после любых вызовов создания окна.</span><span class="sxs-lookup"><span data-stu-id="20e3b-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="20e3b-286">Созданное окно будет связано с осведомленностью о DPI, заданной с помощью Сетсреаддпиаваренессконтекст.</span><span class="sxs-lookup"><span data-stu-id="20e3b-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="20e3b-287">Используйте второй вызов для восстановления сведений о текущем потоке DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="20e3b-288">При использовании масштабирования с масштабированием подпроцессов можно полагаться на Windows для выполнения некоторых задач масштабирования DPI в приложении, что может повысить сложность приложения.</span><span class="sxs-lookup"><span data-stu-id="20e3b-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="20e3b-289">Важно понимать недостатки этого подхода и природы сложностей, которые он представляет.</span><span class="sxs-lookup"><span data-stu-id="20e3b-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="20e3b-290">Дополнительные сведения о поддержке дочерних процессов см. в разделе [масштабирование DPI в смешанном режиме и API с поддержкой точек на дюйм.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="20e3b-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="20e3b-291">Тестирование изменений</span><span class="sxs-lookup"><span data-stu-id="20e3b-291">Testing Your Changes</span></span>

<span data-ttu-id="20e3b-292">После обновления приложения для обеспечения отслеживания DPI для каждого монитора важно убедиться, что приложение правильно отвечает на изменения DPI в среде со смешанным разрешением.</span><span class="sxs-lookup"><span data-stu-id="20e3b-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="20e3b-293">Ниже приведены некоторые особенности тестирования.</span><span class="sxs-lookup"><span data-stu-id="20e3b-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="20e3b-294">Перемещение окон приложений между дисплеями различных значений DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="20e3b-295">Запуск приложения с отображением различных значений DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="20e3b-296">Изменение коэффициента масштабирования для монитора во время работы приложения</span><span class="sxs-lookup"><span data-stu-id="20e3b-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="20e3b-297">Изменение экрана, используемого в качестве основного дисплея, _выход из Windows_ и повторное тестирование приложения после повторного входа.</span><span class="sxs-lookup"><span data-stu-id="20e3b-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="20e3b-298">Это особенно полезно при поиске кода, который использует жестко запрограммированные размеры и размеры.</span><span class="sxs-lookup"><span data-stu-id="20e3b-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="20e3b-299">Распространенные ошибки (Win32)</span><span class="sxs-lookup"><span data-stu-id="20e3b-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="20e3b-300">**Не используйте предлагаемый прямоугольник, предоставленный в WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="20e3b-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="20e3b-301">Когда Windows отправляет окно приложения в виде сообщения [**WM \_ DPICHANGED**](wm-dpichanged.md) , это сообщение содержит предлагаемый прямоугольник, который следует использовать для изменения размера окна.</span><span class="sxs-lookup"><span data-stu-id="20e3b-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="20e3b-302">Очень важно, чтобы приложение использовало этот прямоугольник для изменения размера, как это будет:</span><span class="sxs-lookup"><span data-stu-id="20e3b-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="20e3b-303">Убедитесь, что курсор мыши остается в той же относительной позиции в окне при перетаскивании между дисплеями</span><span class="sxs-lookup"><span data-stu-id="20e3b-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="20e3b-304">Запрещает окну приложения переходить в цикл рекурсивного разрешения на изменение, при котором одно изменение DPI активирует последующее изменение DPI, которое активирует еще одно изменение DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="20e3b-305">Если у вас есть требования для конкретного приложения, которые не позволяют использовать предлагаемый прямоугольник, предоставляемый Windows в \_ сообщении WM DPICHANGED, см. раздел [**WM \_ жетдпискаледсизе**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="20e3b-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="20e3b-306">Это сообщение можно использовать, чтобы дать Windows желаемый размер, который вы хотите использовать после изменения DPI, при этом устраняя проблемы, описанные выше.</span><span class="sxs-lookup"><span data-stu-id="20e3b-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="20e3b-307">**Нехватка документации по виртуализации**</span><span class="sxs-lookup"><span data-stu-id="20e3b-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="20e3b-308">Если HWND или процесс выполняется как не учитывающее DPI или учитывается DPI системы, это может быть растянутым изображением Windows.</span><span class="sxs-lookup"><span data-stu-id="20e3b-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="20e3b-309">В этом случае Windows масштабирует и преобразует конфиденциальную информацию из некоторых API в пространство координат вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="20e3b-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="20e3b-310">Например, если поток, не поддерживающий DPI, запрашивает размер экрана при выполнении на дисплее с высоким разрешением, Windows будет виртуализировать ответ, предоставленный приложению, как если бы экран находился в единицах с 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="20e3b-311">Кроме того, если поток с поддержкой DPI в системе взаимодействует с дисплеем с отображением на разных точках на дюйм, чем при запуске текущего пользователя, Windows проведет масштабирование некоторых вызовов API в пространстве координат, которое будет использоваться HWND, если оно было запущено в исходном коэффициенте масштабирования DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="20e3b-312">При правильном обновлении настольного приложения до масштаба DPI может быть трудно определить, какие вызовы API могут возвращать виртуализированные значения на основе контекста потока. Эта информация в настоящее время не предназначена для документирования корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="20e3b-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="20e3b-313">Имейте в виду, что при вызове любого системного API из контекста потока, поддерживающего DPI или DPI, возвращаемое значение может быть виртуализированным.</span><span class="sxs-lookup"><span data-stu-id="20e3b-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="20e3b-314">Таким образом, убедитесь, что ваш поток выполняется в контексте DPI, который вы ждете при взаимодействии с экраном или отдельными окнами.</span><span class="sxs-lookup"><span data-stu-id="20e3b-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="20e3b-315">При временном изменении контекста DPI потока с помощью [сетсреаддпиаваренессконтекст](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)обязательно восстановите старый контекст, чтобы избежать возникновения неправильного поведения в других приложениях.</span><span class="sxs-lookup"><span data-stu-id="20e3b-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="20e3b-316">**Многие API Windows не имеют контекста DPI**</span><span class="sxs-lookup"><span data-stu-id="20e3b-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="20e3b-317">Многие устаревшие API Windows не включают в себя контекст DPI или HWND в составе своего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="20e3b-318">В результате разработчики часто должны выполнить дополнительную работу по масштабированию любых данных, зависящих от DPI, таких как размеры, точки или значки.</span><span class="sxs-lookup"><span data-stu-id="20e3b-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="20e3b-319">Например, разработчики, использующие [лоадикон](/windows/desktop/api/winuser/nf-winuser-loadiconw) , должны либо загружать значки растровых изображений, либо использовать альтернативные API для загрузки значков правильного размера для соответствующих точек на дюйм, например [лоадимаже](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span><span class="sxs-lookup"><span data-stu-id="20e3b-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="20e3b-320">**Принудительный сброс поддержки DPI в масштабе процесса**</span><span class="sxs-lookup"><span data-stu-id="20e3b-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="20e3b-321">Как правило, режим поддержки DPI для процесса не может быть изменен после инициализации процесса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="20e3b-322">Однако Windows может принудительно изменить режим поддержки DPI для процесса, если попытаться разорвать требование, чтобы все дескрипторы HWND в дереве окон имели одинаковый режим поддержки DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="20e3b-323">Во всех версиях Windows, начиная с Windows 10 1703, невозможно использовать различные дескрипторы HWND в дереве HWND в разных режимах определения DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="20e3b-324">При попытке создать отношение дочернего родителя, которое прерывает это правило, можно сбросить сведения о DPI для всего процесса.</span><span class="sxs-lookup"><span data-stu-id="20e3b-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="20e3b-325">Это можно активировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="20e3b-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="20e3b-326">Вызов CreateWindow, в котором переданное родительское окно находится в режиме, отличном от DPI вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="20e3b-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="20e3b-327">Вызов Сетпарент, в котором два окна связаны с различными режимами определения DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="20e3b-328">В таблице ниже показано, что происходит при попытке нарушения этого правила:</span><span class="sxs-lookup"><span data-stu-id="20e3b-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="20e3b-329">Операция</span><span class="sxs-lookup"><span data-stu-id="20e3b-329">Operation</span></span>                 | <span data-ttu-id="20e3b-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="20e3b-330">Windows 8.1</span></span>                                  | <span data-ttu-id="20e3b-331">Windows 10 (1607 и более ранние версии)</span><span class="sxs-lookup"><span data-stu-id="20e3b-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="20e3b-332">Windows 10 (1703 и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="20e3b-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="20e3b-333">CreateWindow (in-proc)</span><span class="sxs-lookup"><span data-stu-id="20e3b-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="20e3b-334">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-334">N/A</span></span>                                          | <span data-ttu-id="20e3b-335">**Дочерние наследуемые** (смешанный режим)</span><span class="sxs-lookup"><span data-stu-id="20e3b-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="20e3b-336">**Дочерние наследуемые** (смешанный режим)</span><span class="sxs-lookup"><span data-stu-id="20e3b-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="20e3b-337">CreateWindow (Cross-proc)</span><span class="sxs-lookup"><span data-stu-id="20e3b-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="20e3b-338">**Принудительный сброс** (для процесса вызывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="20e3b-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="20e3b-339">**Дочерние наследуемые** (смешанный режим)</span><span class="sxs-lookup"><span data-stu-id="20e3b-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="20e3b-340">**Принудительный сброс** (для процесса вызывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="20e3b-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="20e3b-341">Сетпарент (in-proc)</span><span class="sxs-lookup"><span data-stu-id="20e3b-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="20e3b-342">Н/Д</span><span class="sxs-lookup"><span data-stu-id="20e3b-342">N/A</span></span>                                          | <span data-ttu-id="20e3b-343">**Принудительный сброс** (для текущего процесса)</span><span class="sxs-lookup"><span data-stu-id="20e3b-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="20e3b-344">**Fail** (ошибка \_ недопустимое \_ состояние)</span><span class="sxs-lookup"><span data-stu-id="20e3b-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="20e3b-345">Сетпарент (Cross-proc)</span><span class="sxs-lookup"><span data-stu-id="20e3b-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="20e3b-346">**Принудительный сброс** (для процесса дочернего окна)</span><span class="sxs-lookup"><span data-stu-id="20e3b-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="20e3b-347">**Принудительный сброс** (для процесса дочернего окна)</span><span class="sxs-lookup"><span data-stu-id="20e3b-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="20e3b-348">**Принудительный сброс** (для процесса дочернего окна)</span><span class="sxs-lookup"><span data-stu-id="20e3b-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="20e3b-349">См. также</span><span class="sxs-lookup"><span data-stu-id="20e3b-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e3b-350">Справочник по API с высоким DPI</span><span class="sxs-lookup"><span data-stu-id="20e3b-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="20e3b-351">Масштабирование DPI в смешанном режиме и API с поддержкой DPI.</span><span class="sxs-lookup"><span data-stu-id="20e3b-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

