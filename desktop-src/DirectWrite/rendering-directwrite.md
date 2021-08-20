---
title: DirectWrite подготовки к просмотру
description: DirectWrite подготовки к просмотру
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa640b8963c427b9eaf1d17fd3e4691115a3965d477c5076deb1f5eb05a569db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070594"
---
# <a name="rendering-directwrite"></a>DirectWrite подготовки к просмотру

## <a name="rendering-options"></a>Параметры подготовки к просмотру

Текст с форматированием, описанным только в объекте [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , может быть визуализирован с помощью [Direct2D](../direct2d/direct2d-portal.md), однако существует несколько дополнительных параметров для отрисовки объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Строку, описываемую объектом [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , можно визуализировать с помощью методов, приведенных ниже.

## <a name="1-render-using-direct2d"></a>1. прорисовка с помощью Direct2D

Чтобы отобразить объект [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью Direct2D, используйте метод [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , как показано в следующем коде.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Более подробные сведения о рисовании объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) с помощью [Direct2D](../direct2d/direct2d-portal.md)см. в разделе [Начало работы with DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. прорисовка с помощью пользовательского модуля подготовки текста.

Для отображения с помощью пользовательского модуля подготовки отчетов используется метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , который принимает в качестве аргумента интерфейс обратного вызова, производный от [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) , как показано в следующем коде.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Метод [**идвритетекстлайаут::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) вызывает методы предоставляемого обратного вызова пользовательского модуля подготовки отчетов. Методы [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**дравундерлине**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**дравинлинеобжект**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)и [**дравстрикесраугх**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) выполняют функции рисования.

[**Идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) объявляет методы для рисования выполнения глифа, подчеркивания, перечеркивания и встроенных объектов. Реализация этих методов реализована в приложении. Создание пользовательского модуля подготовки текста позволяет приложению применять дополнительные эффекты при отрисовке текста, например пользовательской заливки или контура. образец пользовательского обработчика текста включен в [пример DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. отрисовка ClearType на поверхность GDI.

В действительности отрисовка на поверхность GDI является примером использования пользовательского модуля подготовки текста. Однако некоторые действия выполняются в форме интерфейса [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .

Чтобы создать этот интерфейс, используйте метод [**идвритегдиинтероп:: креатебитмапрендертаржет**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .

Метод [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) пользовательского обработчика текста вызывает метод [**Идвритебитмапрендертаржет::D равглифрун**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для рисования глифов. Отрисовка подчеркивания, перечеркивания и встроенных объектов должна выполняться пользовательским модулем подготовки отчетов.

Интерфейс [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) преобразуется в контекст устройства (DC) в памяти. Вы получаете маркер этого контроллера домена с помощью метода [**идвритебитмапрендертаржет:: жетмеморидк**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



После выполнения рисования контроллер домена памяти объекта [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) должен быть скопирован на целевую поверхность GDI.

> [!Note]  
> вы также можете передать точечный рисунок на другой тип, например на поверхность GDI+.

 


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



> [!Note]  
> Приложение несет ответственность за визуализацию всех элементов в окне в конце. Сюда входит текст и графика. Это приводит к снижению производительности. Кроме того, при подготовке к просмотру на КОНТРОЛЛЕРе памяти не используется аппаратный ускоренный интерфейс GDI.

 

Более подробный обзор взаимодействия с GDI см. в статье [взаимодействие с GDI](interoperating-with-gdi.md).

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. Прозрачное отображение текста в градациях серого на поверхности GDI. (Windows 8 и более поздние версии)

начиная с Windows 8 можно прозрачно визуализировать текст в градациях серого до поверхности GDI для повышения производительности. Для этого необходимо выполнить следующие действия.

1.  Очистите контроллер памяти, чтобы он был прозрачным.
2.  Отрисовка текста в памяти HDC с помощью сглаживания в оттенках серого (ДВРИТЕ \_ \_ режим сглаживания текста в \_ \_ оттенках серого).
3.  Используйте функцию [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) , чтобы ВИЗУАЛИЗИРОВАТЬ память HDC явным образом на основе конечного целевого параметра HDC.
4.  Повторяйте столько раз, сколько необходимо (скажем, один раз в каждом глифе) и между другими изображениями может быть визуализирован непосредственно в конечный режим HDC без переписывания функцией [**алфабленд**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Прорисовка с помощью Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Отрисовка с использованием пользовательского средства отрисовки текста](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Подготовка к просмотру на поверхности GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Взаимодействие с GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 