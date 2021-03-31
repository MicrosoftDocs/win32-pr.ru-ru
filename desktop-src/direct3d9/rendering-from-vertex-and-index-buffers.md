---
description: Direct3D поддерживает как индексированные, так и неиндексированные методы рисования.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Отрисовка из буферов вершин и индексов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894313"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="d7eea-103">Отрисовка из буферов вершин и индексов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d7eea-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="d7eea-104">Direct3D поддерживает как индексированные, так и неиндексированные методы рисования.</span><span class="sxs-lookup"><span data-stu-id="d7eea-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="d7eea-105">Индексированные методы используют один набор индексов для всех компонентов вершины.</span><span class="sxs-lookup"><span data-stu-id="d7eea-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="d7eea-106">Данные вершин хранятся в буферах вершин, а индексные данные хранятся в буферах индексов.</span><span class="sxs-lookup"><span data-stu-id="d7eea-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="d7eea-107">Ниже приведено несколько распространенных сценариев рисования примитивов с использованием буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="d7eea-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="d7eea-108">Эти примеры сравнивают использование [**IDirect3DDevice9::D равпримитиве**](/windows/desktop/api) и [**IDirect3DDevice9::D равиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="d7eea-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="d7eea-109">Сценарий 1. Рисование двух треугольников без индексирования</span><span class="sxs-lookup"><span data-stu-id="d7eea-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="d7eea-110">Предположим, что вы хотите нарисовать Quad, показанный на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d7eea-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![Иллюстрация квадрата, состоящего из двух треугольников](images/dip-fig1.png)

<span data-ttu-id="d7eea-112">Если для отрисовки двух треугольников используется тип-примитив список треугольников, каждый треугольник будет храниться в виде трех отдельных вершин, в результате чего аналогичный буфер вершин появится на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d7eea-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![схема буфера вершин, определяющая три вершины для двух треугольников](images/dip-fig2.png)

<span data-ttu-id="d7eea-114">Вызов рисования очень прост; начиная с позиции 0 в буфере вершин Нарисуйте два треугольника.</span><span class="sxs-lookup"><span data-stu-id="d7eea-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="d7eea-115">Если отбор включен, то порядок вершин будет важен.</span><span class="sxs-lookup"><span data-stu-id="d7eea-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="d7eea-116">В этом примере предполагается, что состояние исключается по часовой стрелке по умолчанию, поэтому видимые треугольники должны отображаться в порядке по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="d7eea-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="d7eea-117">Тип-примитив списка треугольников просто считывает три вершины в линейном порядке из буфера для каждого треугольника, поэтому этот вызов будет рисовать треугольники (0, 1, 2) и (3, 4, 5):</span><span class="sxs-lookup"><span data-stu-id="d7eea-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="d7eea-118">Сценарий 2. Рисование двух треугольников с помощью индексирования</span><span class="sxs-lookup"><span data-stu-id="d7eea-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="d7eea-119">Как вы заметите, буфер вершин содержит дублирующиеся данные в расположениях 0 и 4, 2 и 5.</span><span class="sxs-lookup"><span data-stu-id="d7eea-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="d7eea-120">Это имеет смысл, поскольку два треугольника совместно используют две общие вершины.</span><span class="sxs-lookup"><span data-stu-id="d7eea-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="d7eea-121">Эти дублирующиеся данные непроизводительна, а буфер вершин можно сжать с помощью буфера индексов.</span><span class="sxs-lookup"><span data-stu-id="d7eea-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="d7eea-122">Буфер вершин меньшего размера сокращает объем данных вершин, которые должны быть отправлены на графический адаптер.</span><span class="sxs-lookup"><span data-stu-id="d7eea-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="d7eea-123">Что еще более важно, использование буфера индексов позволяет адаптеру хранить вершины в кэше вершин. Если рисуемый примитив содержит недавно использовавшуюся вершину, эту вершину можно извлечь из кэша, а не считывать из буфера вершин, что приводит к значительному увеличению производительности.</span><span class="sxs-lookup"><span data-stu-id="d7eea-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="d7eea-124">Индексный буфер индексируется в буфере вершин, поэтому каждая уникальная вершина должна храниться в буфере вершин только один раз.</span><span class="sxs-lookup"><span data-stu-id="d7eea-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="d7eea-125">На следующей схеме показан индексированный подход к предыдущему сценарию рисования.</span><span class="sxs-lookup"><span data-stu-id="d7eea-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![схема буфера индекса для предыдущего буфера вершин](images/dip-fig3.png)

<span data-ttu-id="d7eea-127">В буфере индекса хранятся значения индекса VB, которые ссылаются на определенную вершину в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="d7eea-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="d7eea-128">Буфер вершин можно рассматривать как массив вершин, поэтому индекс VB — это просто индекс в буфере вершин для целевой вершины.</span><span class="sxs-lookup"><span data-stu-id="d7eea-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="d7eea-129">Точно так же, индекс в индексе является индексом в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="d7eea-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="d7eea-130">Это может очень быстро обойтись, если не соблюдать осторожность, поэтому убедитесь, что вы знаете, какой словарь используется: индекс значений VB в буфере вершин, индекс значений индекса в буфере, а также буфер индексов, в котором хранятся значения индекса VB.</span><span class="sxs-lookup"><span data-stu-id="d7eea-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="d7eea-131">Вызов рисования показан ниже.</span><span class="sxs-lookup"><span data-stu-id="d7eea-131">The drawing call is shown below.</span></span> <span data-ttu-id="d7eea-132">Значения всех аргументов обсуждаются по длине для следующего сценария рисования. Теперь просто обратите внимание, что этот вызов снова указывает Direct3D отобразить список треугольников, содержащий два треугольника, начиная с позиции 0 в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="d7eea-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="d7eea-133">Этот вызов выполнит рисование тех же двух треугольников в том же порядке, что и раньше, обеспечивая правильную ориентацию по часовой стрелке:</span><span class="sxs-lookup"><span data-stu-id="d7eea-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="d7eea-134">Сценарий 3. Рисование одного треугольника с помощью индексирования</span><span class="sxs-lookup"><span data-stu-id="d7eea-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="d7eea-135">Представьте, что теперь нужно нарисовать только второй треугольник, но вы хотите использовать тот же буфер вершин и буфер индексов, которые используются при рисовании целых чисел, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="d7eea-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![схема буфера индекса и буфера вершин для второго треугольника](images/dip-fig4.png)

