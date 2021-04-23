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
# <a name="graphics-containers"></a><span data-ttu-id="d3c5c-103">Графические контейнеры</span><span class="sxs-lookup"><span data-stu-id="d3c5c-103">Graphics Containers</span></span>

<span data-ttu-id="d3c5c-104">Состояние графики — область обрезки, преобразования и параметры качества — хранятся в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d3c5c-105">Windows GDI+ позволяет временно заменить или дополнить часть состояния в объекте **Graphics** с помощью контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="d3c5c-106">Чтобы запустить контейнер, вызовите метод [**Graphics:: Бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) **графического** объекта, а затем завершите контейнер, вызвав метод [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="d3c5c-107">В между **Graphics:: бегинконтаинер** и **Graphics:: ендконтаинер** любые изменения состояния, вносимые в объект **Graphics** , принадлежат контейнеру и не перезаписывают существующее состояние объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="d3c5c-108">В следующем примере создается контейнер в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d3c5c-109">Мировое преобразование **графического** объекта — это преобразование единиц измерения 200 справа, а объемное преобразование контейнера — это перевод на 100 единиц вниз.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="d3c5c-110">Обратите внимание, что в предыдущем примере инструкция, `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` выполненная между вызовами [**Graphics:: Бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , создает другой прямоугольник, отличный от того же оператора, сделанного после вызова **Graphics:: ендконтаинер**.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="d3c5c-111">Только горизонтальное преобразование применяется к вызову **DrawRectangle** , сделанному за пределами контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="d3c5c-112">Оба преобразования — горизонтальный перевод 200 единиц и вертикального перевода 100 единиц — применяются к [**графическому элементу::D вызов равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) в контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="d3c5c-113">На следующем рисунке показаны два прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-113">The following illustration shows the two rectangles.</span></span>

![снимок экрана: окно с двумя прямоугольниками, нарисованными с помощью синего пера, одно расположение над другим](images/aboutgdip05-art17.png)

<span data-ttu-id="d3c5c-115">Контейнеры могут быть вложены в контейнеры.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-115">Containers can be nested within containers.</span></span> <span data-ttu-id="d3c5c-116">В следующем примере создается контейнер внутри [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта и другой контейнер в первом контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="d3c5c-117">Мировым преобразованием **графического** объекта является преобразование единиц измерения 100 в направлении x и 80 единиц по оси y.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="d3c5c-118">Преобразование «мир» первого контейнера — это поворот на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="d3c5c-119">Универсальное преобразование второго контейнера — это масштабирование с коэффициентом 2 в направлении x.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="d3c5c-120">Вызов метода [**Graphics::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) выполняется внутри второго контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


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



<span data-ttu-id="d3c5c-121">На следующем рисунке показан эллипс.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-121">The following illustration shows the ellipse.</span></span>

![снимок экрана: окно, содержащее повернутый синий эллипс со своим центром с меткой (100, 80)](images/aboutgdip05-art18.png)

<span data-ttu-id="d3c5c-123">Обратите внимание, что все три преобразования применяются к [**графике::D вызов равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) , сделанный во втором (внутреннем) контейнере.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="d3c5c-124">Также обратите внимание на порядок преобразований: сначала масштабирование, затем поворот, затем преобразование.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="d3c5c-125">Сначала применяется внутреннее преобразование, а внешнее преобразование применяется последним.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="d3c5c-126">Любое свойство [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта может быть задано внутри контейнера (между вызовами [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="d3c5c-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="d3c5c-127">Например, область обрезки может быть задана внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="d3c5c-128">Любая прорисовка, выполненная внутри контейнера, будет ограничена областью обрезки этого контейнера и будет ограничена областями отсечения всех внешних контейнеров и вырезанной области самого объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="d3c5c-129">Свойства, обсуждаемые до сих пор, — универсальное преобразование и отсеченная область — объединяются вложенными контейнерами.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="d3c5c-130">Другие свойства временно заменяются вложенным контейнером.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="d3c5c-131">Например, если задать режим сглаживания Смусингмодеантиалиас в контейнере, то все методы рисования, вызываемые внутри этого контейнера, будут использовать режим сглаживания без сглаживания, но методы рисования, вызываемые после [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , будут использовать режим сглаживания, который находился перед вызовом [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="d3c5c-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="d3c5c-132">Еще один пример объединения мировых преобразований [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта и контейнера, предположим, вы хотите нарисовать глаз и поместить его в различные места в последовательности лиц.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="d3c5c-133">В следующем примере глаз переводится в начало координат системы координат.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


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



<span data-ttu-id="d3c5c-134">На следующем рисунке показан глаз и оси координат.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-134">The following illustration shows the eye and the coordinate axes.</span></span>

![Иллюстрация, на которой показан глаз, состоящий из трех эллипсов: по одному для структуры, IRI и пупил](images/aboutgdip05-art19.png)

<span data-ttu-id="d3c5c-136">Функция Дравэйе, определенная в предыдущем примере, получает адрес объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и сразу же создает контейнер внутри этого объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="d3c5c-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="d3c5c-137">Этот контейнер изолирует любой код, который вызывает функцию Дравэйе, из параметров свойства, сделанных во время выполнения функции Дравэйе.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="d3c5c-138">Например, код в функции Дравэйе задает область обрезки объекта **Graphics** , но когда дравэйе возвращает управление вызывающей подпрограмме, область обрезки будет совпадать с той, что была до вызова дравэйе.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="d3c5c-139">В следующем примере рисуются три эллипса (Face), в каждом из которых находится глаз.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


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



<span data-ttu-id="d3c5c-140">На следующем рисунке показаны три эллипса.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-140">The following illustration shows the three ellipses.</span></span>

![снимок экрана: окно с тремя эллипсами, каждое из которых содержит глаз с другим размером и поворотом](images/aboutgdip05-art20.png)

<span data-ttu-id="d3c5c-142">В предыдущем примере все эллипсы рисуются с помощью вызова `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , который рисует эллипс по центру в источнике системы координат.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="d3c5c-143">Эллипсы перемещаются с левого верхнего угла клиентской области путем задания универсального преобразования [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="d3c5c-144">Оператор приводит к центрированию первого эллипса в (100, 100).</span><span class="sxs-lookup"><span data-stu-id="d3c5c-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="d3c5c-145">Оператор приводит к тому, что центр второго эллипса будет 100 единиц справа от центра первого эллипса.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="d3c5c-146">Точно так же центр третьего эллипса находится в 100 единиц справа от центра второго эллипса.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="d3c5c-147">Контейнеры в предыдущем примере используются для преобразования глаза относительно центра данного эллипса.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="d3c5c-148">Первый взгляд рисуется в центре эллипса без преобразования, поэтому вызов Дравэйе не находится внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="d3c5c-149">Второй глаз поворачивается в 40 градусов и выводит 30 единиц в центре эллипса, поэтому функция Дравэйе и методы, которые задают преобразование, вызываются внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="d3c5c-150">Третий взгляд растягивается и поворачивается и рисуется в центре эллипса.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="d3c5c-151">Как и во втором глазе, функция Дравэйе и методы, которые задают преобразование, вызываются внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
