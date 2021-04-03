---
title: Вертикальный текст
description: Начиная с Windows 8, DirectWrite имеет ряд новых API, позволяющих использовать вертикальный текст в приложениях.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987554"
---
# <a name="vertical-text"></a>Вертикальный текст

Начиная с Windows 8, [DirectWrite](direct-write-portal.md) имеет ряд новых API, позволяющих использовать вертикальный текст в приложениях.

## <a name="drawing-vertical-text"></a>Рисование вертикального текста

Можно нарисовать вертикальный текст с помощью Direct2D, используя методы [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) . Чтобы нарисовать текст по вертикали, передайте [**дврите \_ \_ направление чтения \_ сверху \_ \_ вниз**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) в метод [**идвритетекстформат:: сетреадингдиректион**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) и [**\_ направление потока дврите \_ \_ прямо \_ \_ влево**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) к методу [**идвритетекстформатсетфловдиректион**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) . Затем можно создать и нарисовать вертикальный объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

## <a name="analyzing-character-orientation"></a>Анализ ориентации символов

Каждый символ имеет предпочтительную ориентацию символов или направление, в котором этот символ должен быть ориентирован на любой направленный макет. Например, в традиционном горизонтальном макете текст на китайском языке и текст для китайского языка ориентированы вертикально. С другой стороны, в вертикальном макете текст на китайском языке остается вертикальным, а Латинский текст поворачивается в 90 градусов. Это различие в ориентации рассматривается в этом примере.

![изображение английского и китайского текста в горизонтальном и вертикальном макетах.](images/vertical-text.png)

Чтобы определить ориентацию текста, необходимо реализовать интерфейсы [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) и [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) . Источник и приемник принимают глифы и позволяют проверить их ориентацию по вертикали.

После реализации источника и приемника вызовите метод [**анализевертикалглифориентатион**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) . В примере образа эта функция возвращает 3 выполнения: "Английский", "中国" и "Английский".

## <a name="going-from-characters-to-glyphs"></a>Переход от символов к глифам

Теперь, когда вы уверены, что выполнение содержит вертикальные глифы, необходимо получить доступ к этим глифам. В приведенном выше примере существует 3 запуска: один с вертикальными глифами и два без. Чтобы перейти от символов к глифам, вызовите [**жетглифиндицес**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Этот метод возвращает соответствующие индексы глифов для символов в примере. Поскольку метод [**анализевертикалглифориентатион**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) возвращает запуск с вертикальными глифами, необходимо вызвать [**жетвертикалглифвариантс**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), возвращающий вертикально ориентированные идентификаторы глифов вместо текущих идентификаторов глифов.

## <a name="drawing-text-vertically"></a>Рисование текста по вертикали

Наконец, необходимо разместить и нарисовать текст. Поскольку текст рисуется по вертикали, необходимо получить дополнительные сведения, чтобы текст латиницы был правильно выведен. Если нарисовать весь текст на центральном базовом плане, то текст латиницы будет переводиться в середину строки. Для правильного согласования текста необходимо иметь доступ как к центральному, так и к базовому показателю латиницы. Используйте метод [**IDWriteTextAnalyzer1:: Onbaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) , чтобы получить числовые значения указанных базовых показателей. Можно вычесть базовый план латиницы из центрального базового плана, чтобы получить смещение между ними.

Все эти сведения позволяют нарисовать текст на экране. Сначала вызовите метод [**жетглифориентатионтрансформ**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) с результатами объектов [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) и [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) .

Если вы используете [Direct2D](rendering-by-using-direct2d.md) , необходимо также задать универсальное преобразование для целевого объекта отрисовки Direct2D для вертикальной отрисовки.

Наконец, вызовите [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) три раза, один раз для каждого блока текста. На двух блоках текста, находящихся на английском языке, необходимо применить смещение, которое вычисляется между линиями латиницы и центральными планами.

Теперь текст в приложении будет отображаться вертикально с правильной ориентацией на глифы.

 

 