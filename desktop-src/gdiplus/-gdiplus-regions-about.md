---
description: Регион — это часть поверхности отображения.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Области (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885037"
---
# <a name="regions-gdi"></a>Области (GDI+)

Регион — это часть поверхности отображения. Регионы могут быть простыми (один прямоугольник) или сложными (сочетание многоугольников и замкнутых кривых). На следующем рисунке показаны два региона: одна из которых состоит из прямоугольника, а другая — из контура.

![Иллюстрация, демонстрирующая прозрачную прямоугольную область, перекрывающие непрозрачную изогнутую фигуру](images/aboutgdip02-art27.png)

Регионы часто используются для обрезки и проверки попадания. Обрезка включает в себя ограничения рисования в определенной области экрана (обычно это часть экрана, которую необходимо обновить). Проверка нажатия включает проверку на предмет того, находится ли курсор в определенной области экрана при нажатии кнопки мыши.

Область можно создать из прямоугольника или из контура. Кроме того, можно создавать сложные регионы, объединяя существующие регионы. Класс [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) предоставляет следующие методы для объединения областей: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [XOR](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))и [**Region:: комплементарный**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

Пересечение двух регионов — это набор всех точек, принадлежащих обоим регионам. Объединение — это набор всех точек, принадлежащих одному или другому или обоим регионам. Дополнение региона — это набор всех точек, которые не находятся в регионе. На следующем рисунке показано пересечение и объединение двух регионов на предыдущем рисунке.

![Иллюстрация, демонстрирующая пересечение областей на предыдущем рисунке и их пересечение](images/aboutgdip02-art28.png)

Метод [XOR](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) , применяемый к паре регионов, создает область, содержащую все точки, принадлежащие к одному региону или к другой, но не к обеим. Метод [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) , применяемый к паре регионов, создает область, содержащую все точки в первом регионе, которые не находятся во втором регионе. На следующем рисунке показаны регионы, являющиеся результатом применения методов XOR и Exclude к двум регионам, показанным в начале этого раздела.

![Иллюстрация, показывающая части в любом регионе, но не обе, и часть прямоугольника, которая не пересекается с изогнутой областью](images/aboutgdip02-art29.png)

Для заполнения области требуется объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , объект [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) и объект [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) . Объект **Graphics** предоставляет метод [**Graphics:: филлрегион**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) , а объект **Brush** сохраняет атрибуты заливки, например цвет или шаблон. В следующем примере область заполняется сплошным цветом.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
