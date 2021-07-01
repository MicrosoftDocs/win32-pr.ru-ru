---
description: Сведения о фильтре модуля чтения WM ASF для DirectShow. Это фильтр оболочки для объекта модуля чтения, поставляемого с пакетом SDK Windows Media Format.
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: Фильтр чтения WM ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330ab870b97fc3e84ccb5b0f726d4f35ef1af147
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118669"
---
# <a name="wm-asf-reader-filter-directshow"></a>Фильтр чтения WM ASF (DirectShow)

Модуль чтения WM ASF — это фильтр оболочки для объекта Reader, предоставляемый с пакетом SDK для Windows Media Format, который является рекомендуемым фильтром источника для воспроизведения содержимого и содержимого на основе Windows Media, созданных с помощью любого дмос кодировщика Microsoft MPEG-4.



| Метка | Значение |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter), [**иамекстендедсикинг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), **IServiceProvider** Кроме того, фильтр предоставляет следующие интерфейсы пакета SDK Windows Media Format: [**Ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo), [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced), [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2), [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (через **IServiceProvider**).<br/> |
| Типы носителей входных закрепления                    | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Интерфейсы входных закрепления                     | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Типы носителей для выходного ПИН-кода                   | МУЛЬТИМЕДИЙное \_ видео, MediaType \_ Audio, MediaType \_ команду скрипта, MediaType \_ филетрансфер                                                                                                                                                                                                                                                                                                                                                                                                     |
| Интерфейсы выходного ПИН-кода                    | [**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**иамвмбуфферпасс**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), **IServiceProvider**, Кроме того, ПИН-коды предоставляют следующие интерфейсы пакета SDK для формата Windows Media: **IWMStreamConfig2** (через **IServiceProvider**).<br/>                                                                                                                                                                                                                                    |
| Фильтровать CLSID                             | \_ВМАСФРЕАДЕР CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID страницы свойств                      | Нет страницы свойств.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Исполняемый объект                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Remarks

При наличии имени файла ASF или URL-адреса средство чтения WM ASF считывает сжатое содержимое, анализирует сжатые потоки и предоставляет закрепление вывода для каждого из них. Этот фильтр подключается к фильтрам аудио-и видеокодеков, которые выполняют распаковку. Поиск поддерживается, если ASF-файл доступен для поиска. Время чтения ASF помечает образцы перед их прямой отправкой, но не изменяет метки времени каким бы то ни было образом.

Воспроизведение с тактовой частотой, отличной от 1,0 (как указано в [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)), не поддерживается.

Когда среда выполнения пакета SDK Windows Media Format отправляет сообщения [**\_ о состоянии ВМТ**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) в фильтр модуля записи WM ASF, фильтр перенаправляет все сообщения, связанные с получением лицензии DRM, в виде событий [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) . Дополнительные сведения см. [в разделе read DRM-Protected ASF Files in DirectShow](reading-drm-protected-asf-files-in-directshow.md).

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

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
