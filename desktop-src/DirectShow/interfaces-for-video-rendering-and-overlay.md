---
description: Интерфейсы для отрисовки и наложения видео
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Интерфейсы для отрисовки и наложения видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40a8fcfa2d5e848c0e33fda14828c868cead28b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482580"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a>Интерфейсы для отрисовки и наложения видео

Эти интерфейсы поддерживают управление приложениями при отрисовке видео. Обратите внимание, что некоторые из этих интерфейсов теперь являются устаревшими, так как фильтр модуля подготовки видео для микширования обеспечивает превосходную визуализацию и управление наложением.




| Интерфейс | Описание | 
|-----------|-------------|
| <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a> | Предоставляет доступ к сведениям и параметрам, закрытым субтитрами. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>иамоверлайфкс</strong></a> | Примените эффекты наложенного захвата к видеоповерхности. (Не рекомендуется.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>иамвидеодеЦиматионпропертиес</strong></a> | управление тем, как DirectShow масштабирует изображение видео, если видеоокно меньше собственного размера видео. (Не рекомендуется.) | 
| <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a> | Задайте свойства видео. | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a> | Просмотр видео в режиме эксклюзивного полноэкранного режима в Microsoft DirectDraw. (Не рекомендуется.) | 
| <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>иддравексклмодевидеокаллбакк</strong></a> | Интерфейс обратного вызова для получения уведомлений об изменениях в положении, размере и видимости оверлея. (Не рекомендуется.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>идиректдраввидео</strong></a> | Отключить указанные возможности DirectDraw. (Не рекомендуется.) | 
| <a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>идиректдравмедиасампле</strong></a> | доступ к поверхности DirectDraw, выделенной с помощью <a href="overlay-mixer-filter.md">оверлея Mixer</a> фильтр. (Не рекомендуется.) | 
| <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>имиксероккс</strong></a> | Реализуется на наложении Mixer. включает бесоконные клиенты, такие как ActiveX® элементы управления для получения и задания свойств прямоугольника видео и порекомендовать фильтр событий. | 
| <a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>имиксероккснотифи</strong></a> | реализуется бесоконными клиентами и вызывается наложением Mixer для отправки уведомлений о событиях, влияющих на экранный видеомонитор. | 
| <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a> | установите элементы управления цветами видео на наложении Mixer фильтр при совместном использовании нескольких видеопотоков. (Не рекомендуется.) | 
| <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a> | Запросите модуль подготовки видео о производительности. | 
| <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a> | Задание свойств окна видео. | 
| <ul><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul> | Интерфейсы устройства визуализации 9 с микшированием видео. | 
| <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>ивмраспектратиоконтрол</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>ивмрдеинтерлацеконтрол</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>ивмрфилтерконфиг</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>ивмримажекомпоситор</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>ивмримажепресентер</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>ивмримажепресентерконфиг</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>ивмрмиксербитмап</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>ивмрмиксерконтрол</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>ивмрсурфацеаллокатор</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>ивмрсурфацеаллокаторнотифи</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>ивмрвиндовлессконтрол</strong></a></li></ul> | Интерфейсы модуля подготовки видео для микширования 7. | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



