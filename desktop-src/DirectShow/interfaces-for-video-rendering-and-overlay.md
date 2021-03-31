---
description: Интерфейсы для отрисовки и наложения видео
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Интерфейсы для отрисовки и наложения видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806478"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="c81d3-103">Интерфейсы для отрисовки и наложения видео</span><span class="sxs-lookup"><span data-stu-id="c81d3-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="c81d3-104">Эти интерфейсы поддерживают управление приложениями при отрисовке видео.</span><span class="sxs-lookup"><span data-stu-id="c81d3-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="c81d3-105">Обратите внимание, что некоторые из этих интерфейсов теперь являются устаревшими, так как фильтр модуля подготовки видео для микширования обеспечивает превосходную визуализацию и управление наложением.</span><span class="sxs-lookup"><span data-stu-id="c81d3-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c81d3-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c81d3-106">Interface</span></span></th>
<th><span data-ttu-id="c81d3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c81d3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c81d3-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-109">Предоставляет доступ к сведениям и параметрам, закрытым субтитрами.</span><span class="sxs-lookup"><span data-stu-id="c81d3-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>иамоверлайфкс</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-111">Примените эффекты наложенного захвата к видеоповерхности.</span><span class="sxs-lookup"><span data-stu-id="c81d3-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="c81d3-112">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>иамвидеодеЦиматионпропертиес</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-114">Управление тем, как DirectShow масштабирует изображение видео, если видеоокно меньше собственного размера видео.</span><span class="sxs-lookup"><span data-stu-id="c81d3-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="c81d3-115">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-117">Задайте свойства видео.</span><span class="sxs-lookup"><span data-stu-id="c81d3-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-119">Просмотр видео в режиме эксклюзивного полноэкранного режима в Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c81d3-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="c81d3-120">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>иддравексклмодевидеокаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-122">Интерфейс обратного вызова для получения уведомлений об изменениях в положении, размере и видимости оверлея.</span><span class="sxs-lookup"><span data-stu-id="c81d3-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="c81d3-123">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>идиректдраввидео</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-125">Отключить указанные возможности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c81d3-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="c81d3-126">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>идиректдравмедиасампле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-128">Доступ к поверхности DirectDraw, выделенной фильтром <a href="overlay-mixer-filter.md">микшера оверлея</a> . (Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>имиксероккс</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-130">Реализовано в микшере наложения.</span><span class="sxs-lookup"><span data-stu-id="c81d3-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="c81d3-131">Позволяет бесоконным клиентам, таким как элементы управления ActiveX®, получать и задавать свойства прямоугольника видео и рекомендовать фильтр событий.</span><span class="sxs-lookup"><span data-stu-id="c81d3-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>имиксероккснотифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-133">Реализуется бесоконными клиентами и вызывается микшером наложения для отправки уведомлений о событиях, влияющих на экранный видеомонитор.</span><span class="sxs-lookup"><span data-stu-id="c81d3-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-135">Установите элементы управления цветами видео в фильтре микшера наложения при совместном использовании нескольких видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="c81d3-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="c81d3-136">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="c81d3-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c81d3-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-138">Запросите модуль подготовки видео о производительности.</span><span class="sxs-lookup"><span data-stu-id="c81d3-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c81d3-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="c81d3-140">Задание свойств окна видео.</span><span class="sxs-lookup"><span data-stu-id="c81d3-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="c81d3-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="c81d3-155">Интерфейсы устройства визуализации 9 с микшированием видео.</span><span class="sxs-lookup"><span data-stu-id="c81d3-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c81d3-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>ивмраспектратиоконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>ивмрдеинтерлацеконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>ивмрфилтерконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>ивмримажекомпоситор</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>ивмримажепресентер</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>ивмримажепресентерконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>ивмрмиксербитмап</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>ивмрмиксерконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>ивмрсурфацеаллокатор</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>ивмрсурфацеаллокаторнотифи</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="c81d3-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>ивмрвиндовлессконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="c81d3-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="c81d3-167">Интерфейсы модуля подготовки видео для микширования 7.</span><span class="sxs-lookup"><span data-stu-id="c81d3-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c81d3-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c81d3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c81d3-169">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="c81d3-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



