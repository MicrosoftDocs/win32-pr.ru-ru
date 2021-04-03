---
description: Разделы, посвященные расширенному записи
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Разделы, посвященные расширенному записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140363"
---
# <a name="advanced-capture-topics"></a>Разделы, посвященные расширенному записи

В этом разделе описаны некоторые дополнительные аспекты видеозаписи в DirectShow. Большинство проблем, описанных в этом разделе, автоматически обрабатываются интерфейсом [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Однако эти сведения могут оказаться полезными, если необходимо устранить неполадки в приложении видеозаписи. Кроме того, этот раздел следует прочесть, если приложение создает собственную диаграмму записи какого-либо типа, и вы обнаружите, что ICaptureGraphBuilder2 не соответствует вашим потребностям. Наконец, в этом разделе содержатся некоторые сведения об использовании фильтра формирователя видео (VMR) в приложении видеозаписи.

Граф видеозаписи можно создать целиком с помощью методов [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Можно также объединить два интерфейса, используя ICaptureGraphBuilder2 для некоторых задач и Играфбуилдер для других.

В этом разделе рассматриваются следующие вопросы.

-   [Обработка событий перерисовки в видеозаписи](handling-repaint-events-in-video-capture.md)
-   [Работа с категориями ПИН-кодов](working-with-pin-categories.md)
-   [Использование фильтра Smart Tee](using-the-smart-tee-filter.md)
-   [Использование микшера наложения в видеозаписи](using-the-overlay-mixer-in-video-capture.md)
-   [ПИН-коды порта видео](video-port-pins.md)
-   [Тип формата VideoInfo2](videoinfo2-format-type.md)
-   [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md)
-   [Фильтры драйвера класса WDM](wdm-class-driver-filters.md)
-   [Использование захвата WDDM в DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



