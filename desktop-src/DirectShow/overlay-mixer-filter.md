---
description: Фильтр смешивания наложений
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Фильтр смешивания наложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476990"
---
# <a name="overlay-mixer-filter"></a>Фильтр смешивания наложений

наложение Mixer фильтр — это модуль подготовки видео, разработанный специально для воспроизведения DVD-дисков и вещания видеопотоков с субтитрами в виде 21 строки. наложение Mixer также поддерживает расширения видеопортов (впес), позволяя работать с аппаратными декодерами MPEG-2 или аналоговыми телевизионными тюнерами, которые отправляют видео непосредственно на графическую карту, а не через шину PCI.

> [!Note]  
> модуль [подготовки видео 9](video-mixing-renderer-filter-9.md) теперь является предпочтительным для Mixer фильтра, за исключением сценариев впе.

 

наложение Mixer использует DirectDraw для отрисовки. Для этого требуется наложение поверхности на графической карте. Основной видеопоток должен быть подключен к ПИН-коду 0. Вторичные потоки (рисунки с субтитрами или изображения DVD) подключены к контактам 1 и выше. наложение Mixer блитс вторичные потоки непосредственно на основной суфаце; Он не смешивается и не использует альфа-смешение.

наложение Mixer использует модуль подготовки видео для управления окнами. модуль подготовки отчетов подключается к закреплениям вывода Mixer наложения.

Этот фильтр автоматически добавляется к графу фильтра, когда приложения используют интерфейсы [**идвдграфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) и [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) для создания графа. фильтр Graph Manager не будет автоматически добавлять наложение Mixer на граф.

