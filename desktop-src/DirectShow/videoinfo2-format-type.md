---
description: Тип формата VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Тип формата VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683072"
---
# <a name="videoinfo2-format-type"></a>Тип формата VideoInfo2

Предпочитаемый тип носителя для предварительного просмотра может быть типом с форматом [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Эта структура формата поддерживает специальные функции, такие как чередование изображений и пропорций изображения.

VMR-7 и VMR-9 поддерживают [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) напрямую. При подключении VMR к декодеру они будут согласовывать оптимальный формат. Однако старый фильтр модуля подготовки отчетов не поддерживает **VIDEOINFOHEADER2**. Чтобы использовать типы форматов **VIDEOINFOHEADER2** с фильтром модуля подготовки отчетов, необходимо вставить фильтр [микшера наложения](overlay-mixer-filter.md) на диаграмму.

1.  Перечислите предпочтительные типы носителей в закреплениях вывода фильтра декодера с помощью метода [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Проверьте первый тип носителя в последовательности перечисления.
3.  Если используется формат формата **\_ VideoInfo2**, подключите выходной закрепление к микшеру наложения. Затем подключите микшер наложения к модулю подготовки видео. (См. раздел [Контакты порта видео](video-port-pins.md).)

Если вы не следите за этими функциями, не нужно использовать микшер наложения. Подключите декодер непосредственно к модулю визуализации видео, и он подключится к формату [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> <dt>

[Использование микшера наложения в видеозаписи](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



