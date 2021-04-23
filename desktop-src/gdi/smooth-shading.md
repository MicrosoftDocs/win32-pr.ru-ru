---
description: Гладкая Заливка — это метод заливки области цветом градиента.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Плавная Заливка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265525"
---
# <a name="smooth-shading"></a><span data-ttu-id="9ef78-103">Плавная Заливка</span><span class="sxs-lookup"><span data-stu-id="9ef78-103">Smooth Shading</span></span>

<span data-ttu-id="9ef78-104">*Гладкая заливка* — это метод заливки области цветом градиента.</span><span class="sxs-lookup"><span data-stu-id="9ef78-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="9ef78-105">Включая сведения о цвете вместе с границами примитива рисования, указывает цветовой градиент.</span><span class="sxs-lookup"><span data-stu-id="9ef78-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="9ef78-106">GDI линейно интерполирует цвет внутри примитива, переданного в конечные точки цвета.</span><span class="sxs-lookup"><span data-stu-id="9ef78-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="9ef78-107">Сведения о цвете и вершине включаются в сведения о положении в структуре [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .</span><span class="sxs-lookup"><span data-stu-id="9ef78-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="9ef78-108">Используйте функцию [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) для заполнения структуры треугольника или прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9ef78-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="9ef78-109">Чтобы заполнить треугольник с помощью плавной заливки, вызовите **градиентфилл** с тремя конечными точками треугольника.</span><span class="sxs-lookup"><span data-stu-id="9ef78-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="9ef78-110">Чтобы заполнить прямоугольник с помощью плавной заливки, вызовите **градиентфилл** с координатами верхнего левого и нижнего правого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9ef78-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="9ef78-111">**Градиентфилл** ссылается на структуры [**тривертекс**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ прямоугольника градиента**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)и [**градиентного \_ треугольника**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .</span><span class="sxs-lookup"><span data-stu-id="9ef78-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="9ef78-112">Пример см. в разделе [Рисование затененного треугольника](drawing-a-shaded-triangle.md).</span><span class="sxs-lookup"><span data-stu-id="9ef78-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



