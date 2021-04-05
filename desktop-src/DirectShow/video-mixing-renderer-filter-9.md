---
description: Фильтр визуализации 9 для микшера видео
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Фильтр визуализации 9 для микшера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815256"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="7d513-103">Фильтр визуализации 9 для микшера видео</span><span class="sxs-lookup"><span data-stu-id="7d513-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="7d513-104">В DirectX 9 фильтр рендеринга видео 9 (VMR-9) предлагает расширенные возможности отрисовки видео на всех платформах, поддерживаемых DirectX.</span><span class="sxs-lookup"><span data-stu-id="7d513-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="7d513-105">Он полностью интегрирован с возможностями 3D-функций DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="7d513-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="7d513-106">Например, вы можете легко добавлять видео в игры и другие трехмерные среды или преобразовывать видеоизображения с помощью шейдеров Direct3D Pixel и других эффектов.</span><span class="sxs-lookup"><span data-stu-id="7d513-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="7d513-107">Этот фильтр не поддерживает порты видео.</span><span class="sxs-lookup"><span data-stu-id="7d513-107">This filter does not support video ports.</span></span>

<span data-ttu-id="7d513-108">Для обеспечения обратной совместимости VMR-9 не является модулем подготовки отчетов по умолчанию в любой системе.</span><span class="sxs-lookup"><span data-stu-id="7d513-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="7d513-109">Чтобы использовать этот фильтр, необходимо явно добавить его в граф фильтра и настроить перед подключением любого из входных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="7d513-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="7d513-110">VMR-9 использует собственный набор интерфейсов, структур и перечислений, которые не всегда идентичны соответствующим типам данных, используемым с VMR-7.</span><span class="sxs-lookup"><span data-stu-id="7d513-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="7d513-111">VMR-9 поддерживает до 16 мониторов.</span><span class="sxs-lookup"><span data-stu-id="7d513-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d513-112">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="7d513-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7d513-113">VMR-9 поддерживает несколько различных режимов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="7d513-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="7d513-114">Он поддерживает другой набор интерфейсов в зависимости от режима рендеринга.</span><span class="sxs-lookup"><span data-stu-id="7d513-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="7d513-115">Все режимы: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d513-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="7d513-116">Режим безрендеринга: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d513-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="7d513-117">Оконный режим: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ибасиквидео</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d513-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="7d513-118">Режим без окон: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d513-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="7d513-119">Чтобы задать режим рендеринга, вызовите метод <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: сетрендерингмоде</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7d513-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="7d513-120">Дополнительные сведения см. в статье <a href="vmr-modes-of-operation.md">режимы VMR в операции</a>.</span><span class="sxs-lookup"><span data-stu-id="7d513-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d513-121">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7d513-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7d513-122">Входные контакты будут подключаться с любым типом, поддерживаемым базовым видеооборудованием.</span><span class="sxs-lookup"><span data-stu-id="7d513-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d513-123">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7d513-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7d513-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Иамвидеоакцелератор</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>иоверлай</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d513-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d513-125">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7d513-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7d513-126">Не применяется</span><span class="sxs-lookup"><span data-stu-id="7d513-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d513-127">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7d513-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7d513-128">Не применяется</span><span class="sxs-lookup"><span data-stu-id="7d513-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d513-129">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="7d513-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="7d513-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="7d513-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d513-131">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7d513-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7d513-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7d513-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d513-133">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="7d513-133">Executable</span></span></td>
<td><span data-ttu-id="7d513-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7d513-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d513-135"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="7d513-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7d513-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="7d513-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d513-137"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="7d513-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7d513-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7d513-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7d513-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d513-139">Remarks</span></span>

<span data-ttu-id="7d513-140">Приложение может предоставить пользовательский объект распределителя-Presenter, который предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="7d513-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="7d513-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="7d513-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="7d513-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7d513-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="7d513-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="7d513-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="7d513-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7d513-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="7d513-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="7d513-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="7d513-146">Дополнительные сведения о пользовательских распределительных выступающих см. [в разделе Предоставление настраиваемой Allocator-Presenter для VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="7d513-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="7d513-147">Приложение также может предоставить пользовательский компоновщик подключаемых модулей, который предоставляет следующий интерфейс:</span><span class="sxs-lookup"><span data-stu-id="7d513-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="7d513-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="7d513-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="7d513-149">Чтобы настроить VMR с помощью пользовательского компоновщика, вызовите [**IVMRFilterConfig9:: сетимажекомпоситор**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="7d513-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d513-150">См. также</span><span class="sxs-lookup"><span data-stu-id="7d513-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d513-151">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7d513-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7d513-152">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="7d513-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




