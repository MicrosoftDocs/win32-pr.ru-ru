---
description: Графическое состояние &\# 8212; отсеченная область, преобразования и параметры качества &\# 8212; хранятся в объекте Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Графические контейнеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558978"
---
# <a name="graphics-containers"></a>Графические контейнеры

Состояние графики — область обрезки, преобразования и параметры качества — хранятся в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Windows GDI+ позволяет временно заменить или дополнить часть состояния в объекте **Graphics** с помощью контейнера. Чтобы запустить контейнер, вызовите метод [**Graphics:: Бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) **графического** объекта, а затем завершите контейнер, вызвав метод [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) . В между **Graphics:: бегинконтаинер** и **Graphics:: ендконтаинер** любые изменения состояния, вносимые в объект **Graphics** , принадлежат контейнеру и не перезаписывают существующее состояние объекта **Graphics** .

В следующем примере создается контейнер в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Мировое преобразование **графического** объекта — это преобразование единиц измерения 200 справа, а объемное преобразование контейнера — это перевод на 100 единиц вниз.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Обратите внимание, что в предыдущем примере инструкция, `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` выполненная между вызовами [**Graphics:: Бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , создает другой прямоугольник, отличный от того же оператора, сделанного после вызова **Graphics:: ендконтаинер**. Только горизонтальное преобразование применяется к вызову **DrawRectangle** , сделанному за пределами контейнера. Оба преобразования — горизонтальный перевод 200 единиц и вертикального перевода 100 единиц — применяются к [**графическому элементу::D вызов равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) в контейнере. На следующем рисунке показаны два прямоугольника.

![снимок экрана: окно с двумя прямоугольниками, нарисованными с помощью синего пера, одно расположение над другим](images/aboutgdip05-art17.png)

Контейнеры могут быть вложены в контейнеры. В следующем примере создается контейнер внутри [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта и другой контейнер в первом контейнере. Мировым преобразованием **графического** объекта является преобразование единиц измерения 100 в направлении x и 80 единиц по оси y. Преобразование «мир» первого контейнера — это поворот на 30 градусов. Универсальное преобразование второго контейнера — это масштабирование с коэффициентом 2 в направлении x. Вызов метода [**Graphics::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) выполняется внутри второго контейнера.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



На следующем рисунке показан эллипс.

![снимок экрана: окно, содержащее повернутый синий эллипс со своим центром с меткой (100, 80)](images/aboutgdip05-art18.png)

Обратите внимание, что все три преобразования применяются к [**графике::D вызов равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) , сделанный во втором (внутреннем) контейнере. Также обратите внимание на порядок преобразований: сначала масштабирование, затем поворот, затем преобразование. Сначала применяется внутреннее преобразование, а внешнее преобразование применяется последним.

Любое свойство [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта может быть задано внутри контейнера (между вызовами [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). Например, область обрезки может быть задана внутри контейнера. Любая прорисовка, выполненная внутри контейнера, будет ограничена областью обрезки этого контейнера и будет ограничена областями отсечения всех внешних контейнеров и вырезанной области самого объекта **Graphics** .

Свойства, обсуждаемые до сих пор, — универсальное преобразование и отсеченная область — объединяются вложенными контейнерами. Другие свойства временно заменяются вложенным контейнером. Например, если задать режим сглаживания Смусингмодеантиалиас в контейнере, то все методы рисования, вызываемые внутри этого контейнера, будут использовать режим сглаживания без сглаживания, но методы рисования, вызываемые после [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , будут использовать режим сглаживания, который находился перед вызовом [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Еще один пример объединения мировых преобразований [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта и контейнера, предположим, вы хотите нарисовать глаз и поместить его в различные места в последовательности лиц. В следующем примере глаз переводится в начало координат системы координат.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



На следующем рисунке показан глаз и оси координат.

![Иллюстрация, на которой показан глаз, состоящий из трех эллипсов: по одному для структуры, IRI и пупил](images/aboutgdip05-art19.png)

Функция Дравэйе, определенная в предыдущем примере, получает адрес объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и сразу же создает контейнер внутри этого объекта **Graphics** . Этот контейнер изолирует любой код, который вызывает функцию Дравэйе, из параметров свойства, сделанных во время выполнения функции Дравэйе. Например, код в функции Дравэйе задает область обрезки объекта **Graphics** , но когда дравэйе возвращает управление вызывающей подпрограмме, область обрезки будет совпадать с той, что была до вызова дравэйе.

В следующем примере рисуются три эллипса (Face), в каждом из которых находится глаз.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



На следующем рисунке показаны три эллипса.

![снимок экрана: окно с тремя эллипсами, каждое из которых содержит глаз с другим размером и поворотом](images/aboutgdip05-art20.png)

В предыдущем примере все эллипсы рисуются с помощью вызова `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , который рисует эллипс по центру в источнике системы координат. Эллипсы перемещаются с левого верхнего угла клиентской области путем задания универсального преобразования [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта. Оператор приводит к центрированию первого эллипса в (100, 100). Оператор приводит к тому, что центр второго эллипса будет 100 единиц справа от центра первого эллипса. Точно так же центр третьего эллипса находится в 100 единиц справа от центра второго эллипса.

Контейнеры в предыдущем примере используются для преобразования глаза относительно центра данного эллипса. Первый взгляд рисуется в центре эллипса без преобразования, поэтому вызов Дравэйе не находится внутри контейнера. Второй глаз поворачивается в 40 градусов и выводит 30 единиц в центре эллипса, поэтому функция Дравэйе и методы, которые задают преобразование, вызываются внутри контейнера. Третий взгляд растягивается и поворачивается и рисуется в центре эллипса. Как и во втором глазе, функция Дравэйе и методы, которые задают преобразование, вызываются внутри контейнера.

 

 
