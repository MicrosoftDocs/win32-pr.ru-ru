---
description: Фильтр смешивания наложений
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Фильтр смешивания наложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894097"
---
# <a name="overlay-mixer-filter"></a>Фильтр смешивания наложений

Фильтр микшера наложения — это модуль подготовки видео, разработанный специально для воспроизведения DVD-дисков и широковещательных видеопотоков с закрытым субтитром Line-21. Микшер наложения также поддерживает расширения видеопортов (Впес), позволяя работать с аппаратными декодерами MPEG-2 или аналоговыми ТЕЛЕВИЗИОНными тюнерами, которые отправляют видео непосредственно на графическую карту, а не через шину PCI.

> [!Note]  
> Модуль [подготовки видео 9](video-mixing-renderer-filter-9.md) теперь является предпочтительным для фильтра микшера наложения, за исключением сценариев впе.

 

Микшер наложения использует DirectDraw для подготовки к просмотру. Для этого требуется наложение поверхности на графической карте. Основной видеопоток должен быть подключен к ПИН-коду 0. Вторичные потоки (рисунки с субтитрами или изображения DVD) подключены к контактам 1 и выше. Микшер наложения блитс вторичные потоки непосредственно на основной суфаце; Он не смешивается и не использует альфа-смешение.

Микшер наложения использует модуль подготовки видео для управления окнами. Модуль подготовки видео подключается к выходному закрепления микшера наложения.

Этот фильтр автоматически добавляется к графу фильтра, когда приложения используют интерфейсы [**идвдграфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) и [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) для создания графа. Диспетчер графов фильтров не будет автоматически добавлять микшер наложения к графу.

