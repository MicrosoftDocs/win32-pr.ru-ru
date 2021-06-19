---
description: Сведения об использовании изображений, точечных рисунков и метафайлов. Windows GDI+ предоставляет класс Image для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Использование изображений, точечных рисунков и метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395539"
---
# <a name="using-images-bitmaps-and-metafiles"></a>Использование изображений, точечных рисунков и метафайлов

Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы). Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) наследуют от класса **Image** . Класс **Bitmap** расширяет возможности класса **Image** , предоставляя дополнительные методы для загрузки, сохранения и манипулирования растровыми изображениями. Класс **Metafile** расширяет возможности класса **Image** , предоставляя дополнительные методы для записи и проверки векторных изображений.

В следующих разделах рассматриваются классы [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)и [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) более подробно:

-   [Загрузка и отображение растровых изображений](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [Загрузка и отображение метафайлов](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [Запись метафайлов](-gdiplus-recording-metafiles-use.md)
-   [Обрезка и масштабирование изображений](-gdiplus-cropping-and-scaling-images-use.md)
-   [Вращение, отражение и наклон изображений](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [Использование режима интерполяции для управления качеством изображения во время масштабирования](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [Создание эскизов изображений](-gdiplus-creating-thumbnail-images-use.md)
-   [Использование кэшированного точечного рисунка для повышения производительности](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [Повышение производительности за счет предотвращения автоматического масштабирования](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [Чтение и запись метаданных](-gdiplus-reading-and-writing-metadata-use.md)

 

 



