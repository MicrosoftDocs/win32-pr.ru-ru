---
title: Обрезка с помощью Axis-Alignedного прямоугольника
description: Показывает, как обрезать область с помощью прямоугольника с выровняйтем по осям.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569322"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Обрезка с помощью Axis-Alignedного прямоугольника

В этом разделе описывается, как обрезать изображение с помощью прямоугольника, ориентированного на оси. Этот подход создает только прямоугольные клипы, так как границы содержимого вычисляются по осям прямоугольника. Этот подход более эффективен, чем использование слоев с границами содержимого. Дополнительные сведения см. в разделе[Общие сведения о слоях](direct2d-layers-overview.md).

**Обрезка с помощью прямоугольника обрезки, ориентированного на оси**

1.  Загрузка исходного изображения из ресурса. Сведения о загрузке точечного рисунка см. в разделе [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).
2.  Вызовите [**ID2D1RenderTarget::P ушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , чтобы указать прямоугольник. Команды отрисовки обрезаются до прямоугольника.

3.  Paint исходный образ.
4.  Вызовите [**ID2D1RenderTarget::P опаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , чтобы удалить последний обрезанный по оси клип из целевого объекта прорисовки.

Например, на следующем рисунке исходное растровое изображение слева составляет 200 \* 130 пикселей. Точечный рисунок справа является исходным точечным рисунком, обрезанным по оси с выкрашенным по осям прямоугольником. Размеры (от 20 до 20) до (100, 100).

![Иллюстрация точечного рисунка Голдфиш до и после усечения растрового изображения](images/cliparegion-axisalignedclip.png)

Чтобы создать обрезанное изображение, создайте прямоугольную структуру в качестве области обрезки. Вызовите [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) с областью обрезки и закрасьте исходное изображение. Вызовите [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , чтобы удалить клип из целевого объекта прорисовки. В следующем примере кода показано, как это сделать:


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct2D](reference.md)
</dt> </dl>

 

 