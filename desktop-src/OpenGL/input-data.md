---
title: Входные данные
description: Для конвейера OpenGL требуется ввод нескольких типов данных.
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Конвейер обработки OpenGL, входные данные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661535"
---
# <a name="input-data"></a><span data-ttu-id="679ad-104">Входные данные</span><span class="sxs-lookup"><span data-stu-id="679ad-104">Input Data</span></span>

<span data-ttu-id="679ad-105">Для конвейера OpenGL требуется ввод нескольких типов данных:</span><span class="sxs-lookup"><span data-stu-id="679ad-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="679ad-106">**Вершины**.</span><span class="sxs-lookup"><span data-stu-id="679ad-106">**Vertices**.</span></span> <span data-ttu-id="679ad-107">Вершины описывают форму нужного геометрического объекта.</span><span class="sxs-lookup"><span data-stu-id="679ad-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="679ad-108">Чтобы задать вершины, используйте [**функции \* глвертекс**](glvertex-functions.md) в сочетании с [**глбегин**](glbegin.md) и [**гленд**](glend.md) для создания точки, линии или многоугольника.</span><span class="sxs-lookup"><span data-stu-id="679ad-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="679ad-109">Можно также использовать [**глрект**](glrect-functions.md) для описания всего прямоугольника за один раз.</span><span class="sxs-lookup"><span data-stu-id="679ad-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="679ad-110">**Флаг границы**.</span><span class="sxs-lookup"><span data-stu-id="679ad-110">**Edge flag**.</span></span> <span data-ttu-id="679ad-111">По умолчанию все грани многоугольников являются границами границ.</span><span class="sxs-lookup"><span data-stu-id="679ad-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="679ad-112">Используйте [**гледжефлаг \***](gledgeflag-functions.md) , чтобы явно задать флаг границы.</span><span class="sxs-lookup"><span data-stu-id="679ad-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="679ad-113">**Текущая растровая размещается**.</span><span class="sxs-lookup"><span data-stu-id="679ad-113">**Current raster position**.</span></span> <span data-ttu-id="679ad-114">В соответствии [**с \* глрастерпос**](glrasterpos-functions.md), текущая битовая точка используется для определения растровых координат для операций рисования пикселей и точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="679ad-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="679ad-115">**Текущее нормальное состояние**.</span><span class="sxs-lookup"><span data-stu-id="679ad-115">**Current normal**.</span></span> <span data-ttu-id="679ad-116">Обычная векторная связь, связанная с определенной вершиной, определяет, как поверхность на этой вершине ориентирована в трехмерном пространстве. Это, в свою очередь, влияет на то, насколько интенсивно получится конкретная вершина.</span><span class="sxs-lookup"><span data-stu-id="679ad-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="679ad-117">Используйте [**глнормал \***](glnormal-functions.md) для указания обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="679ad-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="679ad-118">**Текущий цвет**.</span><span class="sxs-lookup"><span data-stu-id="679ad-118">**Current color**.</span></span> <span data-ttu-id="679ad-119">Цвет вершины, а также условия освещения определяют окончательный, освещенный цвет.</span><span class="sxs-lookup"><span data-stu-id="679ad-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="679ad-120">Цвет задается с помощью [**глколор \***](glcolor-functions.md) в режиме RGBA или с [**глиндекс \***](glindex-functions.md) в режиме индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="679ad-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="679ad-121">**Текущие координаты текстуры**.</span><span class="sxs-lookup"><span data-stu-id="679ad-121">**Current texture coordinates**.</span></span> <span data-ttu-id="679ad-122">Координаты текстуры, заданные с помощью [**глтекскурд \***](gltexcoord-functions.md), определяют расположение в текстурной карте для связи с вершиной объекта.</span><span class="sxs-lookup"><span data-stu-id="679ad-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="679ad-123">При вызове **глвертекс \*** результирующая вершина наследует текущий флаг границы, нормальную, цветовую и текстурную координаты.</span><span class="sxs-lookup"><span data-stu-id="679ad-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="679ad-124">Поэтому **гледжефлаг \***, **глнормал \***, **глколор \*** и **\* глтекскурд** должны вызываться до **глвертекс \***, если они повлияют на результирующую вершину.</span><span class="sxs-lookup"><span data-stu-id="679ad-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 




