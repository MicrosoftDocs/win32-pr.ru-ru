---
description: С учетом сцены, содержащей много объектов, использующих одну геометрию, можно нарисовать множество экземпляров этой геометрии с различными ориентациями, размерами, цветами и т. д. Благодаря значительному повышению производительности, уменьшая объем данных, необходимых для модуля подготовки отчетов.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Эффективная прорисовка нескольких экземпляров геометрии (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894325"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="6b2cc-103">Эффективная прорисовка нескольких экземпляров геометрии (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b2cc-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="6b2cc-104">С учетом сцены, содержащей много объектов, использующих одну геометрию, можно нарисовать множество экземпляров этой геометрии с различными ориентациями, размерами, цветами и т. д. Благодаря значительному повышению производительности, уменьшая объем данных, необходимых для модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="6b2cc-105">Это можно сделать с помощью двух методов: первый для рисования индексированной геометрии и второй для неиндексированной геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="6b2cc-106">Оба метода используют два буфера вершин: один для предоставления геометрических данных, а другой — для передачи данных экземпляра каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="6b2cc-107">Данные экземпляра могут представлять собой широкий спектр сведений, таких как преобразование, цветовые данные или освещение данных, в основном все, что можно описать в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="6b2cc-108">Рисование большого количества экземпляров геометрии с помощью этих методов может значительно сократить объем данных, отправляемых в модуль подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="6b2cc-109">Рисование индексированной геометрии</span><span class="sxs-lookup"><span data-stu-id="6b2cc-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="6b2cc-110">Сравнение производительности индексированных геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="6b2cc-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="6b2cc-111">Рисование неиндексированной геометрии</span><span class="sxs-lookup"><span data-stu-id="6b2cc-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="6b2cc-112">Сравнение производительности неиндексированных геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="6b2cc-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="6b2cc-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6b2cc-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="6b2cc-114">Рисование индексированной геометрии</span><span class="sxs-lookup"><span data-stu-id="6b2cc-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="6b2cc-115">Буфер вершин содержит данные по вершинам, определяемые объявлением вершины.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="6b2cc-116">Предположим, что часть каждой вершины содержит геометрические данные, а часть каждой вершины содержит данные экземпляра для каждого объекта, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![схема буфера вершин для индексированной геометрии](images/drawingmultipleinstances.png)

<span data-ttu-id="6b2cc-118">Для этого способа требуется устройство, которое поддерживает 3 \_ 0 модель шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="6b2cc-119">Этот метод работает с любым программируемым шейдером, но не с фиксированным конвейером функций.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="6b2cc-120">Для буферов вершин, показанных выше, приведены соответствующие объявления буфера вершин:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="6b2cc-121">Эти объявления определяют два буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="6b2cc-122">Первое объявление (для потока 0, обозначенное нулями в столбце 1) определяет геометрические данные, состоящие из: положение, нормаль, тангенс, бинормал и данные координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="6b2cc-123">Второе объявление (для потока 1, обозначенное элементами в столбце 1) определяет данные экземпляра для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="6b2cc-124">Каждый экземпляр определяется с помощью числа с плавающей запятой 4 4 компонентов и цвета из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="6b2cc-125">Первые четыре значения можно использовать для инициализации матрицы 4x4, что означает, что эти данные будут иметь уникальный размер, расположение и поворот каждого экземпляра геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="6b2cc-126">Первые четыре компонента используют семантику координат текстуры, которая, в данном случае, означает, что это общее 4-компонентное число.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="6b2cc-127">При использовании произвольных данных в объявлении вершины используйте семантику координат текстуры, чтобы пометить ее.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="6b2cc-128">Последний элемент в потоке используется для цветовых данных.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="6b2cc-129">Это можно применить в шейдере вершин, чтобы присвоить каждому экземпляру уникальный цвет.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="6b2cc-130">Перед отрисовкой необходимо вызвать [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) , чтобы привязать потоки буфера вершин к устройству.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="6b2cc-131">Ниже приведен пример, в котором привязываются как буферы вершин:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="6b2cc-132">[**Сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) использует [D3DSTREAMSOURCE \_ индекседдата](other-direct3d-constants.md) для обнаружения индексированных геометрических данных.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="6b2cc-133">В этом случае Stream 0 содержит индексированные данные, описывающие геометрию объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="6b2cc-134">Это значение логически объединяется с числом экземпляров геометрии для рисования.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="6b2cc-135">Обратите внимание, что D3DSTREAMSOURCE \_ индекседдата и количество экземпляров для рисования всегда должны быть заданы в потоке 0.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="6b2cc-136">Во втором вызове [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) использует [D3DSTREAMSOURCE \_ инстанцедата](other-direct3d-constants.md) для обнаружения потока, содержащего данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="6b2cc-137">Это значение логически объединяется с 1, так как каждая вершина содержит один набор данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="6b2cc-138">Последние два вызова [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывают указатели буфера вершин к устройству.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="6b2cc-139">После завершения подготовки к просмотру данных экземпляра убедитесь, что частота потока вершин сброшена обратно в состояние по умолчанию (что не использует создание экземпляров).</span><span class="sxs-lookup"><span data-stu-id="6b2cc-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="6b2cc-140">Так как в этом примере используются два потока, установите оба потока, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="6b2cc-141">Сравнение производительности индексированных геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="6b2cc-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="6b2cc-142">Хотя невозможно выполнить одно заключение о том, насколько этот метод может сократить время визуализации в каждом приложении, учитывайте разницу в объеме потоковых данных в среде выполнения и количестве изменений состояния, которые будут сокращены при использовании метода создания экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="6b2cc-143">Эта последовательность визуализации использует преимущества рисования нескольких экземпляров одной и той же геометрии:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="6b2cc-144">Обратите внимание, что цикл визуализации вызывается один раз, данные геометрии передаются в потоке, а n экземпляров — в потоковой передаче один раз.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="6b2cc-145">Следующая последовательность отображения идентична функциональности, но не использует преимущества создания экземпляров:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="6b2cc-146">Обратите внимание, что весь цикл рендеринга упаковывается вторым циклом для рисования каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="6b2cc-147">Теперь геометрические данные передаются в модуль подготовки отчетов n раз (вместо одного раза), а все состояния конвейера также могут быть установлены избыточно для каждого рисуемого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="6b2cc-148">Эта последовательность отображения, скорее всего, будет значительно ниже.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="6b2cc-149">Обратите внимание, что параметры [**дравиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) не изменились между двумя циклами отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="6b2cc-150">Рисование неиндексированной геометрии</span><span class="sxs-lookup"><span data-stu-id="6b2cc-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="6b2cc-151">При [рисовании индексированной геометрии](#drawing-indexed-geometry)буферы вершин были настроены для рисования нескольких экземпляров индексированной геометрии с большей эффективностью.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="6b2cc-152">Для рисования неиндексированной геометрии можно также использовать [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) .</span><span class="sxs-lookup"><span data-stu-id="6b2cc-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="6b2cc-153">Для этого требуется другой макет буфера вершин и другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="6b2cc-154">Чтобы нарисовать неиндексированную геометрию, подготовьте буферы вершин, как на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![схема буфера вершин для неиндексированной геометрии](images/olderstyleinstancing.png)

<span data-ttu-id="6b2cc-156">Этот метод не поддерживается аппаратным ускорением на любом устройстве.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="6b2cc-157">Она поддерживается только при обработке вершин программного обеспечения и будет работать только с шейдерами [VS \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .</span><span class="sxs-lookup"><span data-stu-id="6b2cc-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="6b2cc-158">Поскольку этот метод работает с неиндексированной геометрией, буфер индекса отсутствует.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="6b2cc-159">Как показано на схеме, буфер вершин, содержащий геометрию, содержит n копий геометрических данных.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="6b2cc-160">Для каждого рисуемого экземпляра данные геометрии считываются из первого буфера вершин, а данные экземпляра считываются из второго буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="6b2cc-161">Ниже приведены соответствующие объявления буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="6b2cc-162">Эти объявления идентичны объявлениям, выполненным в примере индексированной геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="6b2cc-163">Опять же, первое объявление (для потока 0) определяет геометрические данные, а второе объявление (для потока 1) определяет данные экземпляра для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="6b2cc-164">При создании первого буфера вершин обязательно загрузите его с числом экземпляров геометрических данных, которые будут изображены.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="6b2cc-165">Перед отрисовкой необходимо настроить разделитель, который сообщает среде выполнения о том, как разделить первый буфер вершин на n экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="6b2cc-166">Затем установите разделитель с помощью [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="6b2cc-167">Первый вызов [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) говорит, что поток 0 содержит n экземпляров m вершин.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="6b2cc-168">Затем [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывает поток 0 к буферу вершинной геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="6b2cc-169">Во втором вызове [**сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) определяет поток 1 в качестве источника данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="6b2cc-170">Вторым параметром является количество вершин в каждом объекте (m).</span><span class="sxs-lookup"><span data-stu-id="6b2cc-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="6b2cc-171">Помните, что поток данных экземпляра должен всегда объявляться как второй поток.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="6b2cc-172">Затем [**сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) привязывает поток 1 к буферу вершин, содержащему данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="6b2cc-173">После завершения подготовки к просмотру данных экземпляра убедитесь, что частота потока вершин сброшена обратно в состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="6b2cc-174">Так как в этом примере используются два потока, установите оба потока, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="6b2cc-175">Сравнение производительности неиндексированных геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="6b2cc-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="6b2cc-176">Основным преимуществом этого стиля создания экземпляров является то, что его можно использовать для неиндексированной геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="6b2cc-177">Хотя невозможно выполнить одно заключение о том, насколько этот метод может сократить время визуализации в каждом приложении, рассмотрите разницу в объеме потоковых данных в среде выполнения и количестве изменений состояния, которые будут сокращены для следующей последовательности визуализации:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="6b2cc-178">Обратите внимание, что цикл визуализации вызывается один раз.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="6b2cc-179">Геометрические данные передаются по потоковой передаче один раз, хотя для потоковой передачи существует n экземпляров геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="6b2cc-180">Данные из буфера вершин экземпляра передаются в потоковую передачу один раз.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="6b2cc-181">Следующая последовательность отображения идентична функциональности, но не использует преимущества создания экземпляров:</span><span class="sxs-lookup"><span data-stu-id="6b2cc-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="6b2cc-182">Без создания экземпляров для рисования каждого объекта цикл визуализации должен быть заключен во второй цикл.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="6b2cc-183">Устраняя второй цикл рендеринга, следует рассчитывать на лучшую производительность из-за меньшего количества изменений состояния визуализации, которые вызываются внутри цикла.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="6b2cc-184">В целом, разумно рассчитывать на то, что индексированный метод ([Рисование индексированной геометрии](#drawing-indexed-geometry)) будет работать лучше, чем неиндексированный метод ([Рисование неиндексированной геометрии](#drawing-non-indexed-geometry)), так как индексированный метод выполняет только потоковую передачу только одной копии данных геометрии.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="6b2cc-185">Обратите внимание, что параметры для [**дравиндекседпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) не изменялись для всех последовательностей отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6b2cc-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b2cc-186">См. также</span><span class="sxs-lookup"><span data-stu-id="6b2cc-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2cc-187">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="6b2cc-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="6b2cc-188">[Пример создания экземпляров](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="6b2cc-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
