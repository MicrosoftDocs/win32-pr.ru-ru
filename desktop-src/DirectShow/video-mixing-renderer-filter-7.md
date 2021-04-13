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
# <a name="video-mixing-renderer-filter-7"></a>Фильтр визуализации 7 для микширования видео

Этот раздел относится к Windows XP или более поздним версиям.

В Windows XP и более поздних версиях модуль подготовки видео (VMR-7) является модулем обработки видео по умолчанию. Он называется VMR-7, так как на внутреннем уровне используется DirectDraw 7. В DirectX 9 аналогичный, но отдельный фильтр VMR-9 доступен для распространения в системах, не использующих XP. VMR-9 использует Direct3D 9.

> [!Note]  
> Фильтр VMR доступен в Windows XP и более поздних версиях. Он недоступен через распространяемый пакет DirectX или в предыдущих версиях Windows. В большинстве случаев приложения должны использовать [устройство микширования видео 9](video-mixing-renderer-filter-9.md).

 

К свойствам VMR относятся:

-   True альфа-смешение до 16 входных потоков
-   Доступ к составному изображению до его подготовки к просмотру
-   Модель подключаемых модулей, которая позволяет сторонним разработчикам реализовать пользовательские видеоэффекты.
-   Поддержка до 15 мониторов.

Во время построения графа на Windows XP и более поздних версиях диспетчер графов фильтров не будет использовать старые фильтры для подготовки видео или микшера наложения, если только они не будут явно созданы и добавлены в граф.

Дополнительные сведения см. [в разделе Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td>Все режимы:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li>
<li><a href="ikspropertyset.md"><strong>икспропертисет</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>ивмраспектратиоконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>ивмрдеинтерлацеконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>ивмрфилтерконфиг</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>ивмрмиксербитмап</strong></a></li>
</ul>
Режим с окнами:<br/>
<ul>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>ибасиквидео</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>ивидеовиндов</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>ивмрмониторконфиг</strong></a></li>
</ul>
Режим без окон:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>ивмрвиндовлессконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>ивмрмониторконфиг</strong></a></li>
</ul>
Режим безрендеринга:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>ивмрсурфацеаллокаторнотифи</strong></a></li>
</ul>
Режим микшера:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>ивмрмиксерконтрол</strong></a></li>
</ul>
Сведения о различных режимах VMR-7 см. в разделе <a href="vmr-modes-of-operation.md">режимы VMR в операции</a>.<br/></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Основной тип: MEDIATYPE_VideoSubtype: зависит от графического оборудования. Должно быть несжатым видео.<br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>иамвидеоакцелератор</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>Иоверлай</strong></a> (см. примечания)</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>ивмрвидеостреамконтрол</strong></a></li>
</ul></td>
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
<td>С этим фильтром связано два идентификатора CLSID:
<ul>
<li>CLSID_VideoMixingRenderer: создает VMR-7. Если для создания VMR-7 недостаточно системных ресурсов, вызов <strong>CoCreateInstance</strong> завершается ошибкой.</li>
<li>CLSID_VideoRendererDefault: создает VMR-7, если доступны системные ресурсы, или, в противном случае, создает старый фильтр модуля <a href="video-renderer-filter.md">подготовки</a> отчетов.</li>
</ul>
Используйте CLSID_VideoMixingRenderer, если требуются специальные возможности VMR-7. В противном случае используйте CLSID_VideoRendererDefault, который почти не может завершиться сбоем, так как он возвращается к старому фильтру модуля подготовки отчетов.<br/></td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Не применяется</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Закрепление ввода предоставляет интерфейс **иоверлай** только в том случае, если фильтр VMR-7 находится в оконном режиме. Единственным методом **иоверлай** , который реализует ПИН-код, является **жетвиндовхандле**, который позволяет приложению получить маркер окна видео фильтра. Все остальные методы **иоверлай** возвращают E \_ нотимпл. В режиме без окон фильтр не создает окно видео, поэтому ПИН-код не предоставляет интерфейс.

Приложение может предоставить пользовательский объект распределителя-Presenter, который предоставляет следующие интерфейсы:

-   [**ивмримажепресентер**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**Ивмримажепресентерконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (необязательно)
-   [**Ивмрмониторконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (необязательно)
-   [**ивмрсурфацеаллокатор**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**Ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (необязательно)

Дополнительные сведения о пользовательских распределительных выступающих см. [в разделе предоставление настраиваемого Allocator-Presenter для VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Приложение также может предоставить пользовательский компоновщик подключаемых модулей, который предоставляет следующий интерфейс:

-   [**ивмримажекомпоситор**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Чтобы настроить VMR с помощью пользовательского компоновщика, вызовите [**ивмрфилтерконфиг:: сетимажекомпоситор**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