> [!Note]  
> В следующей таблице подтипы мультимедиа, принятые на входном ПИН-коде 0, зависят от оборудования. Микшер оверлея не может определить, поддерживается ли конкретный подтип, пока не создаст поверхность DirectDraw. Таким образом, единственным способом, с помощью которого восходящий фильтр определяет, поддерживается ли подтип, является попытка подключения к этому подтипу.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>Иамоверлайфкс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>иамвидеодеЦиматионпропертиес</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a>, <a href="ikspropertyset.md"><strong>икспропертисет</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Основной тип: MEDIATYPE_Video<br/> Подтипы<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (только ПИН-код 0)</li>
<li>Форматы YUV для DirectDraw (только ПИН-код)</li>
<li>Форматы ускорения видео DirectDraw (только ПИН-код 0)</li>
<li>Форматы DirectDraw RGB (все входные ПИН-коды)</li>
</ul>
Типы форматов:<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Иамвидеоакцелератор</strong></a>, <a href="ikspin.md"><strong>икспин</strong></a>, <a href="ikspropertyset.md"><strong>икспропертисет</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>имиксерпинконфиг</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>иоверлай</strong></a> (только ПИН-код 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств.</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>qdvd.dll</td>
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



 

### <a name="remarks"></a>Комментарии

Микшер наложения использует сочетание цветов назначения для смешивания поверхностей видео с наложенными слоями. Он блитс цветовой ключ и вторичное видео на основную поверхность и отправляет основное видео в область наложения. Затем графическая карта комбинирует две поверхности в буфер фрейма.

Чтобы проверить, поддерживает ли графический драйвер наложение оборудования, вызовите метод **IDirectDraw7:: Caps**. Если поле **двмаксвисиблеоверлайс** в структуре **ддкапс** больше нуля, драйвер поддерживает наложение оборудования.

Приложения могут управлять поведением микшера наложения через интерфейс [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . Разработчики игр могут использовать микшер наложения для показа видео в режиме исключительного использования DirectDraw, как описано далее в этом разделе. [Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9) теперь обеспечивает лучшую поддержку видео в играх. Дополнительные сведения см. [в разделе Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md).

Ниже приведены сведения о преимуществах для разработчиков фильтров, а также разработчиков игр, желающих использовать микшер наложения в режиме исключительного использования DirectDraw.

**Внутренние операции микшера наложения**

Микшер наложения предоставляет входной ПИН-код для каждого входящего потока. Как правило, существует три входных контакта: ПИН-код 0 для видеоданных и контакты 1 и 2 для строки 21 и подизображения DVD. На внутреннем экране микшер наложения создает объект DirectDraw с основной поверхностью, включающей весь рабочий стол, а также область оверлея, прямоугольник которой определяется размером видеопотока на ПИН-коде 0. Если декодер не задает цветовой ключ, микшер наложения использует цветовые ключи по умолчанию: темно-серый для более новых графических карт и пурпурный для старых 256-цветных карт.

> [!Note]  
> Результаты не определены, если декодер доставляет два вторичных видеопотока одновременно в одном месте на поверхности наложения. (Иногда это происходит с DVD-дисками, содержащими подизображения и строки 21.) Видео может мерцать или отображать только один из потоков.

 

В Windows Vista и более поздних версиях микшер наложения отключает композицию диспетчер окон рабочего стола (DWM), если драйвер экрана поддерживает наложение оборудования. Приложения должны избегать использования фильтра микшера наложения; Вместо этого используйте VMR-9 или Расширенный модуль обработки видео (Евр).

**Вышестоящее подключение с помощью видеодекодера**

Обычно входные контакты микшера перекрытия подключаются к восходящего видеодекодера. Основной видеопоток должен подключаться к ПИН-коду 0. Потоки 21 или субтитры подключаются к закреплениям 1 или выше. Если декодер является программным декодером, который использует только ЦП узла, соединение между декодером и ПИН-кодом 0 является [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Если декодер использует аппаратное ускорение, соединение с закреплением 0 должно использовать [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) инферфаце. Эти два типа соединений являются взаимоисключающими.

Если декодер наводится непосредственно на поверхность наложения, он должен использовать интерфейс [**иоверлай**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) для ПИН-кода 0 и реализовывать интерфейс [**иоверлайнотифи**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

Фильтры, которые создают оболочку аппаратного декодера и подключаются к микшеру наложения через порт видео, должны реализовывать интерфейс [**ивпконфиг**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . Микшер наложения реализует интерфейс [**ивпнотифи**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . Эти два интерфейса позволяют декодеру указать нужные им поверхности наложения и включить микшер наложения для информирования декодера о расположении этих поверхностей в видеопамяти.

Микшер наложения также обеспечивает правильное масштабирование прямоугольника видео. Видеозапись включает в себя определенные проблемы, связанные с масштабированием предварительной версии изображения и захватом кадров видео с чередованием. Если вы разрабатываете фильтр или драйвер WDM для аппаратного устройства видеозаписи, см. Дополнительные сведения по этим темам на страницах справочника по [**ивпконфиг**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) и [**ивпнотифи**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) .

Микшер наложения не используется в сценариях записи 1394 или USB. Он используется в видеозаписи через шину PCI.

**Подчиненное соединение с модулем подготовки видео**

Микшер наложения имеет выходной ПИН-код, который подключается к фильтру модуля [обработки видео](video-renderer-filter.md) . Модуль подготовки видео в данном случае не отображает видео; Он просто управляет окном видео.

Для соединения с закреплением используется интерфейс [**иоверлай**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) , а не интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Модуль подготовки видео передает свой обработчик на экран с помощью микшера наложения на DirectDraw, который управляет вырезанием прямоугольника. Приложения могут управлять модулем подготовки видео с помощью интерфейсов [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) в диспетчере графов фильтров.

**Монопольный режим DirectDraw**

Режим использования режима DirectDraw с наложением позволяет играм отображать видео в некоторой части экрана. В этом режиме микшер наложения выводит видео непосредственно на поверхность DirectDraw, созданную игровым приложением, а не в окно, предоставленное модулем подготовки видео. Это позволяет играм управлять ключом цвета. Микшер наложения предоставляет только один входной ПИН-код в режиме монопольного режима DirectDraw. Это означает, что в этом режиме не может быть выполнено смешение линии 21 или DVD-диска.

Чтобы использовать микшер наложения в режиме энергомонопольного режима DirectDraw, создайте экземпляр микшера наложения и запросите его для интерфейса [**иддравексклмодевидео**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) перед построением графа фильтра. Затем вызовите [**иддравексклмодевидео:: сетддравсурфаце**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) , чтобы указать поверхность DirectDraw для отрисовки. Одним из существенных ограничений этого режима является то, что игра не получает доступ к реальным видео-битам. При использовании **иддравексклмодевидео** приложение создает основную поверхность, а микшер наложения создает поверхность наложения.

Можно также использовать монопольный режим DirectDraw для выполнения безоконной отрисовки (например, на веб-странице), но это не рекомендуется, поскольку микшер наложения не выполняет смешанный режим в этом режиме. Это означает, что не удается отобразить данные из линии 21 или подизображения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




