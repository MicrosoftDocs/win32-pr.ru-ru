---
description: Приложение должно использовать структуру RECT для определения прямоугольника.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Координаты прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997318"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="e3e64-103">Координаты прямоугольника</span><span class="sxs-lookup"><span data-stu-id="e3e64-103">Rectangle Coordinates</span></span>

<span data-ttu-id="e3e64-104">Приложение должно использовать структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) для определения прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e3e64-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="e3e64-105">Структура задает координаты двух точек: верхнего левого и нижнего правого угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e3e64-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="e3e64-106">Стороны прямоугольника расширяются из этих двух точек и параллельны с осью x и осью y.</span><span class="sxs-lookup"><span data-stu-id="e3e64-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="e3e64-107">Значения координат для прямоугольника выражаются как целые числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="e3e64-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="e3e64-108">Значение координаты правой стороны прямоугольника должно быть больше, чем у левой стороны.</span><span class="sxs-lookup"><span data-stu-id="e3e64-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="e3e64-109">Аналогично, значение координаты нижнего значения должно быть больше верхнего.</span><span class="sxs-lookup"><span data-stu-id="e3e64-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="e3e64-110">Так как приложения могут использовать прямоугольники для различных целей, функции Rectangle не используют явную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="e3e64-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="e3e64-111">Вместо этого все координаты прямоугольника и измерения задаются в виде логических значений со знаком.</span><span class="sxs-lookup"><span data-stu-id="e3e64-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="e3e64-112">Режим сопоставления и функция, в которых используется прямоугольник, определяют единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="e3e64-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="e3e64-113">Дополнительные сведения о координатах и режимах сопоставления см. в разделе [координатные пространства и преобразования](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="e3e64-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
