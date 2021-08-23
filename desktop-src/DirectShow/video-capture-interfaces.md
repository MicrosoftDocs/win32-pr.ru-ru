---
description: Интерфейсы видеозаписи
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Интерфейсы видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633064"
---
# <a name="video-capture-interfaces"></a>Интерфейсы видеозаписи

эти интерфейсы поддерживают видеозапись, с помощью устройств microsoft® Windows® Driver Model (WDM) или устаревшего видео microsoft® video для устройств Windows® (VFW).



| Интерфейс                                                        | Описание                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**иаманалогвидеодекодер**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Управление цифрами видео на карте записи видео WDM.                                                      |
| [**иамбуффернеготиатион**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Управление способом выделения буфера с помощью ПИН-кода.                                                                         |
| [**иамкопикаптурефилепрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Интерфейс обратного вызова для получения сведений о ходе операции копирования файла.                                         |
| [**иамкроссбар**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Создание аппаратного подключения между источником аудио-или видеопотока WDM и устройством записи WDM.                   |
| [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Запросите фильтр записи о производительности захвата.                                                            |
| [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Управление временем запуска и окончания отдельных потоков.                                                      |
| [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Запросите и задайте формат вывода фильтра записи.                                                            |
| [**иамвфвкаптуредиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Отображение диалоговых окон, предоставляемых драйверами записи VFW.                                                    |
| [**иамвидеоконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Управление изображением с устройства записи.                                                                   |
| [**иамвидеопрокамп**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Настройте качество видеосигнала, например яркость, контрастность, цветовой тон, насыщенность, гамма и четкость. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Создание графов фильтра для видеозаписи.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Укажите имя и атрибуты выходного файла.                                                           |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы управления внешними устройствами](external-device-control-interfaces.md)
</dt> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



