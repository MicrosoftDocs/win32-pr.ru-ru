---
description: См. сочетание одного или нескольких флагов, управляющих поведением при создании устройства в константе D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011287"
---
# <a name="d3dcreate"></a><span data-ttu-id="cd030-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="cd030-103">D3DCREATE</span></span>

<span data-ttu-id="cd030-104">Сочетание одного или нескольких флагов, управляющих поведением при создании устройства.</span><span class="sxs-lookup"><span data-stu-id="cd030-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd030-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="cd030-105">#define</span></span></td>
<td><span data-ttu-id="cd030-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cd030-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="cd030-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="cd030-108">Приложение запрашивает у устройства все головки, которыми владеет этот главный адаптер.</span><span class="sxs-lookup"><span data-stu-id="cd030-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="cd030-109">Недопустимый флаг для неосновных адаптеров.</span><span class="sxs-lookup"><span data-stu-id="cd030-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="cd030-110">Если этот флаг установлен, параметры представления, передаваемые в <a href="/windows/desktop/api"><strong>креатедевице</strong></a> , должны указывать на массив <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cd030-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="cd030-111">Число элементов в <strong>D3DPRESENT_PARAMETERS</strong> должно равняться количеству адаптеров, определенных элементом Нумберофадаптерсинграуп структуры <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd030-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="cd030-112">Среда выполнения DirectX присвоит каждому элементу каждый заголовок в числовом порядке, указанном элементом Адаптерординалинграуп <strong>D3DCAPS9</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd030-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="cd030-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="cd030-114">Direct3D будет управлять ресурсами вместо драйвера.</span><span class="sxs-lookup"><span data-stu-id="cd030-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="cd030-115">Вызовы Direct3D не завершатся ошибкой ресурсов, например нехваткой видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="cd030-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="cd030-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="cd030-117">Как и D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D будет управлять ресурсами, а не драйвером.</span><span class="sxs-lookup"><span data-stu-id="cd030-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="cd030-118">В отличие от D3DCREATE_DISABLE_DRIVER_MANAGEMENT D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX будет возвращать ошибки для таких условий, как нехватка видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="cd030-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="cd030-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="cd030-120">Приводит к тому, что среда выполнения не регистрирует горячие клавиши для принтскрин, Ctrl-Printscreen и Alt-Printscreen для захвата содержимого рабочего стола или окна.</span><span class="sxs-lookup"><span data-stu-id="cd030-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd030-121">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cd030-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cd030-122">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cd030-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="cd030-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="cd030-124">Ограничьте вычисления до основного потока приложения.</span><span class="sxs-lookup"><span data-stu-id="cd030-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="cd030-125">Если флаг не установлен, среда выполнения может выполнять обработку вершин программного обеспечения и другие вычисления в рабочем потоке для повышения производительности многопроцессорных систем.</span><span class="sxs-lookup"><span data-stu-id="cd030-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd030-126">Различия между Windows XP и Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="cd030-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="cd030-127">Этот флаг доступен в Windows Vista, Windows Server 2008 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd030-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="cd030-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="cd030-129">Включает сбор данных о текущей статистике на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cd030-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="cd030-130">Вызовы <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>жетпресентстатистикс</strong></a> будут возвращать допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="cd030-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd030-131">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cd030-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cd030-132">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cd030-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="cd030-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="cd030-134">Задайте точность вычислений Direct3D с плавающей запятой до точности, используемой вызывающим потоком.</span><span class="sxs-lookup"><span data-stu-id="cd030-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="cd030-135">Если этот флаг не указан, Direct3D по умолчанию принимает значение Single-to-ближайшего режима, по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="cd030-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="cd030-136">Режим двойной точности снизит производительность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cd030-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="cd030-137">Части Direct3D предполагают, что исключения модуля с плавающей запятой имеют маску. снятие маски этих исключений может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="cd030-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="cd030-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="cd030-139">Указывает аппаратную обработку вершин.</span><span class="sxs-lookup"><span data-stu-id="cd030-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="cd030-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="cd030-141">Задает смешанную обработку вершин (как программного, так и аппаратного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="cd030-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="cd030-142">Для Windows 10 версии 1607 и более поздней использовать этот параметр не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cd030-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="cd030-143">См. D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="cd030-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="cd030-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="cd030-145">Указывает процесс обработки вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="cd030-145">Specifies software vertex processing.</span></span> <span data-ttu-id="cd030-146">Для Windows 10 версии 1607 и более поздней использовать этот параметр не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cd030-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="cd030-147">Используйте D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="cd030-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cd030-148">Если аппаратная обработка вершин недоступна, использование обработки вершин программного обеспечения не рекомендуется в Windows 10, версия 1607 (и более поздние версии), так как эффективность обработки вершин программного обеспечения значительно уменьшилась при повышении безопасности реализации.</span><span class="sxs-lookup"><span data-stu-id="cd030-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="cd030-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="cd030-150">Указывает, что приложение запрашивает безпотоковую безопасность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cd030-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="cd030-151">Таким образом, поток Direct3D становится более часто становиться владельцем своей глобальной <a href="/windows/desktop/Sync/critical-section-objects">критической секции</a> , что может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="cd030-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="cd030-152">Если приложение обрабатывает сообщения окна в одном потоке, одновременно делая вызовы API Direct3D в другой, приложение должно использовать этот флаг при создании устройства.</span><span class="sxs-lookup"><span data-stu-id="cd030-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="cd030-153">Это окно также необходимо уничтожить перед выгрузкой d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="cd030-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="cd030-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="cd030-155">Указывает, что Direct3D не должен изменять фокус окна каким бы ни было образом.</span><span class="sxs-lookup"><span data-stu-id="cd030-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cd030-156">Если этот флаг установлен, приложение должно полностью поддерживать все события управления фокусом, такие как события ALT + TAB и щелчок мыши.</span><span class="sxs-lookup"><span data-stu-id="cd030-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd030-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="cd030-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="cd030-158">Указывает, что Direct3D не поддерживает вызовы Get \* для любых данных, которые могут храниться в блоках состояния.</span><span class="sxs-lookup"><span data-stu-id="cd030-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="cd030-159">Он также указывает Direct3D не предоставлять какие бы то ни было службы эмуляции для обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="cd030-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="cd030-160">Это означает, что если устройство не поддерживает обработку вершин, то приложение может использовать только после преобразования вершин.</span><span class="sxs-lookup"><span data-stu-id="cd030-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd030-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="cd030-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="cd030-162">Разрешает экранные заставки во время полноэкранного приложения.</span><span class="sxs-lookup"><span data-stu-id="cd030-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="cd030-163">Без этого флага Direct3D отключает заставки в течение всего времени, пока вызывающее приложение находится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="cd030-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="cd030-164">Если вызывающее приложение уже является экранной заставкой, этот флаг не действует.</span><span class="sxs-lookup"><span data-stu-id="cd030-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd030-165">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cd030-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cd030-166">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cd030-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cd030-167">D3DCREATE \_ оборудование \_ ВЕРТЕКСПРОЦЕССИНГ, D3DCREATE \_ Mixed \_ вертекспроцессинг и D3DCREATE \_ Software вертекспроцессинг являются взаимоисключающими \_ флагами.</span><span class="sxs-lookup"><span data-stu-id="cd030-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="cd030-168">При вызове [**креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)необходимо указать хотя бы один из этих флагов обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="cd030-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="cd030-169">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="cd030-169">Constant Information</span></span>



| <span data-ttu-id="cd030-170">Требование</span><span class="sxs-lookup"><span data-stu-id="cd030-170">Requirement</span></span>                         |  <span data-ttu-id="cd030-171">Значение</span><span class="sxs-lookup"><span data-stu-id="cd030-171">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="cd030-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cd030-172">Header</span></span>                   | <span data-ttu-id="cd030-173">D3D9. h</span><span class="sxs-lookup"><span data-stu-id="cd030-173">D3D9.h</span></span>     |
| <span data-ttu-id="cd030-174">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="cd030-174">Minimum operating system</span></span> | <span data-ttu-id="cd030-175">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cd030-175">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cd030-176">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cd030-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd030-177">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="cd030-177">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
