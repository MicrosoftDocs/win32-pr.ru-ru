---
description: Фильтр мультиплексора AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Фильтр мультиплексора AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f923ed944781bbaa36179b02db9022f38fc98ff6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478640"
---
# <a name="avi-mux-filter"></a>Фильтр мультиплексора AVI

Фильтр мультиплексора AVI принимает несколько входных потоков и покидает их в формате AVI. Фильтр использует отдельные входные сигналы для каждого входного потока и один выходной ПИН-код для потока AVI.

С помощью этого фильтра можно сохранять файлы на диск в формате AVI. Фильтр обычно подключается к фильтру [записи файлов](file-writer-filter.md) , но может подключаться к любому фильтру, чей входной ПИН-код поддерживает интерфейсы IStream и [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>иконфигавимукс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>иконфигинтерлеавинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>иперсистмедиапропертибаг</strong></a>, ISpecifyPropertyPages | | Типы входных закрепления Любой основной тип, соответствующий старому типу FOURCC или MEDIATYPE_AUXLine21Data. (Дополнительные сведения см. в разделе <a href="fourccmap.md"><strong>класс фаурккмап</strong></a>.)<ul><li>Если основной тип — MEDIATYPE_Audio, формат должен быть FORMAT_WaveFormatEx.</li><li>Если основной тип — MEDIATYPE_Video, формат должен быть FORMAT_VideoInfo или FORMAT_DvInfo.</li><li>Если основной тип — MEDIATYPE_Interleaved, формат должен быть FORMAT_DvInfo.</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>Иамстреамконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, ипропертибаг, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления MEDIATYPE_Stream, MEDIASUBTYPE_Avi | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_AviDest | | CLSID страницы свойств | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | | Исполняемый файл | qcap.dll | | <a href="merit.md"></a> Кому | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Комментарии

В следующих примечаниях описаны различные аспекты функциональности фильтра мультиплексора AVI.

Маркеры

При создании фильтра мультиплексора формата AVI он имеет один входной ПИН-код. При подключении каждого входного ПИН-кода фильтр создает новый входной ПИН-код.

Свойства потока

Входные контакты поддерживают интерфейс Ипропертибаг для установки свойств отдельных потоков. В настоящее время определено следующее свойство:



| Свойство | Описание                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Имя потока. Это свойство записывается как `'strn'` фрагмент. |



 

Если фильтр запущен или приостановлен, метод Ипропертибаг:: Write возвращает \_ \_ неправильное состояние VFW E \_ .

Частота кадров

Если вышестоящий фильтр не задает частоту кадров в элементе **авгтимеперфраме** структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , то компонент AVI мультиплексор использует метки времени в первом кадре видео. Формат файла AVI не поддерживает переменные частоты кадров.

Удаленные кадры

Фильтр мультиплексора AVI рассчитывает пропущенные кадры на основе значений времени каждого образца, если они доступны, или в качестве штампов времени образца. Он записывает запись индекса нулевой длины для каждого удаленного кадра.

имедиасикинг

Фильтр мультиплексора AVI реализует интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) следующим образом:

-   Метод [**жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) возвращает текущий ход выполнения мультиплексирования. если вы перекодируете файл (медленнее, чем в реальном времени), это значение становится более точным, чем значение, возвращаемое диспетчером Graph Manager. Дополнительные сведения см. в разделе "Примечания" на странице справочника по Жеткуррентпоситион.
-   Метод [**WebMethod**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) запрашивает каждый вышестоящий фильтр и возвращает длительность самого длинного потока. Если какой-либо из этих фильтров не выполняет вызов методаической длительности (или не поддерживает Имедиасикинг), то мультиплексор AVI возвращает код ошибки и заполняет параметр *пдуратион* наиболее длинной длительностью. Однако значение *пдуратион* в этом случае не обязательно является длиной самого длинного входного потока.
-   Мультиплексор AVI не реализует методы Жетстоппоситион, Disposition, Жетпреролл, методомического и недоступности. и не реализует какие бы то ни было \* методы Set для поиска.

Расширения формата файлов AVI 2,0

в настоящее время DirectShow поддерживает следующие расширения формата файлов AVI 2,0:

-   Увеличен размер AVI-файла (более 1 ГБ)
-   Иерархическое индексирование

Дополнительные сведения см. в статье версия 1,02 для расширений формата AVI-файлов Опендмл, опубликованных в Подкомитете формат файла Опендмл AVI M – JPEG.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



