---
title: Общие сведения о взаимодействии
description: Содержит сводку по различным технологиям, которые можно использовать с Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, взаимодействие GDI
- Direct2D, взаимодействие GDI+
- Direct2D, взаимодействие
- Direct2D, взаимодействие DirectWrite
- взаимодействие, Direct2D
- взаимодействие, Direct3D
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
- взаимодействие, интерфейс графических устройств (GDI)
- взаимодействие, GDI+
- взаимодействие DirectWrite
- взаимодействие, DirectWrite
- Компонент обработки изображений Windows (WIC)
- WIC (компонент для работы с образами Windows)
- взаимодействие, Windows компонент создания образов (WIC)
- Direct2D, взаимодействие с WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385332"
---
# <a name="interoperability-overview"></a>Общие сведения о взаимодействии

Одна из Direct2D's ключевых функций заключается в обеспечении взаимодействия между Direct2D и другими платформами отрисовки, чтобы разработчики могли использовать определенные сильные стороны каждой платформы, не беспокоясь о компрометации, выбрав одну платформу для всех нужд. В этом разделе перечислены различные платформы, с которыми взаимодействуют Direct2D. В него входят следующие разделы.

-   [Взаимодействие GDI](#gdi-interoperability)
-   [GDI+ Взаимодействие](#gdi-interoperability)
-   [Совместимость с Direct3D](#direct3d-interoperability)
-   [DirectWrite Взаимодействие](#directwrite-interoperability)
-   [Windows Взаимодействие компонента обработки изображений (WIC)](#windows-imaging-component-wic-interoperability)
-   [Связанные темы](#related-topics)

На следующей диаграмме показаны различные платформы, с которыми Direct2D взаимозаменяемыми, и перечислены некоторые методы и интерфейсы, обеспечивающие взаимодействие.

![Схема платформ, Direct2D взаимодействующих с, включая Direct3D 10,1, DirectWrite, WIC, GDI+ и GDI.](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Взаимодействие GDI

Direct2D обеспечивает двухстороннее взаимодействие с GDI. Вы можете использовать [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) для записи содержимого Direct2D в [контекст устройства](/windows/desktop/gdi/device-contexts) GDI (DC) или использовать [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для получения представления контроллера домена для целевого объекта рендеринга.

Дополнительные сведения и примеры см. в статье [Общие сведения о взаимодействии Direct2D и GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>GDI+ Взаимодействие

GDI+ с Direct2D можно использовать так же, как и GDI. вы можете использовать [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) для записи содержимого Direct2D на тот же контроллер домена, что и GDI+ое содержимое. Такой подход позволяет приступить к добавлению содержимого Direct2D в приложения, которые в основном отображаются с помощью GDI+.

Можно также использовать [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для предоставления доступа к контроллеру домена GDI, записывающему с помощью Direct2D, а затем использовать метод [**фромхдк**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) для создания объекта. Этот подход удобен для приложений, которые в основном отображаются с помощью Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности визуализации с GDI+.

## <a name="direct3d-interoperability"></a>Совместимость с Direct3D

Direct2D может использовать целевой объект отрисовки поверхности DXGI (созданный методом [**креатедксгисурфацерендер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) для записи в [идксгисурфаце](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Это действие позволяет добавлять двумерные фоны и интерфейсы в трехмерные сцены и использовать содержимое Direct2D в качестве текстуры для трехмерной модели. Direct2D также может взять [идксгисурфаце](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) и использовать метод [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) для создания растрового представления.

Дополнительные сведения и примеры см. в статье [Общие сведения о взаимодействии Direct2D и Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>DirectWrite Взаимодействие

Direct2D тесно интегрирован с DirectWrite. Direct2D упрощает визуализацию DirectWrite содержимого, предоставляя методы [**DrawText**](id2d1rendertarget-drawtext.md), [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)и [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Windows Взаимодействие компонента обработки изображений (WIC)

Direct2D предоставляет методы [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)и [**креатевикбитмапрендертаржет**](id2d1factory-createwicbitmaprendertarget.md) для управления точечными рисунками WIC.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие сведения о взаимодействии Direct2D и GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Общие сведения о взаимодействии Direct2D и Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 