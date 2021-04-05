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
# <a name="video-mixing-renderer-filter-9"></a>Фильтр визуализации 9 для микшера видео

В DirectX 9 фильтр рендеринга видео 9 (VMR-9) предлагает расширенные возможности отрисовки видео на всех платформах, поддерживаемых DirectX. Он полностью интегрирован с возможностями 3D-функций DirectX 9. Например, вы можете легко добавлять видео в игры и другие трехмерные среды или преобразовывать видеоизображения с помощью шейдеров Direct3D Pixel и других эффектов.

Этот фильтр не поддерживает порты видео.

Для обеспечения обратной совместимости VMR-9 не является модулем подготовки отчетов по умолчанию в любой системе. Чтобы использовать этот фильтр, необходимо явно добавить его в граф фильтра и настроить перед подключением любого из входных ПИН-кодов. VMR-9 использует собственный набор интерфейсов, структур и перечислений, которые не всегда идентичны соответствующим типам данных, используемым с VMR-7.

VMR-9 поддерживает до 16 мониторов.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td>VMR-9 поддерживает несколько различных режимов рендеринга. Он поддерживает другой набор интерфейсов в зависимости от режима рендеринга.<br/>
<ul>
<li>Все режимы: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li>Режим безрендеринга: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li>Оконный режим: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ибасиквидео</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li>Режим без окон: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul>
Чтобы задать режим рендеринга, вызовите метод <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: сетрендерингмоде</strong></a>. Дополнительные сведения см. в статье <a href="vmr-modes-of-operation.md">режимы VMR в операции</a>.<br/></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Входные контакты будут подключаться с любым типом, поддерживаемым базовым видеооборудованием.</td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Иамвидеоакцелератор</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>иоверлай</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_VideoMixingRenderer9</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Н/Д</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




