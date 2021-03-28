---
description: 'Можно заполнить путь, передав адрес объекта GraphicsPath методу Graphics:: Филлпас.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Заполнение открытых фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559917"
---
# <a name="filling-open-figures"></a>Заполнение открытых фигур

Можно заполнить путь, передав адрес объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) методу [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) . Метод **Graphics:: филлпас** заполняет путь в соответствии с режимом заполнения (альтернативным или обмоткой), установленным в данный момент для пути. Если путь содержит какие-либо открытые фигуры, то путь будет заполнен так, как будто эти фигуры были закрыты. GDI+ закрывает фигуру, рисуя прямую линию от конечной точки до ее начальной точки.

В следующем примере создается путь, который содержит одну открытую фигуру (дугу) и одну замкнутую фигуру (эллипс). Метод [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет путь в соответствии с заданным по умолчанию режимом заполнения, который является филлмодеалтернате.


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



На следующем рисунке показаны выходные данные предыдущего кода. Обратите внимание, что путь заполнен (в соответствии с Филлмодеалтернате), как если бы открытая фигура была замкнута с помощью прямой линии от конечной точки до ее начальной точки.

![Иллюстрация, показывающая высоту эллипса, которая пересекает нижнюю половину расширенного эллипса; объединение заполнено, но пересечение пусто](images/fillopenpath.png)

 

 



