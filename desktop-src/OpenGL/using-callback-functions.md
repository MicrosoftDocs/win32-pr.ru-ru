---
title: Использование функций обратного вызова
description: Функции обратного вызова GLU, Глубегинполигон, Глутессвертекс, Глунекстконтаур и Глуендполигон, похожи на функции многоугольников OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Служебная программа OpenGL (GLU), функции обратного вызова
- GLU (служебная программа OpenGL), функции обратного вызова
- Служебная программа OpenGL (GLU), тесселяция
- GLU (служебная программа OpenGL), тесселяция
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888055"
---
# <a name="using-callback-functions"></a><span data-ttu-id="952aa-107">Использование функций обратного вызова</span><span class="sxs-lookup"><span data-stu-id="952aa-107">Using Callback Functions</span></span>

<span data-ttu-id="952aa-108">Функции обратного вызова GLU, [**глубегинполигон**](glubeginpolygon.md), [**глутессвертекс**](glutessvertex.md), [**глунекстконтаур**](glunextcontour.md)и [**Глуендполигон**](gluendpolygon.md), похожи на функции многоугольников OpenGL.</span><span class="sxs-lookup"><span data-stu-id="952aa-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="952aa-109">Обычно они сохраняют данные для треугольников, сеток треугольников и вентиляторов треугольников в пользовательских структурах данных или в списках дисплеей OpenGL.</span><span class="sxs-lookup"><span data-stu-id="952aa-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="952aa-110">Для отрисовки многоугольников другой код проходит по структурам данных или вызывает списки отображения.</span><span class="sxs-lookup"><span data-stu-id="952aa-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="952aa-111">Несмотря на то, что функции обратного вызова могут вызывать функции OpenGL для непосредственного показа многоугольников, обычно это не выполняется, так как тесселяция может представлять собой ресурсоемкие вычислительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="952aa-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="952aa-112">Рекомендуется сохранить данные, если есть вероятность, что она будет отображаться снова.</span><span class="sxs-lookup"><span data-stu-id="952aa-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="952aa-113">Функции тесселяции GLU гарантированно не возвращают новые вершины, поэтому не требуется интерполяция вершин, координат текстуры или цвета.</span><span class="sxs-lookup"><span data-stu-id="952aa-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 




