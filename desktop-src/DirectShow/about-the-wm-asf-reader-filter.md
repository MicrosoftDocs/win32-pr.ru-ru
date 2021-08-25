---
description: Сведения о фильтре средства чтения ASF-файлов WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Сведения о фильтре средства чтения ASF-файлов WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873704"
---
# <a name="about-the-wm-asf-reader-filter"></a>Сведения о фильтре средства чтения ASF-файлов WM

Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) . Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока. В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков. Чтобы воспроизвести файл ASF с фильтром чтения WM ASF, вызовите метод [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или [**Играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

модуль чтения WM ASF поддерживает интерфейс DirectShow [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , позволяющий приложениям выполнять временное поиск в файле. Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)), не поддерживается.

фильтр чтения WM ASF также предоставляет несколько Windows интерфейсов пакета SDK для формата мультимедиа, как описано в следующей таблице. эти интерфейсы описаны в документации пакета SDK для Windows Media Format.



| Интерфейс                                             | Как предоставлено                                 | Примечания                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Через **IServiceProvider** в фильтре. | Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM).                             |
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** в фильтре.           | Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.     |
| [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** в фильтре.           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** в фильтре.           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам в формате объекта чтения SDK. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



