---
description: Windows GDI+ предоставляет контейнеры, которые можно использовать для временного замены или дополнения части состояния в объекте Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Вложенные графические контейнеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991637"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="b52c0-103">Вложенные графические контейнеры</span><span class="sxs-lookup"><span data-stu-id="b52c0-103">Nested Graphics Containers</span></span>

<span data-ttu-id="b52c0-104">Windows GDI+ предоставляет контейнеры, которые можно использовать для временного замены или дополнения части состояния в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b52c0-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="b52c0-105">Контейнер создается путем вызова метода [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b52c0-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="b52c0-106">Для формирования вложенных контейнеров можно многократно вызывать **Graphics:: бегинконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="b52c0-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="b52c0-107">Преобразования во вложенных контейнерах</span><span class="sxs-lookup"><span data-stu-id="b52c0-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="b52c0-108">В следующем примере создается [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и контейнер внутри этого объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b52c0-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="b52c0-109">Мировым преобразованием **графического** объекта является преобразование единиц измерения 100 в направлении x и 80 единиц по оси y.</span><span class="sxs-lookup"><span data-stu-id="b52c0-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="b52c0-110">Универсальное преобразование контейнера — это поворот на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="b52c0-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="b52c0-111">Код вызывает</span><span class="sxs-lookup"><span data-stu-id="b52c0-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="b52c0-112">Дважды.</span><span class="sxs-lookup"><span data-stu-id="b52c0-112">twice.</span></span> <span data-ttu-id="b52c0-113">Первый вызов [**Graphics::D равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) находится *внутри контейнера*; Это значит, что вызов осуществляется между вызовами [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) и [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="b52c0-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="b52c0-114">Второй вызов **Graphics::D равректангле** — после вызова **Graphics:: ендконтаинер**.</span><span class="sxs-lookup"><span data-stu-id="b52c0-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


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



<span data-ttu-id="b52c0-115">В приведенном выше коде прямоугольник, рисуемый внутри контейнера, преобразуется сначала по всему миру контейнера (вращение), а затем по всему миру [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта (перевод).</span><span class="sxs-lookup"><span data-stu-id="b52c0-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="b52c0-116">Прямоугольник, рисуемый за пределами контейнера, преобразуется только в мировом преобразовании объекта **Graphics** (перевод).</span><span class="sxs-lookup"><span data-stu-id="b52c0-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="b52c0-117">На следующем рисунке показаны два прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b52c0-117">The following illustration shows the two rectangles.</span></span>

![снимок экрана: окно с двумя красными прямоугольниками в центре одной и той же точки, но с разными поворотами](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="b52c0-119">Обрезка во вложенных контейнерах</span><span class="sxs-lookup"><span data-stu-id="b52c0-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="b52c0-120">В следующем примере показано, как вложенные контейнеры обработают области отсечения.</span><span class="sxs-lookup"><span data-stu-id="b52c0-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="b52c0-121">Код создает [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и контейнер внутри этого **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="b52c0-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="b52c0-122">Вырезанная область объекта **Graphics** является прямоугольником, а область обрезки контейнера — эллипсом.</span><span class="sxs-lookup"><span data-stu-id="b52c0-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="b52c0-123">Код выполняет два вызова метода [**Graphics::D равлине**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="b52c0-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="b52c0-124">Первый вызов **Graphics::D равлине** находится внутри контейнера, а второй вызов **Graphics::D равлине** находится за пределами контейнера (после вызова [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="b52c0-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="b52c0-125">Первая строка обрезается по пересечению двух областей отсечения.</span><span class="sxs-lookup"><span data-stu-id="b52c0-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="b52c0-126">Вторая строка обрезается только прямоугольной вырезанной областью объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b52c0-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


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



<span data-ttu-id="b52c0-127">На следующем рисунке показаны две обрезанные линии.</span><span class="sxs-lookup"><span data-stu-id="b52c0-127">The following illustration shows the two clipped lines.</span></span>

![Иллюстрация эллипса внутри прямоугольника с одной линией, обрезанной с помощью эллипса, а другой — прямоугольником](images/nestedcontainers2.png)

<span data-ttu-id="b52c0-129">Как показано в двух предыдущих примерах, преобразования и области обрезки являются кумулятивными в вложенных контейнерах.</span><span class="sxs-lookup"><span data-stu-id="b52c0-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="b52c0-130">Если задать мировые преобразования контейнера и объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , то оба преобразования будут применяться к элементам, рисуемым внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="b52c0-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="b52c0-131">Преобразование контейнера будет применено первыми, а преобразование объекта **Graphics** будет применено ко второму.</span><span class="sxs-lookup"><span data-stu-id="b52c0-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="b52c0-132">Если задать области обрезки контейнера и объекта **Graphics** , то элементы, рисуемые внутри контейнера, будут обрезаны пересечением двух областей отсечения.</span><span class="sxs-lookup"><span data-stu-id="b52c0-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="b52c0-133">Параметры качества во вложенных контейнерах</span><span class="sxs-lookup"><span data-stu-id="b52c0-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="b52c0-134">Параметры качества ( [**смусингмоде**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**текстрендерингхинт**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)и Like) во вложенных контейнерах не являются накопительными. Вместо этого параметры качества контейнера временно заменяют параметры качества объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b52c0-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="b52c0-135">При создании нового контейнера параметры качества для этого контейнера задаются как значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b52c0-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="b52c0-136">Например, предположим, что у вас есть **графический** объект с режимом сглаживания [\* \* \* \* смусингмодеантиалиас \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \* \*.</span><span class="sxs-lookup"><span data-stu-id="b52c0-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="b52c0-137">При создании контейнера режим сглаживания в контейнере является режимом сглаживания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b52c0-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="b52c0-138">Вы можете задать режим сглаживания контейнера, и все элементы, отображаемые в контейнере, будут отображаться в соответствии с заданным режимом.</span><span class="sxs-lookup"><span data-stu-id="b52c0-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="b52c0-139">Элементы, рисуемые после вызова [**Graphics:: ендконтаинер**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) , будут отображаться в соответствии с режимом сглаживания ([\* \* \* \* смусингмодеантиалиас \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \* \*), который находился перед вызовом [**Graphics:: бегинконтаинер**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="b52c0-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="b52c0-140">Несколько уровней вложенных контейнеров</span><span class="sxs-lookup"><span data-stu-id="b52c0-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="b52c0-141">Вы не ограничены одним контейнером в объекте [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b52c0-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="b52c0-142">Можно создать последовательность контейнеров, каждый из которых вложен в предыдущий, а также указать объемное преобразование, область отсечения и параметры качества для каждого из этих вложенных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b52c0-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="b52c0-143">Если вызвать метод рисования из самого внутреннего контейнера, то преобразования будут применены по порядку, начиная с самого внутреннего контейнера и заканчивая самым внешним контейнером.</span><span class="sxs-lookup"><span data-stu-id="b52c0-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="b52c0-144">Элементы, отображаемые внутри самого внутреннего контейнера, обрезаются пересечением всех областей обрезки.</span><span class="sxs-lookup"><span data-stu-id="b52c0-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="b52c0-145">В следующем примере создается объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и задается его подсказка для отрисовки текста [\* \* \* \* текстрендерингхинтантиалиас \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*.</span><span class="sxs-lookup"><span data-stu-id="b52c0-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="b52c0-146">Код создает два контейнера, один из которых вложен в другой.</span><span class="sxs-lookup"><span data-stu-id="b52c0-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="b52c0-147">Подсказка визуализации текста внешнего контейнера имеет значение [\* \* \* \* текстрендерингхинтсинглебитперпиксел \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* *, а подсказка для отображения текста внутреннего контейнера имеет значение [\* \* \* \* текстрендерингхинтантиалиас \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* \*.</span><span class="sxs-lookup"><span data-stu-id="b52c0-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="b52c0-148">Код рисует три строки: один из внутреннего контейнера, один из внешнего контейнера, а другой — из самого объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b52c0-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


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



<span data-ttu-id="b52c0-149">На следующем рисунке показаны три строки.</span><span class="sxs-lookup"><span data-stu-id="b52c0-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="b52c0-150">Строки, нарисованные из внутреннего контейнера и объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , сглажены с помощью сглаживания.</span><span class="sxs-lookup"><span data-stu-id="b52c0-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="b52c0-151">Строка, выведенная из внешнего контейнера, не сглажена с помощью сглаживания из-за параметра Текстрендерингхинтсинглебитперпиксел.</span><span class="sxs-lookup"><span data-stu-id="b52c0-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![Иллюстрация прямоугольника, содержащего одну и ту же строку. только символы в первой и последней строках являются гладкими](images/nestedcontainers3.png)

 

 
