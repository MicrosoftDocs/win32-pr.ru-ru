---
description: Windows GDI+ предоставляет контейнеры, которые можно использовать для временной замены или дополнения части состояния в объекте Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Вложенные графические контейнеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114984"
---
# <a name="nested-graphics-containers"></a>Вложенные графические контейнеры

Windows GDI+ предоставляет контейнеры, которые можно использовать для временной замены или дополнения части состояния в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Контейнер создается путем вызова метода [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) объекта **Graphics** . Для формирования вложенных контейнеров можно многократно вызывать **Graphics:: бегинконтаинер** .

## <a name="transformations-in-nested-containers"></a>Преобразования во вложенных контейнерах

В следующем примере создается [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и контейнер внутри этого объекта **Graphics** . Мировым преобразованием **графического** объекта является преобразование единиц измерения 100 в направлении x и 80 единиц по оси y. Универсальное преобразование контейнера — это поворот на 30 градусов. Код вызывает


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



Дважды. Первый вызов [**Graphics::D равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) находится *внутри контейнера*; Это значит, что вызов осуществляется между вызовами [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). Второй вызов **Graphics::D равректангле** — после вызова **Graphics:: ендконтаинер**.


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



В приведенном выше коде прямоугольник, рисуемый внутри контейнера, преобразуется сначала по всему миру контейнера (вращение), а затем по всему миру [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта (перевод). Прямоугольник, рисуемый за пределами контейнера, преобразуется только в мировом преобразовании объекта **Graphics** (перевод). На следующем рисунке показаны два прямоугольника.

![снимок экрана: окно с двумя красными прямоугольниками в центре одной и той же точки, но с разными поворотами](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Обрезка во вложенных контейнерах

В следующем примере показано, как вложенные контейнеры обработают области отсечения. Код создает [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и контейнер внутри этого **графического** объекта. Вырезанная область объекта **Graphics** является прямоугольником, а область обрезки контейнера — эллипсом. Код выполняет два вызова метода [**Graphics::D равлине**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) . Первый вызов **Graphics::D равлине** находится внутри контейнера, а второй вызов **Graphics::D равлине** находится за пределами контейнера (после вызова [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Первая строка обрезается по пересечению двух областей отсечения. Вторая строка обрезается только прямоугольной вырезанной областью объекта **Graphics** .


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



На следующем рисунке показаны две обрезанные линии.

![Иллюстрация эллипса внутри прямоугольника с одной линией, обрезанной с помощью эллипса, а другой — прямоугольником](images/nestedcontainers2.png)

Как показано в двух предыдущих примерах, преобразования и области обрезки являются кумулятивными в вложенных контейнерах. Если задать мировые преобразования контейнера и объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , то оба преобразования будут применяться к элементам, рисуемым внутри контейнера. Преобразование контейнера будет применено первыми, а преобразование объекта **Graphics** будет применено ко второму. Если задать области обрезки контейнера и объекта **Graphics** , то элементы, рисуемые внутри контейнера, будут обрезаны пересечением двух областей отсечения.

## <a name="quality-settings-in-nested-containers"></a>качество Параметры во вложенных контейнерах

Параметры качества ( [**смусингмоде**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**текстрендерингхинт**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)и Like) во вложенных контейнерах не являются накопительными. Вместо этого параметры качества контейнера временно заменяют параметры качества объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . При создании нового контейнера параметры качества для этого контейнера задаются как значения по умолчанию. Например, предположим, что у вас есть **графический** объект с режимом сглаживания [* * * * смусингмодеантиалиас *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * *. При создании контейнера режим сглаживания в контейнере является режимом сглаживания по умолчанию. Вы можете задать режим сглаживания контейнера, и все элементы, отображаемые в контейнере, будут отображаться в соответствии с заданным режимом. Элементы, рисуемые после вызова [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , будут отображаться в соответствии с режимом сглаживания ([* * * * смусингмодеантиалиас *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * *), который находился перед вызовом [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Несколько уровней вложенных контейнеров

Вы не ограничены одним контейнером в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Можно создать последовательность контейнеров, каждый из которых вложен в предыдущий, а также указать объемное преобразование, область отсечения и параметры качества для каждого из этих вложенных контейнеров. Если вызвать метод рисования из самого внутреннего контейнера, то преобразования будут применены по порядку, начиная с самого внутреннего контейнера и заканчивая самым внешним контейнером. Элементы, отображаемые внутри самого внутреннего контейнера, обрезаются пересечением всех областей обрезки.

В следующем примере создается объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и задается его подсказка для отрисовки текста [* * * * текстрендерингхинтантиалиас * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. Код создает два контейнера, один из которых вложен в другой. Подсказка визуализации текста внешнего контейнера имеет значение [* * * * текстрендерингхинтсинглебитперпиксел * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *, а подсказка для отображения текста внутреннего контейнера имеет значение [* * * * текстрендерингхинтантиалиас * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. Код рисует три строки: один из внутреннего контейнера, один из внешнего контейнера, а другой — из самого объекта **Graphics** .


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



На следующем рисунке показаны три строки. Строки, нарисованные из внутреннего контейнера и объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , сглажены с помощью сглаживания. Строка, выведенная из внешнего контейнера, не сглажена с помощью сглаживания из-за параметра Текстрендерингхинтсинглебитперпиксел.

![Иллюстрация прямоугольника, содержащего одну и ту же строку. только символы в первой и последней строках являются гладкими](images/nestedcontainers3.png)

 

 
