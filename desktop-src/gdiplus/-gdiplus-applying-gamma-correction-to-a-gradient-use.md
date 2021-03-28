---
description: 'Можно включить гамма-коррекцию для градиентной кисти, передав значение TRUE методу Пасградиентбруш:: Сетгаммакорректион этой кисти.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Применение гамма-коррекции к градиенту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156234"
---
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="0e4d3-103">Применение гамма-коррекции к градиенту</span><span class="sxs-lookup"><span data-stu-id="0e4d3-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="0e4d3-104">Можно включить гамма-коррекцию для градиентной кисти, передав **значение true** методу [**Пасградиентбруш:: сетгаммакорректион**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) этой кисти.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="0e4d3-105">Можно отключить гамма-коррекцию, передав **значение false** методу **Пасградиентбруш:: сетгаммакорректион** .</span><span class="sxs-lookup"><span data-stu-id="0e4d3-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="0e4d3-106">По умолчанию гамма-коррекция отключена.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="0e4d3-107">В следующем примере создается кисть линейного градиента и используется эта кисть для заливки двух прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="0e4d3-108">Первый прямоугольник заполняется без гамма-коррекции, а второй прямоугольник заполняется гаммой-коррекцией.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



<span data-ttu-id="0e4d3-109">На следующем рисунке показаны два закрашенных прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="0e4d3-110">Верхний прямоугольник, который не имеет гамма-коррекции, отображается темным в середине.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="0e4d3-111">Нижний прямоугольник, в котором имеется гамма-коррекция, имеет более однородную интенсивность.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![Иллюстрация, демонстрирующая два прямоугольника: цвет заливки первого цвета зависит от интенсивности, заливка второго — меньше](images/gammagradient1.png)

<span data-ttu-id="0e4d3-113">В следующем примере создается кисть градиента контура на основе траектории в форме звезды.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="0e4d3-114">Код использует кисть градиента вдоль пути с отключенной коррекцией гаммы (по умолчанию) для заполнения пути.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="0e4d3-115">Затем код передает **значение true** методу [**Пасградиентбруш:: сетгаммакорректион**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) , чтобы включить гамма-коррекцию для кисти градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="0e4d3-116">Вызов [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) устанавливает универсальное преобразование [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта таким образом, что последующий вызов [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет звезду, расположенную справа от первой звезды.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="0e4d3-117">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="0e4d3-118">Звездочка справа имеет гамма-коррекцию.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="0e4d3-119">Обратите внимание, что звездочка слева, не имеющая гамма-коррекции, содержит области, которые выглядят темными.</span><span class="sxs-lookup"><span data-stu-id="0e4d3-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![Иллюстрация 2 5, на которую указывает, начинается с цветной градиентной заливки; Первый имеет темные области, второй — нет.](images/gammagradient2.png)

 

 



