---
title: Форматы входных данных видео
description: Форматы входных данных видео
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, форматы входных данных видео
- Формат расширенных систем (ASF), форматы входных данных видео
- ASF (расширенный формат систем), форматы входных данных видео
- форматы входных данных видео
- Windows Media Format SDK, форматы видео
- Расширенный формат систем (ASF), форматы видео
- ASF (расширенный формат систем), форматы видео
- форматы видео
- Кодек Windows Media Video 9, форматы входных видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105691480"
---
# <a name="video-input-formats"></a>Форматы входных данных видео

Модуль записи принимает следующие форматы видео в качестве входных данных для сжатия с помощью кодека Windows Media Video 9:

-   ВММЕДИАСУБТИПЕ \_ ийув
-   ВММЕДИАСУБТИПЕ \_ I420
-   ВММЕДИАСУБТИПЕ \_ YV12
-   ВММЕДИАСУБТИПЕ \_ YUY2
-   ВММЕДИАСУБТИПЕ \_ UYVY
-   ВММЕДИАСУБТИПЕ \_ ивю
-   ВММЕДИАСУБТИПЕ \_ YVU9
-   ВММЕДИАСУБТИПЕ \_ RGB32
-   ВММЕДИАСУБТИПЕ \_ Rgb24
-   ВММЕДИАСУБТИПЕ \_ RGB565
-   ВММЕДИАСУБТИПЕ \_ RGB555
-   ВММЕДИАСУБТИПЕ \_ RGB8

Следует всегда использовать [**ивмвритер:: жетинпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) и [**Ивмвритер:: жетинпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) для перечисления доступных входных форматов и получения входного объекта свойств носителя для требуемого формата. Видео входные свойства мультимедиа необходимо изменить, чтобы отразить размер кадра и частоту кадров входного носителя.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Идентификаторы типов мультимедиа**](media-type-identifiers.md)
</dt> <dt>

[**Типы носителей**](media-types.md)
</dt> </dl>

 

 