<span data-ttu-id="d7eea-137">Для этого вызова рисования используется первый индекс в виде 3; Это значение называется StartIndex.</span><span class="sxs-lookup"><span data-stu-id="d7eea-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="d7eea-138">В качестве наименьшего используемого индекса VB используется 0; Это значение называется Мининдекс.</span><span class="sxs-lookup"><span data-stu-id="d7eea-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="d7eea-139">Несмотря на то, что для рисования треугольника требуются только три вершины, эти три вершины распределяются по четырем смежным расположениям в буфере вершин. количество расположений внутри непрерывного блока памяти буфера вершин, необходимого для вызова рисования, называется Нумвертицес, а в этом вызове будет установлено значение 4.</span><span class="sxs-lookup"><span data-stu-id="d7eea-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="d7eea-140">Значения Мининдекс и Нумвертицес — это просто подсказки, помогающие оптимизировать доступ к памяти во время обработки вершин на уровне программного обеспечения. можно просто задать включение всего буфера вершин по цене производительности.</span><span class="sxs-lookup"><span data-stu-id="d7eea-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="d7eea-141">Вот вызов рисования для одиночного треугольника; значение аргумента Басевертексиндекс будет объяснено далее:</span><span class="sxs-lookup"><span data-stu-id="d7eea-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="d7eea-142">Сценарий 4. Рисование одного треугольника с корреспондирующей индексацией</span><span class="sxs-lookup"><span data-stu-id="d7eea-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="d7eea-143">Басевертексиндекс — это значение, которое эффективно добавляется в каждый индекс VB, хранящийся в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="d7eea-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="d7eea-144">Например, если мы передали значение 50 для Басевертексиндекс во время предыдущего вызова, это было бы функционально таким же, как использование буфера индексов на следующей схеме в течение времени вызова Дравиндекседпримитиве:</span><span class="sxs-lookup"><span data-stu-id="d7eea-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![схема буфера индекса со значением 50 для басевертексиндекс](images/dip-fig5.png)

<span data-ttu-id="d7eea-146">Это значение редко устанавливается для любого значения, кроме 0, но может быть полезно, если требуется отделить буфер индексов от буфера вершин: Если при заполнении буфера индекса для определенной сетки расположение сетки в буфере вершин еще не известно, можно просто указать вершины сетки в начале буфера вершин. Когда наступает время на вызов Draw, просто передайте фактическое начальное расположение в качестве Басевертексиндекс.</span><span class="sxs-lookup"><span data-stu-id="d7eea-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="d7eea-147">Этот метод также можно использовать при рисовании нескольких экземпляров сетки с помощью одного буфера индекса. Например, если в буфере вершин содержалась две сетки с одинаковым порядком рисования, но слегка разные вершины (возможно, другие рассеянные цвета или координаты текстуры), то обе сетки могут быть выведены с использованием различных значений для Басевертексиндекс.</span><span class="sxs-lookup"><span data-stu-id="d7eea-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="d7eea-148">Понимая эту концепцию на один шаг дальше, можно использовать один буфер индексов для рисования нескольких экземпляров сетки, каждая из которых содержится в другом буфере вершин, просто переполнить, какой буфер вершин активен, и скорректировать Басевертексиндекс по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d7eea-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="d7eea-149">Обратите внимание, что значение Басевертексиндекс также автоматически добавляется в аргумент Мининдекс, что имеет смысл при рассмотрении того, как оно используется:</span><span class="sxs-lookup"><span data-stu-id="d7eea-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="d7eea-150">Представьте, что теперь нам пришлось бы порисовать только второй треугольник Quad, используя тот же буфер индекса, что и раньше; Однако используется другой буфер вершин, в котором четыре раздела находятся в VB index 50.</span><span class="sxs-lookup"><span data-stu-id="d7eea-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="d7eea-151">Относительный порядок четырех вершин остается неизменным, а только начальное расположение в буфере вершин отличается.</span><span class="sxs-lookup"><span data-stu-id="d7eea-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="d7eea-152">Буфер индекс и буфер вершин будут выглядеть так, как на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="d7eea-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![схема буфера индекса и буфера вершин с индексом VB 50](images/dip-fig6.png)

<span data-ttu-id="d7eea-154">Ниже приведен соответствующий вызов Draw. Обратите внимание, что Басевертексиндекс — единственное значение, которое было изменено из предыдущего сценария.</span><span class="sxs-lookup"><span data-stu-id="d7eea-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="d7eea-155">См. также</span><span class="sxs-lookup"><span data-stu-id="d7eea-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7eea-156">Отрисовка примитивов</span><span class="sxs-lookup"><span data-stu-id="d7eea-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
