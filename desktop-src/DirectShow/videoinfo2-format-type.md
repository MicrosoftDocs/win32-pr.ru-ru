---
description: Тип формата VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Тип формата VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071928"
---
# <a name="videoinfo2-format-type"></a>Тип формата VideoInfo2

Предпочитаемый тип носителя для предварительного просмотра может быть типом с форматом [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Эта структура формата поддерживает специальные функции, такие как чередование изображений и пропорций изображения.

VMR-7 и VMR-9 поддерживают [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) напрямую. При подключении VMR к декодеру они будут согласовывать оптимальный формат. Однако старый фильтр модуля подготовки отчетов не поддерживает **VIDEOINFOHEADER2**. чтобы использовать типы формата **VIDEOINFOHEADER2** с фильтром модуля подготовки отчетов, необходимо вставить [наложение Mixer](overlay-mixer-filter.md) фильтр в граф.

1.  Перечислите предпочтительные типы носителей в закреплениях вывода фильтра декодера с помощью метода [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Проверьте первый тип носителя в последовательности перечисления.
3.  Если используется формат формата **\_ VideoInfo2**, Соедините выходной закрепление с наложением Mixer. затем подключите наложение Mixer к модулю подготовки видео. (См. раздел [Контакты порта видео](video-port-pins.md).)

Если эти функции не важны, использовать наложение Mixer не нужно. Подключение декодер непосредственно в модуль подготовки видео, он будет подключаться к формату [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> <dt>

[использование наложения Mixer в видеозаписи](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



