---
description: интерфейс графических устройств Microsoft Windows (GDI) позволяет приложениям использовать графику и форматированный текст как на дисплее, так и на принтере.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bbdd515379c5c3d1f2c17ff0b991141b3a40a8cb42594be95e391da6dabb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092544"
---
# <a name="windows-gdi"></a>Windows GDI

## <a name="purpose"></a>Назначение

интерфейс графических устройств Microsoft Windows (GDI) позволяет приложениям использовать графику и форматированный текст как на дисплее, так и на принтере. приложения на основе Windows не обращаются непосредственно к графическому оборудованию. Вместо этого GDI взаимодействует с драйверами устройств от имени приложений.

## <a name="where-applicable"></a>Где применимо

GDI можно использовать во всех приложениях на основе Windows.

## <a name="developer-audience"></a>Аудитория разработчиков

Этот API предназначен для использования программистами C/C++. знание Windows [архитектуры, управляемой сообщениями](../learnwin32/window-messages.md) , является обязательным.

## <a name="run-time-requirements"></a>Требования к среде выполнения

Сведения о том, какие операционные системы требуются для использования определенной функции, см. в разделе "требования" документации по функции.

## <a name="in-this-section"></a>Содержание раздела

-   [Растровые изображения](bitmaps.md)
-   [Кисти](brushes.md)
-   [Усечение](clipping.md)
-   [Цвета](colors.md)
-   [Координатные пространства и преобразования](coordinate-spaces-and-transformations.md)
-   [Контексты устройств](device-contexts.md)
-   [Заполненные фигуры](filled-shapes.md)
-   [Шрифты и текст](fonts-and-text.md)
-   [Линии и кривые](lines-and-curves.md)
-   [Метафайлы](metafiles.md)
-   [Несколько мониторов экрана](multiple-display-monitors.md)
-   [Рисование и рисование](painting-and-drawing.md)
-   [Пути](paths.md)
-   [Перья](pens.md)
-   [Диспетчер очереди печати и печати](/previous-versions//dd162860(v=vs.85))
-   [Прямоугольники](rectangles.md)
-   [Регионы](regions.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectX](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[GDI+](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Windows Получение образа](../wia/-wia-startpage.md)
</dt> </dl>

 

 
