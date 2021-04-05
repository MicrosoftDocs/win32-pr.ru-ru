---
description: Интерфейсы кодирования и декодирования файлов
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Интерфейсы кодирования и декодирования файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140715"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Интерфейсы кодирования и декодирования файлов

Эти интерфейсы поддерживают кодирование и декодирование файлов.



| Интерфейс                                                    | Описание                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Извлечение метаданных из потока, например автора и заголовка.                                              |
| [**иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Определите ход выполнения операции открытия файла.                                                             |
| [**иампарсе**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Запросите и задайте время синтаксического анализа для текущей позицией в потоке MPEG.                                     |
| [**иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Управление воспроизведением логических потоков и получение сведений о них.                               |
| [**иамвфвкомпрессдиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Отображение диалоговых окон, предоставляемых кодеками VFW.                                                                 |
| [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Задайте параметры сжатия видео.                                                                            |
| [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Управление тем, как фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) записывает файлы ASF. |
| [**иконфигавимукс**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Управление процессом записи AVI файлов с помощью фильтра [мультиплексора AVI](avi-mux-filter.md) .                                       |
| [**иконфигинтерлеавинг**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Настройка вывода при записи файлов AVI с помощью фильтра мультиплексора AVI.                                             |
| [**идвенк**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Задайте разрешение кодирования в фильтре [видео кодировщика DV](dv-video-encoder-filter.md) .                   |
| [**идвсплиттер**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Понижение частоты кадров для цифрового видеопотока (DV)                                                      |
| [**иипдвдек**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Задайте разрешение декодирования для фильтра [видеодекодера DV](dv-video-decoder-filter.md) .                   |
| [**иперсистмедиапропертибаг**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Установка и получение сведений и отображаемых блоков в потоках AVI.                                                        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы](interfaces.md)
</dt> </dl>

 

 



