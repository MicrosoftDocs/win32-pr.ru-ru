---
description: Константы, используемые \_ параметрами D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701193"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="33522-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="33522-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="33522-104">Константы, [**используемые \_ параметрами D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="33522-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="33522-105">#define</span></span></td>
<td><span data-ttu-id="33522-106">Значение</span><span class="sxs-lookup"><span data-stu-id="33522-106">Value</span></span></td>
<td><span data-ttu-id="33522-107">Описание</span><span class="sxs-lookup"><span data-stu-id="33522-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="33522-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="33522-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="33522-109">0x00000004</span></span></td>
<td><span data-ttu-id="33522-110">Обрезает оконный <a href="/windows/desktop/api"><strong>Блит в</strong></a> клиентскую область окна в области экрана монитора видеоадаптера, создавшего устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="33522-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="33522-111">D3DPRESENTFLAG_DEVICECLIP не является допустимым для D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="33522-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33522-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="33522-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="33522-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="33522-113">0x00000002</span></span></td>
<td><span data-ttu-id="33522-114">Установите этот флаг при создании цепочки устройств или буферов, чтобы включить удаление z-буфера.</span><span class="sxs-lookup"><span data-stu-id="33522-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="33522-115">Если этот флаг установлен, содержимое буфера шаблона глубины будет недействительным после <a href="/windows/desktop/api"><strong>вызова либо</strong></a> <a href="/windows/desktop/api"><strong>сетдепсстенЦилсурфаце</strong></a> с другой поверхностью глубины.</span><span class="sxs-lookup"><span data-stu-id="33522-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="33522-116">Отмена данных z-буфера может повысить производительность и зависит от драйвера.</span><span class="sxs-lookup"><span data-stu-id="33522-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="33522-117">Среда выполнения отладки будет принудительно применять отмену, очистив z-буфер до какого-либо постоянного значения после <a href="/windows/desktop/api"><strong>вызова либо</strong></a> <a href="/windows/desktop/api"><strong>сетдепсстенЦилсурфаце</strong></a> с другой поверхностью глубины.</span><span class="sxs-lookup"><span data-stu-id="33522-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="33522-118">Удаление данных z-буфера недопустимо для всех блокируемых форматов, D3DFMT_D16_LOCKABLE и D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="33522-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="33522-119">Любое использование <a href="/windows/desktop/api"><strong>креатедевице</strong></a> с указанием блокируемого формата и отклонения z-буфера завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="33522-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="33522-120">Дополнительные сведения о форматах см. в разделе <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="33522-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="33522-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="33522-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="33522-122">0x00000001</span></span></td>
<td><span data-ttu-id="33522-123">Установите этот флаг, если приложению требуется возможность непосредственной блокировки заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="33522-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="33522-124">Обратите внимание, что задние буферы не являются блокируемыми, если только в приложении не указано D3DPRESENTFLAG_LOCKABLE_BACKBUFFER при вызове <a href="/windows/desktop/api"><strong>креатедевице</strong></a> или <a href="/windows/desktop/api"><strong>сбросе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="33522-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="33522-125">Блокируемые задние буферы приводят к снижению производительности в некоторых конфигурациях графического оборудования.</span><span class="sxs-lookup"><span data-stu-id="33522-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="33522-126">Выполнение операции блокировки (или использования <a href="/windows/desktop/api"><strong>упдатесурфаце</strong></a> для записи) в блокируемом обратном буфере снижает производительность на многих картах.</span><span class="sxs-lookup"><span data-stu-id="33522-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="33522-127">В этом случае рассмотрите возможность использования текстурированных треугольников для перемещения данных в задний буфер.</span><span class="sxs-lookup"><span data-stu-id="33522-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-128">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-129">В Direct3D9Ex этот флаг не может быть установлен, если D3DSWAPEFFECT имеет D3DSWAPEFFECT_FLIPEX, так как модель перелистывания позволяет диспетчер окон рабочего стола доступ к обратному буферу приложения.</span><span class="sxs-lookup"><span data-stu-id="33522-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="33522-130">Невозможно заблокировать общую поверхность между процессами.</span><span class="sxs-lookup"><span data-stu-id="33522-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33522-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="33522-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="33522-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="33522-132">0x00000020</span></span></td>
<td><span data-ttu-id="33522-133">Повернутые мониторы обрабатываются автоматически при помощи вращающейся копии во время презентации, что не очень эффективно.</span><span class="sxs-lookup"><span data-stu-id="33522-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="33522-134">Этот флаг означает, что приложение будет выполнять собственный поворот экрана.</span><span class="sxs-lookup"><span data-stu-id="33522-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-135">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-136">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="33522-137">Приложения могут достичь собственного вращения, возможно, с помощью матрицы повернутого представления.</span><span class="sxs-lookup"><span data-stu-id="33522-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="33522-138">Для поиска текущего параметра вращения должны использоваться методы <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>жетдисплаймодикс</strong></a> и <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>жетадаптердисплаймодикс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="33522-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="33522-139">Параметры ширины и высоты буфера в <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>креатедевицеекс</strong></a> и <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ресетекс</strong></a> должны иметь альбомную ориентацию, тогда как структура полноэкранного режима должна быть такой же, как и та, что возвращается из <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>енумадаптермодесекс</strong></a> (т. е. ширина и высота меняются при повороте 90 и 270 градусов).</span><span class="sxs-lookup"><span data-stu-id="33522-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="33522-140">При использовании блокировки повернутых целевых объектов отрисовки, в левом верхнем углу предполагается, что они не будут иметь значение true, целевой объект прорисовки SURFACE_DESC останется альбомным (как подразумевается в параметрах создания), а окно GDI, координаты мыши и, таким образом, должны быть правильно переведены при использовании с целевым объектом отрисовки Direct3D и сценой.</span><span class="sxs-lookup"><span data-stu-id="33522-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="33522-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="33522-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="33522-142">0x00000040</span></span></td>
<td><span data-ttu-id="33522-143">Используйте этот флаг, чтобы указать любой режим вывода RAW, перечисленный видеоадаптером, даже если в Direct3D был указан недопустимый режим.</span><span class="sxs-lookup"><span data-stu-id="33522-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="33522-144">Приложение должно реализовать это надежным образом в случае, если требуемый режим действительно является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="33522-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-145">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-146">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33522-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="33522-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="33522-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33522-148">0x00000010</span></span></td>
<td><span data-ttu-id="33522-149">Это указание драйверу, что задние буферы будут содержать данные видео.</span><span class="sxs-lookup"><span data-stu-id="33522-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="33522-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="33522-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="33522-151">0x00000080</span></span></td>
<td><span data-ttu-id="33522-152">Указывает, является ли наложение полным диапазоном RGB или ограниченным диапазоном RGB.</span><span class="sxs-lookup"><span data-stu-id="33522-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="33522-153">Установка этого флага означает ограниченный диапазон RGB.</span><span class="sxs-lookup"><span data-stu-id="33522-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="33522-154">В ограниченном диапазоне RGB диапазон RGB сжимается таким, что 16:16:16 является черным, а 235:235:235 — белым.</span><span class="sxs-lookup"><span data-stu-id="33522-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-155">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-156">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33522-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="33522-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="33522-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="33522-158">0x00000100</span></span></td>
<td><span data-ttu-id="33522-159">Указывает, является ли наложение BT. 601 или BT. 709.</span><span class="sxs-lookup"><span data-stu-id="33522-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="33522-160">Установка этого флага означает BT. 709 для телевидения высокой четкости (ТВВЧ).</span><span class="sxs-lookup"><span data-stu-id="33522-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-161">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-162">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="33522-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="33522-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="33522-164">0x00000200</span></span></td>
<td><span data-ttu-id="33522-165">Указывает, является ли наложение традиционным Икбкр или расширенным Икбкр (Ксвикк).</span><span class="sxs-lookup"><span data-stu-id="33522-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="33522-166">Установка этого флага означает расширенный Икбкр (Ксвикк).</span><span class="sxs-lookup"><span data-stu-id="33522-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-167">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-168">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33522-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="33522-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="33522-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="33522-170">0x00000400</span></span></td>
<td><span data-ttu-id="33522-171">Установка этого флага означает, что имеющуюся цепочку буферов содержит защищенное содержимое и автоматически заставляет среду выполнения ограничить доступ к имеющуюся цепочку буферов, чтобы только диспетчер настольных систем Windows (DWM) мог использовать имеющуюся цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="33522-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-172">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-173">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33522-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="33522-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="33522-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="33522-175">0x00000800</span></span></td>
<td><span data-ttu-id="33522-176">Установка этого флага означает, что драйвер должен ограничивать доступ ко всем общим ресурсам, созданным для взаимодействия с DWM.</span><span class="sxs-lookup"><span data-stu-id="33522-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="33522-177">Вызывающий объект должен создать канал с проверкой подлинности с помощью драйвера.</span><span class="sxs-lookup"><span data-stu-id="33522-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="33522-178">После этого драйвер должен разрешить доступ к процессам, пытающимся открыть эти общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="33522-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33522-179">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="33522-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="33522-180">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="33522-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="33522-181">Эти константы используются [**\_ параметрами D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="33522-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="33522-182">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="33522-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="33522-183">Header</span><span class="sxs-lookup"><span data-stu-id="33522-183">Header</span></span>                   | <span data-ttu-id="33522-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="33522-184">d3d9types.h</span></span> |
| <span data-ttu-id="33522-185">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="33522-185">Minimum operating system</span></span> | <span data-ttu-id="33522-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="33522-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="33522-187">См. также</span><span class="sxs-lookup"><span data-stu-id="33522-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33522-188">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="33522-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




