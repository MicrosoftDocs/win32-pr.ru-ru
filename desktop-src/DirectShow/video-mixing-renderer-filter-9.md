---
description: Фильтр визуализации 9 для микшера видео
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Фильтр визуализации 9 для микшера видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2077679599db45ab80e7be931a83f500c156405c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466591"
---
# <a name="video-mixing-renderer-filter-9"></a>Фильтр визуализации 9 для микшера видео

В DirectX 9 фильтр рендеринга видео 9 (VMR-9) предлагает расширенные возможности отрисовки видео на всех платформах, поддерживаемых DirectX. Он полностью интегрирован с возможностями 3D-функций DirectX 9. Например, вы можете легко добавлять видео в игры и другие трехмерные среды или преобразовывать видеоизображения с помощью шейдеров Direct3D Pixel и других эффектов.

Этот фильтр не поддерживает порты видео.

Для обеспечения обратной совместимости VMR-9 не является модулем подготовки отчетов по умолчанию в любой системе. Чтобы использовать этот фильтр, необходимо явно добавить его в граф фильтра и настроить перед подключением любого из входных ПИН-кодов. VMR-9 использует собственный набор интерфейсов, структур и перечислений, которые не всегда идентичны соответствующим типам данных, используемым с VMR-7.

VMR-9 поддерживает до 16 мониторов.




| | | Интерфейсы фильтра | VMR-9 поддерживает несколько различных режимов рендеринга. Он поддерживает другой набор интерфейсов в зависимости от режима рендеринга.<br /><ul><li>Все режимы: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Режим безрендеринга: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Оконный режим: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ибасиквидео</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Режим без окон: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Чтобы задать режим рендеринга, вызовите метод <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: сетрендерингмоде</strong></a>. Дополнительные сведения см. в статье <a href="vmr-modes-of-operation.md">режимы VMR в операции</a>.<br /> | | Типы входных закрепления Входные контакты будут подключаться с любым типом, поддерживаемым базовым видеооборудованием. | | Интерфейсы входных закрепления | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Иамвидеоакцелератор</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>иоверлай</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | | Типы выходных закрепления Неприменимо. | | Интерфейсы выходного ПИН-кода | Неприменимо. | | Фильтровать CLSID | CLSID_VideoMixingRenderer9 | | CLSID страницы свойств | Н/Д | | Исполняемый файл | Quartz.dll | | <a href="merit.md"></a> Кому | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

Приложение может предоставить пользовательский объект распределителя-Presenter, который предоставляет следующие интерфейсы:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (необязательно)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (необязательно)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (необязательно)

Дополнительные сведения о пользовательских распределительных выступающих см. [в разделе Предоставление настраиваемой Allocator-Presenter для VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Приложение также может предоставить пользовательский компоновщик подключаемых модулей, который предоставляет следующий интерфейс:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Чтобы настроить VMR с помощью пользовательского компоновщика, вызовите [**IVMRFilterConfig9:: сетимажекомпоситор**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




