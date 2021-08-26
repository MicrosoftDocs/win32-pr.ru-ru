---
description: Windows Фильтр источника мультимедиа
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Фильтр источника мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1e617a51095aec7cb409e46ba8f19f14f76fcd6f8d8a9bffeaa13843b1728b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982213"
---
# <a name="windows-media-source-filter"></a>Windows Фильтр источника мультимедиа

этот фильтр является устаревшим фильтром источников для Windows мультимедиа® содержимого. он используется проигрыватель Windows Media 6,4. как правило, самый простой и надежный способ использовать этот фильтр — использовать элемент управления ActiveX проигрыватель Windows Media 6,4. многие методы, предоставляемые этим фильтром, также доступны через элемент управления ActiveX. дополнительные сведения см. в пакете SDK для проигрыватель Windows Media.

Когда этому фильтру присваивается имя локального ASF-файла или URL для удаленного файла, он считывает файл, анализирует сжатые потоки и создает выходной ПИН-код для каждого из них. этот фильтр не использует пакет SDK для Windows Media Format. в нем используются устанавливаемые на основе кодеков Windowsные декодеры мультимедиа, а не DMO версии. ПИН-код звука всегда подключается к фильтру обработчика ASF ACM, и видео всегда подключается к обработчику ICM. (ICM в этом случае относится к исходному имени диспетчера сжатия видео.) Фильтр не поддерживает поиск.

На следующей схеме показан граф фильтра с этим фильтром.

![граф фильтра источников Windows Media](images/wms-wmv-graph.png)

для обеспечения обратной совместимости с проигрыватель Windows Media 6,4 этот фильтр является фильтром источников по умолчанию для файлов с расширениями wma, wmv и asf. Для воспроизведения файлов более новые приложения должны использовать фильтр [чтения WM ASF](wm-asf-reader-filter.md) . Однако модуль чтения WM ASF не поддерживает воспроизведение потокового содержимого.

самый простой способ воспроизведения потокового Windows содержимого на основе носителя — использовать пакет SDK для проигрыватель Windows Media. кроме того, можно использовать пакет SDK для Windows Media Format. не рекомендуется пытаться создать пользовательский проигрыватель на основе фильтра источника Windows носителей.



| Метка | Значение |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**иамчаннелинфо**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**иамекстендедсикинг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**иамнетшовконфиг**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Типы носителей входных закрепления                    | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Интерфейсы входных закрепления                     | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Типы носителей для выходного ПИН-кода                   | Зависит от потоков в файле ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Фильтровать CLSID                             | См. примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Исполняемый объект                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Заслуживают](merit.md)                       | неуспешный \_ режим                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Remarks

CLSID фильтра не определен в кнетворк. h. Используйте этот макрос в своем собственном файле заголовка:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Фильтр чтения WM ASF](wm-asf-reader-filter.md)
</dt> </dl>

 

 



