---
description: 'Службы Windows GDI+ делятся на следующие три основные категории:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Три части GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997458"
---
# <a name="the-three-parts-of-gdi"></a><span data-ttu-id="18aa0-103">Три части GDI+</span><span class="sxs-lookup"><span data-stu-id="18aa0-103">The Three Parts of GDI+</span></span>

<span data-ttu-id="18aa0-104">Службы Windows GDI+ делятся на следующие три основные категории:</span><span class="sxs-lookup"><span data-stu-id="18aa0-104">The services of Windows GDI+ fall into the following three broad categories:</span></span>

-   [<span data-ttu-id="18aa0-105">двумерная векторная графика</span><span class="sxs-lookup"><span data-stu-id="18aa0-105">2-D vector graphics</span></span>](#2-d-vector-graphics)
-   [<span data-ttu-id="18aa0-106">Создание образов</span><span class="sxs-lookup"><span data-stu-id="18aa0-106">Imaging</span></span>](#imaging)
-   [<span data-ttu-id="18aa0-107">Оформление текста</span><span class="sxs-lookup"><span data-stu-id="18aa0-107">Typography</span></span>](#typography)

## <a name="2-d-vector-graphics"></a><span data-ttu-id="18aa0-108">двумерная векторная графика</span><span class="sxs-lookup"><span data-stu-id="18aa0-108">2-D vector graphics</span></span>

<span data-ttu-id="18aa0-109">Векторная графика включает Рисование примитивов (таких как линии, кривые и цифры), которые задаются наборами точек в системе координат.</span><span class="sxs-lookup"><span data-stu-id="18aa0-109">Vector graphics involves drawing primitives (such as lines, curves, and figures) that are specified by sets of points on a coordinate system.</span></span> <span data-ttu-id="18aa0-110">Например, прямая линия может быть задана двумя конечными точками, а прямоугольник может быть задан точкой, указывающей расположение верхнего левого угла, и пару чисел, определяющих его ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="18aa0-110">For example, a straight line can be specified by its two endpoints, and a rectangle can be specified by a point giving the location of its upper-left corner and a pair of numbers giving its width and height.</span></span> <span data-ttu-id="18aa0-111">Простой путь может быть задан массивом точек, которые должны быть соединены прямыми линиями.</span><span class="sxs-lookup"><span data-stu-id="18aa0-111">A simple path can be specified by an array of points to be connected by straight lines.</span></span> <span data-ttu-id="18aa0-112">Сплайн Безье — это сложная кривая, определяемая четырьмя контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="18aa0-112">A Bézier spline is a sophisticated curve specified by four control points.</span></span>

<span data-ttu-id="18aa0-113">Интерфейс GDI+ предоставляет классы, в которых хранятся сведения о самих примитивах, классы, которые хранят сведения о том, как рисуются примитивы, и о классах, которые на самом деле выполняют рисование.</span><span class="sxs-lookup"><span data-stu-id="18aa0-113">GDI+ provides classes that store information about the primitives themselves, classes that store information about how the primitives are to be drawn, and classes that actually do the drawing.</span></span> <span data-ttu-id="18aa0-114">Например, класс **Rect** сохраняет расположение и размер прямоугольника. класс **Pen** сохраняет сведения о цвете линии, толщине линии и стиле линии. и класс **Graphics** содержит методы для рисования линий, прямоугольников, контуров и других фигур.</span><span class="sxs-lookup"><span data-stu-id="18aa0-114">For example, the **Rect** class stores the location and size of a rectangle; the **Pen** class stores information about line color, line width, and line style; and the **Graphics** class has methods for drawing lines, rectangles, paths, and other figures.</span></span> <span data-ttu-id="18aa0-115">Существует также несколько классов **кистей** , которые хранят сведения о том, как замкнутые фигуры и контуры заполняются цветами или шаблонами.</span><span class="sxs-lookup"><span data-stu-id="18aa0-115">There are also several **Brush** classes that store information about how closed figures and paths are to be filled with colors or patterns.</span></span>

## <a name="imaging"></a><span data-ttu-id="18aa0-116">Создание образов</span><span class="sxs-lookup"><span data-stu-id="18aa0-116">Imaging</span></span>

<span data-ttu-id="18aa0-117">Некоторые виды изображений сложно или невозможно отобразить с помощью методов векторной графики.</span><span class="sxs-lookup"><span data-stu-id="18aa0-117">Certain kinds of pictures are difficult or impossible to display with the techniques of vector graphics.</span></span> <span data-ttu-id="18aa0-118">Например, изображения на кнопках панели инструментов и изображения, отображаемые в виде значков, трудно указать как коллекции линий и кривых.</span><span class="sxs-lookup"><span data-stu-id="18aa0-118">For example, the pictures on toolbar buttons and the pictures that appear as icons would be difficult to specify as collections of lines and curves.</span></span> <span data-ttu-id="18aa0-119">Цифровая фотография стадионного бейсбольного мяча будет еще сложнее создавать с помощью векторных методов.</span><span class="sxs-lookup"><span data-stu-id="18aa0-119">A high-resolution digital photograph of a crowded baseball stadium would be even more difficult to create with vector techniques.</span></span> <span data-ttu-id="18aa0-120">Изображения этого типа хранятся в виде точечных рисунков, массивов чисел, представляющих цвета отдельных точек на экране.</span><span class="sxs-lookup"><span data-stu-id="18aa0-120">Images of this type are stored as bitmaps, arrays of numbers that represent the colors of individual dots on the screen.</span></span> <span data-ttu-id="18aa0-121">Структуры данных, в которых хранятся сведения о точечных рисунках, обычно сложнее, чем те, которые необходимы для векторной графики, поэтому для этой цели используется несколько классов в GDI+.</span><span class="sxs-lookup"><span data-stu-id="18aa0-121">Data structures that store information about bitmaps tend to be more complex than those required for vector graphics, so there are several classes in GDI+ devoted to this purpose.</span></span> <span data-ttu-id="18aa0-122">Примером такого класса является **качедбитмап**, который используется для хранения точечного рисунка в памяти для быстрого доступа и вывода.</span><span class="sxs-lookup"><span data-stu-id="18aa0-122">An example of such a class is **CachedBitmap**, which is used to store a bitmap in memory for fast access and display.</span></span>

## <a name="typography"></a><span data-ttu-id="18aa0-123">Шрифтовое оформление</span><span class="sxs-lookup"><span data-stu-id="18aa0-123">Typography</span></span>

<span data-ttu-id="18aa0-124">Типографская речь идет с отображением текста в различных шрифтах, размерах и стилях.</span><span class="sxs-lookup"><span data-stu-id="18aa0-124">Typography is concerned with the display of text in a variety of fonts, sizes, and styles.</span></span> <span data-ttu-id="18aa0-125">GDI+ обеспечивает впечатляющий объем поддержки для этой сложной задачи.</span><span class="sxs-lookup"><span data-stu-id="18aa0-125">GDI+ provides an impressive amount of support for this complex task.</span></span> <span data-ttu-id="18aa0-126">Одной из новых функций в GDI+ является сглаживание подточек, которое предоставляет текст, отображаемый на ЖК-экране, более гладкий внешний вид.</span><span class="sxs-lookup"><span data-stu-id="18aa0-126">One of the new features in GDI+ is subpixel antialiasing, which gives text rendered on an LCD screen a smoother appearance.</span></span>

 

 



