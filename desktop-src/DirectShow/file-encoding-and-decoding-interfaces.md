---
description: Интерфейсы кодирования и декодирования файлов
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Интерфейсы кодирования и декодирования файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6654497b0d2407666b286fb74f06a91e66834cfb963b62b7e22eb5755fa30b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639664"
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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы](interfaces.md)
</dt> </dl>

 

 



