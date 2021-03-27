---
description: 'Шаблон штриховки состоит из двух цветов: один для фона, а другой для линий, образующих шаблон на фоне.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Заполнение фигуры шаблоном штриховки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987912"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="5f0c1-103">Заполнение фигуры шаблоном штриховки</span><span class="sxs-lookup"><span data-stu-id="5f0c1-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="5f0c1-104">Шаблон штриховки состоит из двух цветов: один для фона, а другой для линий, образующих шаблон на фоне.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="5f0c1-105">Для заполнения замкнутой фигуры шаблоном штриховки используйте объект [**хатчбруш**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="5f0c1-106">В следующем примере показано, как заполнить эллипс с помощью шаблона штриховки:</span><span class="sxs-lookup"><span data-stu-id="5f0c1-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="5f0c1-107">На следующем рисунке показан закрашенный эллипс.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-107">The following illustration shows the filled ellipse.</span></span>

![Иллюстрация эллипса, заполненного шаблоном штриховки горизонтальных линий в сплошном фоне](images/hatch1.png)

<span data-ttu-id="5f0c1-109">Конструктор [**хатчбруш**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) принимает три аргумента: стиль штриховки, цвет линии штриховки и цвет фона.</span><span class="sxs-lookup"><span data-stu-id="5f0c1-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="5f0c1-110">Аргумент стиля штриховки может быть любым элементом перечисления [**хатчстиле**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) .</span><span class="sxs-lookup"><span data-stu-id="5f0c1-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="5f0c1-111">В перечислении **хатчстиле** более 50 элементов; Некоторые из этих элементов показаны в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="5f0c1-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="5f0c1-112">**хатчстилехоризонтал**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="5f0c1-113">**хатчстилевертикал**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="5f0c1-114">**хатчстилефорварддиагонал**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="5f0c1-115">**хатчстилебаккварддиагонал**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="5f0c1-116">**хатчстилекросс**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="5f0c1-117">**хатчстиледиагоналкросс**</span><span class="sxs-lookup"><span data-stu-id="5f0c1-117">**HatchStyleDiagonalCross**</span></span>

 

 



