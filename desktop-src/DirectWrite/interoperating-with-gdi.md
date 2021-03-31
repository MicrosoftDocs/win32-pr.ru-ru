---
title: Взаимодействие с GDI
description: DirectWrite предоставляет путь перехода от и некоторые возможности взаимодействия с, модели шрифта GDI, а также интерфейсы для отрисовки текста в растровое изображение, которое затем может быть отображено в окне.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, взаимодействие GDI
- DirectWrite, взаимодействие
- совместимость
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070046"
---
# <a name="interoperating-with-gdi"></a>Взаимодействие с GDI

[DirectWrite](direct-write-portal.md) предоставляет путь перехода от и некоторые возможности взаимодействия с, модели шрифта GDI, а также интерфейсы для отрисовки текста в растровое изображение, которое затем может быть отображено в окне.

Этот обзор содержит следующие компоненты.

-   [Введение](#introduction)
-   [Часть 1. Идвритегдиинтероп](#part-1-idwritegdiinterop)
-   [Часть 2. объекты Font](#part-2-font-objects)
-   [Часть 3. Подготовка к просмотру](#part-3-rendering)

## <a name="introduction"></a>Введение

[DirectWrite](direct-write-portal.md) предоставляет методы для преобразования между LOGFONT структурой GDI и интерфейсами шрифтов DirectWrite. Это позволяет использовать GDI для некоторых или всех перечислений и выделений шрифтов, используя преимущества улучшенной функциональности и производительности DirectWrite. DirectWrite также имеет интерфейсы для отрисовки в точечный рисунок, если требуется отображать текст на поверхности GDI.

## <a name="part-1-idwritegdiinterop"></a>Часть 1. Идвритегдиинтероп

Интерфейс [**идвритегдиинтероп**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) используется для преобразования между структурами шрифтов GDI и интерфейсами шрифтов [DirectWrite](direct-write-portal.md) , а также для создания объекта [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) . Получите объект **идвритегдиинтероп** с помощью метода [**Идвритефактори:: жетгдиинтероп**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , как показано в следующем коде.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Часть 2. объекты Font

GDI использует структуру LOGFONT для хранения сведений о шрифте и стиле текста. Метод [**идвритегдиинтероп:: креатефонтфромлогфонт**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) ПРЕОБРАЗУЕТ структуру LOGFONT в объект [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , как показано в следующем коде.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Однако [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) не инкапсулирует все те же сведения, что и LOGFONT. Структура LOGFONT содержит размер шрифта, вес, стиль, подчеркивание, зачеркивание, имя начертания шрифта и другие сведения. Объекты **идвритефонт** содержат сведения о шрифте, его весе и стиле, но не размер шрифта, подчеркивание и т. д. При использовании [DirectWrite](direct-write-portal.md)элементы сведений, такие как эти, инкапсулируются объектом [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) или для конкретных диапазонов текста — объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

У вас есть возможность преобразовать [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) в LOGFONT с помощью [**Идвритегдиинтероп:: конвертфонттологфонт**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Часть 3. Подготовка к просмотру

Для отрисовки текста DirectWrite на поверхности GDI используется настраиваемый модуль подготовки текста. См. раздел [Подготовка к поверхности GDI](render-to-a-gdi-surface.md) .

 

 