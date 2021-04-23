---
description: Фильтр источников Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Фильтр источников Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8e2c2f2e575a70d85fdce3d9b8d643e270f721
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909002"
---
# <a name="windows-media-source-filter"></a>Фильтр источников Windows Media

Этот фильтр является устаревшим фильтром источника для® содержимого Windows Media. Он используется проигрывателем Windows Media 6,4. Как правило, самый простой и надежный способ использовать этот фильтр — использовать элемент управления ActiveX проигрывателя Windows Media 6,4. Многие методы, предоставляемые этим фильтром, также доступны через элемент управления ActiveX. Дополнительные сведения см. в разделе пакет SDK для проигрывателя Windows Media.

Когда этому фильтру присваивается имя локального ASF-файла или URL для удаленного файла, он считывает файл, анализирует сжатые потоки и создает выходной ПИН-код для каждого из них. Этот фильтр не использует пакет SDK для формата Windows Media. Он использует устанавливаемые кодеки декодеров Windows Media, а не версии DMO. ПИН-код звука всегда подключается к фильтру обработчика ASF ACM, и видео всегда подключается к обработчику ICM. (ICM в этом случае относится к исходному имени диспетчера сжатия видео.) Фильтр не поддерживает поиск.

На следующей схеме показан граф фильтра с этим фильтром.

![граф фильтра источников Windows Media](images/wms-wmv-graph.png)

Для обеспечения обратной совместимости с проигрывателем Windows Media 6,4 этот фильтр является фильтром источников по умолчанию для файлов с расширениями WMA, WMV и ASF. Для воспроизведения файлов более новые приложения должны использовать фильтр [чтения WM ASF](wm-asf-reader-filter.md) . Однако модуль чтения WM ASF не поддерживает воспроизведение потокового содержимого.

Самый простой способ воспроизведения потокового содержимого на основе Windows Media — использовать пакет SDK для проигрывателя Windows Media. Другой вариант — использовать пакет SDK Windows Media Format. Не рекомендуется пытаться создать пользовательский проигрыватель на основе фильтра источников Windows Media.



| Метка | Значение |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иамчаннелинфо**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**иамекстендедсикинг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**иамнетшовконфиг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Типы носителей входных закрепления                    | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Интерфейсы входных закрепления                     | Не применяется                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Типы носителей для выходного ПИН-кода                   | Зависит от потоков в файле ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Фильтровать CLSID                             | См. примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Исполняемый объект                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Заслуживают](merit.md)                       | неуспешный \_ режим                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Комментарии

CLSID фильтра не определен в кнетворк. h. Используйте этот макрос в своем собственном файле заголовка:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Фильтр чтения WM ASF](wm-asf-reader-filter.md)
</dt> </dl>

 

 