> [!Note]  
> В следующей таблице подтипы мультимедиа, принятые на входном ПИН-коде 0, зависят от оборудования. наложение Mixer не может определить, поддерживается ли конкретный подтип, пока не создаст поверхность DirectDraw. Таким образом, единственным способом, с помощью которого восходящий фильтр определяет, поддерживается ли подтип, является попытка подключения к этому подтипу.

 




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>Иамоверлайфкс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>иамвидеодеЦиматионпропертиес</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a>, <a href="ikspropertyset.md"><strong>икспропертисет</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Типы входных закрепления Основной тип: MEDIATYPE_Video<br /> Подтипы<br /><ul><li>MEDIASUBTYPE_Overlay (только ПИН-код 0)</li><li>Форматы YUV для DirectDraw (только ПИН-код)</li><li>Форматы ускорения видео DirectDraw (только ПИН-код 0)</li><li>Форматы DirectDraw RGB (все входные ПИН-коды)</li></ul>Типы форматов:<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | | Интерфейсы входных закрепления | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Иамвидеоакцелератор</strong></a>, <a href="ikspin.md"><strong>икспин</strong></a>, <a href="ikspropertyset.md"><strong>икспропертисет</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>имиксерпинконфиг</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>иоверлай</strong></a> (только ПИН-код 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Типы выходных закрепления MEDIATYPE_Video, MEDIASUBTYPE_Overlay | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_OverlayMixer | | CLSID страницы свойств | Нет страницы свойств. | | Исполняемый файл | qdvd.dll | | <a href="merit.md"></a> Кому | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Комментарии

наложение Mixer использует сочетание цветов назначения для смешивания поверхностей видео с наложенными слоями. Он блитс цветовой ключ и вторичное видео на основную поверхность и отправляет основное видео в область наложения. Затем графическая карта комбинирует две поверхности в буфер фрейма.

Чтобы проверить, поддерживает ли графический драйвер наложение оборудования, вызовите метод **IDirectDraw7:: Caps**. Если поле **двмаксвисиблеоверлайс** в структуре **ддкапс** больше нуля, драйвер поддерживает наложение оборудования.

приложения могут управлять некоторыми поведениями наложения Mixer через интерфейс [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . разработчики игр могут использовать наложение Mixer для показа видео в режиме исключительного использования DirectDraw, как описано далее в этом разделе. [Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9) теперь обеспечивает лучшую поддержку видео в играх. Дополнительные сведения см. [в разделе Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md).

ниже приведены сведения о преимуществах разработчиков фильтров и разработчиков игр, желающих использовать наложение Mixer в режиме энергоисключающего режима DirectDraw.

**наложение Mixer внутренних операций**

наложение Mixer предоставляет входной пин-код для каждого входящего потока. Как правило, существует три входных контакта: ПИН-код 0 для видеоданных и контакты 1 и 2 для строки 21 и подизображения DVD. на внутреннем уровне Mixer наложение создает объект DirectDraw с основной поверхностью, включающей весь рабочий стол, а также область оверлея, прямоугольник которой определяется размером видеопотока на пин-коде 0. если в декодере не указан цветовой ключ, наложение Mixer использует цветовые ключи по умолчанию: темно-серый для более новых графических карт и пурпурный для более старых 256-цветных карт.

> [!Note]  
> Результаты не определены, если декодер доставляет два вторичных видеопотока одновременно в одном месте на поверхности наложения. (Иногда это происходит с DVD-дисками, содержащими подизображения и строки 21.) Видео может мерцать или отображать только один из потоков.

 

в Windows Vista и более поздних версиях наложение Mixer отключает композицию диспетчер окон рабочего стола (DWM), если драйвер экрана поддерживает наложение оборудования. приложения должны избегать использования наложения Mixer фильтра; Вместо этого используйте VMR-9 или Расширенный модуль обработки видео (Евр).

**Вышестоящее подключение с помощью видеодекодера**

как правило, входные контакты Mixer оверлея подключаются к восходящего видеодекодера. Основной видеопоток должен подключаться к ПИН-коду 0. Потоки 21 или субтитры подключаются к закреплениям 1 или выше. Если декодер является программным декодером, который использует только ЦП узла, соединение между декодером и ПИН-кодом 0 является [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Если декодер использует аппаратное ускорение, соединение с закреплением 0 должно использовать [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) инферфаце. Эти два типа соединений являются взаимоисключающими.

Если декодер наводится непосредственно на поверхность наложения, он должен использовать интерфейс [**иоверлай**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) для ПИН-кода 0 и реализовывать интерфейс [**иоверлайнотифи**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

фильтры, которые заключают аппаратный декодер и подключаются к наложению, Mixer через порт видео, должны реализовывать интерфейс [**ивпконфиг**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . наложение Mixer реализует интерфейс [**ивпнотифи**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . эти два интерфейса позволяют декодеру указать нужные им поверхности наложения и включить Mixer наложения для информирования декодера о расположении этих поверхностей в видеопамяти.

наложение Mixer также обеспечивает правильное масштабирование прямоугольника видео. Видеозапись включает в себя определенные проблемы, связанные с масштабированием предварительной версии изображения и захватом кадров видео с чередованием. Если вы разрабатываете фильтр или драйвер WDM для аппаратного устройства видеозаписи, см. Дополнительные сведения по этим темам на страницах справочника по [**ивпконфиг**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) и [**ивпнотифи**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) .

наложение Mixer не используется в сценариях записи 1394 или USB. Он используется в видеозаписи через шину PCI.

**Подчиненное соединение с модулем подготовки видео**

наложение Mixer имеет выходной пин-код, который подключается к фильтру модуля [подготовки видео](video-renderer-filter.md) . Модуль подготовки видео в данном случае не отображает видео; Он просто управляет окном видео.

Для соединения с закреплением используется интерфейс [**иоверлай**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) , а не интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . модуль подготовки видео передает его обработчику через наложение Mixer на DirectDraw, который управляет вырезками прямоугольника. приложения могут управлять модулем подготовки видео с помощью интерфейсов [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) в фильтре Graph Manager.

**Монопольный режим DirectDraw**

режим монопольного использования Mixer оверлея позволяет играм отображать видео в некоторой части экрана. в этом режиме наложение Mixer преобразовывает видео непосредственно в поверхность DirectDraw, созданную игровым приложением, а не в окно, предоставленное модулем подготовки видео. Это позволяет играм управлять ключом цвета. наложение Mixer предоставляет только один входной пин-код в режиме монопольного режима DirectDraw. это означает, что в этом режиме не может быть выполнено смешение линии 21 или DVD-диска.

чтобы использовать наложение Mixer в режиме энергомонопольного режима DirectDraw, создайте экземпляр оверлея Mixer и запросите его для интерфейса [**иддравексклмодевидео**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) перед построением графа фильтра. Затем вызовите [**иддравексклмодевидео:: сетддравсурфаце**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) , чтобы указать поверхность DirectDraw для отрисовки. Одним из существенных ограничений этого режима является то, что игра не получает доступ к реальным видео-битам. при использовании **иддравексклмодевидео** приложение создает основную поверхность, а наложение Mixer создает поверхность наложения.

можно также использовать монопольный режим DirectDraw для выполнения безоконной отрисовки (например, на веб-странице), но это не рекомендуется, поскольку наложение Mixer не выполняет смешанный режим в этом режиме. Это означает, что не удается отобразить данные из линии 21 или подизображения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




