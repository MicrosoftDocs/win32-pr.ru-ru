---
description: Сведения о фильтре средства чтения ASF-файлов WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Сведения о фильтре средства чтения ASF-файлов WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894982"
---
# <a name="about-the-wm-asf-reader-filter"></a>Сведения о фильтре средства чтения ASF-файлов WM

Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) . Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока. В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков. Чтобы воспроизвести файл ASF с фильтром чтения WM ASF, вызовите метод [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или [**Играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

Модуль чтения WM ASF поддерживает интерфейс DirectShow [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , позволяющий приложениям выполнять временное Поиск в файле. Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)), не поддерживается.

Фильтр чтения WM ASF также предоставляет несколько интерфейсов Windows Media Format SDK, как описано в следующей таблице. Эти интерфейсы описаны в документации пакета Windows Media Format SDK.



| Интерфейс                                             | Как предоставлено                                 | Комментарии                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Через **IServiceProvider** в фильтре. | Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM).                             |
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** в фильтре.           | Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.     |
| [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** в фильтре.           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** в фильтре.           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам в формате объекта чтения SDK. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



