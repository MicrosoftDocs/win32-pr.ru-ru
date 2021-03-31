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
# <a name="interfaces-for-video-rendering-and-overlay"></a>Интерфейсы для отрисовки и наложения видео

Эти интерфейсы поддерживают управление приложениями при отрисовке видео. Обратите внимание, что некоторые из этих интерфейсов теперь являются устаревшими, так как фильтр модуля подготовки видео для микширования обеспечивает превосходную визуализацию и управление наложением.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Интерфейс</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Предоставляет доступ к сведениям и параметрам, закрытым субтитрами.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>иамоверлайфкс</strong></a></td>
<td>Примените эффекты наложенного захвата к видеоповерхности. (Не рекомендуется.)</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>иамвидеодеЦиматионпропертиес</strong></a></td>
<td>Управление тем, как DirectShow масштабирует изображение видео, если видеоокно меньше собственного размера видео. (Не рекомендуется.)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Задайте свойства видео.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a></td>
<td>Просмотр видео в режиме эксклюзивного полноэкранного режима в Microsoft DirectDraw. (Не рекомендуется.)</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>иддравексклмодевидеокаллбакк</strong></a></td>
<td>Интерфейс обратного вызова для получения уведомлений об изменениях в положении, размере и видимости оверлея. (Не рекомендуется.)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>идиректдраввидео</strong></a></td>
<td>Отключить указанные возможности DirectDraw. (Не рекомендуется.)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>идиректдравмедиасампле</strong></a></td>
<td>Доступ к поверхности DirectDraw, выделенной фильтром <a href="overlay-mixer-filter.md">микшера оверлея</a> . (Не рекомендуется.)</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>имиксероккс</strong></a></td>
<td>Реализовано в микшере наложения. Позволяет бесоконным клиентам, таким как элементы управления ActiveX®, получать и задавать свойства прямоугольника видео и рекомендовать фильтр событий.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>имиксероккснотифи</strong></a></td>
<td>Реализуется бесоконными клиентами и вызывается микшером наложения для отправки уведомлений о событиях, влияющих на экранный видеомонитор.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Установите элементы управления цветами видео в фильтре микшера наложения при совместном использовании нескольких видеопотоков. (Не рекомендуется.)</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></td>
<td>Запросите модуль подготовки видео о производительности.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a></td>
<td>Задание свойств окна видео.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul></td>
<td>Интерфейсы устройства визуализации 9 с микшированием видео.</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>ивмраспектратиоконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>ивмрдеинтерлацеконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>ивмрфилтерконфиг</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>ивмримажекомпоситор</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>ивмримажепресентер</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>ивмримажепресентерконфиг</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>ивмрмиксербитмап</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>ивмрмиксерконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>ивмрсурфацеаллокатор</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>ивмрсурфацеаллокаторнотифи</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>ивмрвиндовлессконтрол</strong></a></li>
</ul></td>
<td>Интерфейсы модуля подготовки видео для микширования 7.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



