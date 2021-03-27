---
description: Windows GDI+ предоставляет класс Image и класс Bitmap для хранения изображений в памяти и манипуляции изображениями в памяти.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Использование кодировщиков и декодеров изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144854"
---
# <a name="using-image-encoders-and-decoders"></a>Использование кодировщиков и декодеров изображений

Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) для хранения изображений в памяти и манипуляции изображениями в памяти. GDI+ записывает изображения на дисковые файлы с помощью кодировщиков изображений и загружает изображения с дисковых файлов с помощью декодеров изображений. Кодировщик преобразует данные в **образе** или **растровом** объекте в указанный формат дискового файла. Декодер преобразует данные в файле на диске в формат, необходимый для **растровых** объектов **Image** и Bitmap. В GDI+ есть встроенные кодировщики и декодеры, поддерживающие файлы следующих типов:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

В GDI+ также встроены встроенные декодеры, поддерживающие файлы следующих типов:

-   WMF
-   EMF
-   ЗНАЧОК

В следующих разделах более подробно обсуждаются кодировщики и декодеры:

-   [Список установленных кодировщиков](-gdiplus-listing-installed-encoders-use.md)
-   [Список установленных декодеров](-gdiplus-listing-installed-decoders-use.md)
-   [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Определение параметров, поддерживаемых кодировщиком](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Преобразование изображения BMP в изображение PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Задание уровня сжатия JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Преобразование изображения JPEG без потери информации](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Создание и сохранение многокадрового изображения](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Копирование отдельных кадров из образа Multiple-Frame](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



