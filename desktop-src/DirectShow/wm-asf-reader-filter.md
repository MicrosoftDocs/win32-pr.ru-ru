---
description: Сведения о фильтре модуля чтения WM ASF для DirectShow. это фильтр оболочки для объекта модуля чтения, поставляемого с пакетом SDK для Windows Media Format.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Фильтр чтения WM ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e87642637e7a210707c049d9b3c6a1a431b0a277774ce432b1c5c962ff2f317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049164"
---
# <a name="wm-asf-reader-filter-directshow"></a>Фильтр чтения WM ASF (DirectShow)

модуль чтения WM ASF — это фильтр оболочки для объекта reader, поставляемого с пакетом SDK для Windows media Format, который является рекомендуемым фильтром источника для воспроизведения файлов Windows содержимого и содержимого, созданных с помощью любого дмос кодировщика Microsoft MPEG-4.



| Метка | Значение |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**иамекстендедсикинг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** кроме того, фильтр предоставляет следующие Windows интерфейсы SDK формата мультимедиа: [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (через **IServiceProvider**).<br/> |
| Типы носителей входных закрепления                    | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Интерфейсы входных закрепления                     | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Типы носителей для выходного ПИН-кода                   | МУЛЬТИМЕДИЙное \_ видео, MediaType \_ Audio, MediaType \_ команду скрипта, MediaType \_ филетрансфер                                                                                                                                                                                                                                                                                                                                                                                                     |
| Интерфейсы выходного ПИН-кода                    | [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**иамвмбуфферпасс**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider**, кроме того, пин-коды предоставляют следующие Windows интерфейсы SDK формата мультимедиа: **IWMStreamConfig2** (через **IServiceProvider**).<br/>                                                                                                                                                                                                                                    |
| Фильтровать CLSID                             | \_ВМАСФРЕАДЕР CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID страницы свойств                      | Нет страницы свойств.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Исполняемый объект                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Remarks

При наличии имени файла ASF или URL-адреса средство чтения WM ASF считывает сжатое содержимое, анализирует сжатые потоки и предоставляет закрепление вывода для каждого из них. Этот фильтр подключается к фильтрам аудио-и видеокодеков, которые выполняют распаковку. Поиск поддерживается, если ASF-файл доступен для поиска. Время чтения ASF помечает образцы перед их прямой отправкой, но не изменяет метки времени каким бы то ни было образом.

Воспроизведение с тактовой частотой, отличной от 1,0 (как указано в [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)), не поддерживается.

когда среда выполнения пакета SDK Windows Media Format отправляет сообщения [**\_ о состоянии вмт**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) в фильтр модуля записи WM ASF, фильтр перенаправляет все сообщения, связанные с получением лицензии DRM, в виде событий [**\_ \_ событий EC вмт**](ec-wmt-event.md) . Дополнительные сведения см. [в разделе read DRM-Protected ASF Files in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

Читатель WM ASF частично реализует интерфейсы [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) и [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) , чтобы предоставить приложениям доступ к информационным методам объекта Reader. Реализация фильтра просто передает вызовы в интерфейс объекта Reader. Методы потоковой передачи не реализованы, поскольку фильтр должен иметь полный контроль над процессом потоковой передачи. Реализуются следующие методы:

-   [**Ивмреадерадванцед:: Statistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**Ивмреадерадванцед:: SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2:: Жетбуфферпрогресс**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2:: Жетдовнлоадпрогресс**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: Жетплаймоде**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: Жетпротоколнаме**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2:: Сетлогклиентид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: Сетплаймоде**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
