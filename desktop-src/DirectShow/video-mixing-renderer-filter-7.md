---
description: Фильтр визуализации 7 для микширования видео
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Фильтр визуализации 7 для микширования видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543775"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="56048-103">Фильтр визуализации 7 для микширования видео</span><span class="sxs-lookup"><span data-stu-id="56048-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="56048-104">Этот раздел относится к Windows XP или более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="56048-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="56048-105">В Windows XP и более поздних версиях модуль подготовки видео (VMR-7) является модулем обработки видео по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56048-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="56048-106">Он называется VMR-7, так как на внутреннем уровне используется DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="56048-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="56048-107">В DirectX 9 аналогичный, но отдельный фильтр VMR-9 доступен для распространения в системах, не использующих XP.</span><span class="sxs-lookup"><span data-stu-id="56048-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="56048-108">VMR-9 использует Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="56048-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="56048-109">Фильтр VMR доступен в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="56048-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="56048-110">Он недоступен через распространяемый пакет DirectX или в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="56048-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="56048-111">В большинстве случаев приложения должны использовать [устройство микширования видео 9](video-mixing-renderer-filter-9.md).</span><span class="sxs-lookup"><span data-stu-id="56048-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="56048-112">К свойствам VMR относятся:</span><span class="sxs-lookup"><span data-stu-id="56048-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="56048-113">True альфа-смешение до 16 входных потоков</span><span class="sxs-lookup"><span data-stu-id="56048-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="56048-114">Доступ к составному изображению до его подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="56048-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="56048-115">Модель подключаемых модулей, которая позволяет сторонним разработчикам реализовать пользовательские видеоэффекты.</span><span class="sxs-lookup"><span data-stu-id="56048-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="56048-116">Поддержка до 15 мониторов.</span><span class="sxs-lookup"><span data-stu-id="56048-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="56048-117">Во время построения графа на Windows XP и более поздних версиях диспетчер графов фильтров не будет использовать старые фильтры для подготовки видео или микшера наложения, если только они не будут явно созданы и добавлены в граф.</span><span class="sxs-lookup"><span data-stu-id="56048-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="56048-118">Дополнительные сведения см. [в разделе Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="56048-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56048-119">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="56048-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="56048-120">Все режимы:</span><span class="sxs-lookup"><span data-stu-id="56048-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="56048-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="56048-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="56048-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="56048-124"><a href="ikspropertyset.md"><strong>икспропертисет</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="56048-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="56048-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="56048-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="56048-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="56048-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>ивмраспектратиоконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="56048-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>ивмрдеинтерлацеконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="56048-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>ивмрфилтерконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="56048-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>ивмрмиксербитмап</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="56048-133">Режим с окнами:</span><span class="sxs-lookup"><span data-stu-id="56048-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="56048-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ибасиквидео</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="56048-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="56048-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="56048-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>ивмрмониторконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="56048-138">Режим без окон:</span><span class="sxs-lookup"><span data-stu-id="56048-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="56048-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>ивмрвиндовлессконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="56048-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>ивмрмониторконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="56048-141">Режим безрендеринга:</span><span class="sxs-lookup"><span data-stu-id="56048-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="56048-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>ивмрсурфацеаллокаторнотифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="56048-143">Режим микшера:</span><span class="sxs-lookup"><span data-stu-id="56048-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="56048-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>ивмрмиксерконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="56048-145">Сведения о различных режимах VMR-7 см. в разделе <a href="vmr-modes-of-operation.md">режимы VMR в операции</a>.</span><span class="sxs-lookup"><span data-stu-id="56048-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56048-146">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="56048-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="56048-147">Основной тип: MEDIATYPE_VideoSubtype: зависит от графического оборудования.</span><span class="sxs-lookup"><span data-stu-id="56048-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="56048-148">Должно быть несжатым видео.</span><span class="sxs-lookup"><span data-stu-id="56048-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56048-149">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="56048-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="56048-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>иамвидеоакцелератор</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="56048-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="56048-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>Иоверлай</strong></a> (см. примечания)</span><span class="sxs-lookup"><span data-stu-id="56048-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="56048-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="56048-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="56048-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="56048-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>ивмрвидеостреамконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="56048-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56048-157">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="56048-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="56048-158">Не применяется</span><span class="sxs-lookup"><span data-stu-id="56048-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56048-159">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="56048-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="56048-160">Не применяется</span><span class="sxs-lookup"><span data-stu-id="56048-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56048-161">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="56048-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="56048-162">С этим фильтром связано два идентификатора CLSID:</span><span class="sxs-lookup"><span data-stu-id="56048-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="56048-163">CLSID_VideoMixingRenderer: создает VMR-7.</span><span class="sxs-lookup"><span data-stu-id="56048-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="56048-164">Если для создания VMR-7 недостаточно системных ресурсов, вызов <strong>CoCreateInstance</strong> завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="56048-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="56048-165">CLSID_VideoRendererDefault: создает VMR-7, если доступны системные ресурсы, или, в противном случае, создает старый фильтр модуля <a href="video-renderer-filter.md">подготовки</a> отчетов.</span><span class="sxs-lookup"><span data-stu-id="56048-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="56048-166">Используйте CLSID_VideoMixingRenderer, если требуются специальные возможности VMR-7.</span><span class="sxs-lookup"><span data-stu-id="56048-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="56048-167">В противном случае используйте CLSID_VideoRendererDefault, который почти не может завершиться сбоем, так как он возвращается к старому фильтру модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="56048-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56048-168">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="56048-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="56048-169">Не применяется</span><span class="sxs-lookup"><span data-stu-id="56048-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56048-170">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="56048-170">Executable</span></span></td>
<td><span data-ttu-id="56048-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="56048-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56048-172"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="56048-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="56048-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="56048-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56048-174"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="56048-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="56048-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="56048-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="56048-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56048-176">Remarks</span></span>

<span data-ttu-id="56048-177">Закрепление ввода предоставляет интерфейс **иоверлай** только в том случае, если фильтр VMR-7 находится в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="56048-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="56048-178">Единственным методом **иоверлай** , который реализует ПИН-код, является **жетвиндовхандле**, который позволяет приложению получить маркер окна видео фильтра.</span><span class="sxs-lookup"><span data-stu-id="56048-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="56048-179">Все остальные методы **иоверлай** возвращают E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="56048-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="56048-180">В режиме без окон фильтр не создает окно видео, поэтому ПИН-код не предоставляет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="56048-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="56048-181">Приложение может предоставить пользовательский объект распределителя-Presenter, который предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="56048-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="56048-182">**ивмримажепресентер**</span><span class="sxs-lookup"><span data-stu-id="56048-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="56048-183">[**Ивмримажепресентерконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="56048-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="56048-184">[**Ивмрмониторконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="56048-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="56048-185">**ивмрсурфацеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="56048-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="56048-186">[**Ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="56048-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="56048-187">Дополнительные сведения о пользовательских распределительных выступающих см. [в разделе предоставление настраиваемого Allocator-Presenter для VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="56048-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="56048-188">Приложение также может предоставить пользовательский компоновщик подключаемых модулей, который предоставляет следующий интерфейс:</span><span class="sxs-lookup"><span data-stu-id="56048-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="56048-189">**ивмримажекомпоситор**</span><span class="sxs-lookup"><span data-stu-id="56048-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="56048-190">Чтобы настроить VMR с помощью пользовательского компоновщика, вызовите [**ивмрфилтерконфиг:: сетимажекомпоситор**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="56048-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56048-191">См. также</span><span class="sxs-lookup"><span data-stu-id="56048-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56048-192">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="56048-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




