---
description: Глобальное преобразование — это преобразование, которое применяется к каждому элементу, рисуемому данным графическим объектом.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Глобальные и локальные преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556120"
---
# <a name="global-and-local-transformations"></a>Глобальные и локальные преобразования

Глобальное преобразование — это преобразование, которое применяется к каждому элементу, рисуемому данным [**графическим**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объектом. Чтобы создать глобальное преобразование, создайте объект **Graphics** , а затем вызовите его метод [**Graphics:: сеттрансформ**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) . Метод **Graphics:: сеттрансформ** управляет объектом [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , связанным с **графическим** объектом. Преобразование, хранящееся в этом объекте **Matrix** , называется *мировым преобразованием*. Преобразование «мир» может быть простым аффинное преобразованием или сложной последовательностью аффинных преобразований, но независимо от его сложности, преобразование «мир» хранится в одном объекте **Matrix** .

Класс [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет несколько методов для создания составного универсального преобразования: [**Graphics:: мултиплитрансформ**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)и [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). В следующем примере эллипс рисуется дважды: один раз перед созданием универсального преобразования и после. Преобразование сначала масштабируется с коэффициента 0,5 в направлении по оси y, затем преобразует 50 единиц в направлении x, а затем поворачивает на 30 градусов.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



На следующем рисунке показан исходный эллипс и преобразованный эллипс.

![снимок экрана: окно, содержащее два перекрывающихся эллипса; один из них является более узким и повернутым](images/aboutgdip05-art14.png)

> [!Note]  
> В предыдущем примере эллипс поворачивается относительно начала координат системы координат, расположенного в верхнем левом углу клиентской области. Результат будет отличаться от того, на котором вращается эллипс относительно своего центра.

 

Локальное преобразование — это преобразование, которое применяется к конкретному рисуемому элементу. Например, объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) имеет метод [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) , позволяющий преобразовывать точки данных этого пути. В следующем примере демонстрируется рисование прямоугольника без преобразования и контура с преобразованием «вращение». (Предположим, что нет универсального преобразования.)


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Можно сочетать преобразование «мир» с локальными преобразованиями для получения различных результатов. Например, можно использовать преобразование «мир» для изменения системы координат и использования локальных преобразований для вращения и масштабирования объектов, рисуемых в новой системе координат.

Предположим, что требуется система координат с координатами 200 пикселей от левого края клиентской области и 150 пикселей от верхней части клиентской области. Кроме того, предположим, что вы хотите, чтобы единица измерения была в пикселе, ось x указывала вправо, а ось y направлена вверх. В системе координат по умолчанию ось y направлена вниз, поэтому необходимо выполнить отражение по горизонтальной оси. На следующем рисунке показана матрица такого отражения.

![Иллюстрация, демонстрирующая матрицу "три-три"](images/aboutgdip05-art15.png)

Затем предположим, что вам нужно выполнить перевод единиц измерения 200 в правый и 150 единиц.

В следующем примере определяется система координат, только что описанная заданием универсального преобразования [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



Следующий код (помещается после кода в предыдущем примере) создает путь, состоящий из одного прямоугольника с нижним левым углом в источнике новой системы координат. Прямоугольник заполняется один раз без локального преобразования и один раз с локальным преобразованием. Локальное преобразование состоит из горизонтального масштабирования с коэффициентом 2, за которым следует поворот на 30 градусов.


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



На следующем рисунке показана новая система координат и два прямоугольника.

![снимок экрана оси x и y и синий квадрат, наложенный полупрозрачным ректаглем вокруг нижнего левого угла](images/aboutgdip05-art16.png)

 

 



