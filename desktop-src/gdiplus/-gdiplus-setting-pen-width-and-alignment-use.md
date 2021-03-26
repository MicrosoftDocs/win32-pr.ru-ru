---
description: 'При создании объекта Pen можно указать ширину пера в качестве одного из аргументов конструктора. Можно также изменить ширину пера с помощью метода Pen:: Сетвидс.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Задание ширины и выравнивания пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551358"
---
# <a name="setting-pen-width-and-alignment"></a>Задание ширины и выравнивания пера

При создании объекта [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) можно указать ширину пера в качестве одного из аргументов конструктора. Можно также изменить ширину пера с помощью метода [**Pen:: сетвидс**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .

Теоретическая линия имеет нулевую ширину. При рисовании линии Пиксели центрируются по теоретической линии. В следующем примере указанная строка рисуется дважды: один с черным пером толщиной 1 и один раз с зеленым пером шириной 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



На следующем рисунке показаны выходные данные предыдущего кода. Зеленые пиксели и черные пиксели центрируются по теоретической линии.

![Иллюстрация, показывающая тонкую, диагональную, черную линию, окруженную толстой зеленой линией ](images/pens1a.png)

В следующем примере указанный прямоугольник рисуется дважды: один с черным пером толщиной 1 и один раз с зеленым пером шириной 10. Код передает значение **пеналигнментцентер** (элемент перечисления [**пеналигнмент**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) методу [**Pen:: сеталигнмент**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) , чтобы указать, что пикселы, рисуемые зеленым пером, центрируются по границе прямоугольника.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



На следующем рисунке показаны выходные данные предыдущего кода. Зеленые пиксели центрируются по теоретическому прямоугольнику, который представлен черными пикселами.

![Иллюстрация, показывающая тонкую черную линию в фигуре прямоугольника, окруженная зеленой зеленой линией](images/pens2.png)

Можно изменить выравнивание зеленого пера, изменив третью оператор в предыдущем примере следующим образом:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Теперь пикселы в широкой зеленой линии появятся на внутреннем прямоугольнике, как показано на следующем рисунке.

![Иллюстрация, показывающая тонкую черную линию в фигуре прямоугольник, включающую широкую зеленую линию той же фигуры](images/pens3.png)

 

 



