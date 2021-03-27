---
title: Индексирование нескольких выходных потоков
description: В Shader Model 5 шейдер Geometry может поддерживать до четырех отдельных потоков. Это означает, что один шейдер может выводить данные между одним и четырьмя выходными потоками в зависимости от числа объявленных потоков.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067447"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="40495-104">Как индексировать несколько выходных потоков</span><span class="sxs-lookup"><span data-stu-id="40495-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="40495-105">В Shader Model 5 шейдер Geometry может поддерживать до четырех отдельных потоков.</span><span class="sxs-lookup"><span data-stu-id="40495-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="40495-106">Это означает, что один шейдер может выводить данные между одним и четырьмя выходными потоками в зависимости от числа объявленных потоков.</span><span class="sxs-lookup"><span data-stu-id="40495-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="40495-107">Индексирование нескольких выходных потоков</span><span class="sxs-lookup"><span data-stu-id="40495-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="40495-108">Определите поток данных, используя тип шаблона потока.</span><span class="sxs-lookup"><span data-stu-id="40495-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="40495-109">Определите второй поток данных, используя тип шаблона потока.</span><span class="sxs-lookup"><span data-stu-id="40495-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="40495-110">Вывод данных в потоки (или оба) с помощью встроенных функций объекта потокового вывода (например, Append или Рестартстрип).</span><span class="sxs-lookup"><span data-stu-id="40495-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="40495-111">При использовании одного выходного потока можно создавать ленты треугольников, полосковые линии или списки точек.</span><span class="sxs-lookup"><span data-stu-id="40495-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="40495-112">При хранении полос треугольника и линии в буфере потокового выхода они развертываются в соответствии со списками треугольников и строк соответственно.</span><span class="sxs-lookup"><span data-stu-id="40495-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="40495-113">Можно также растрировать один поток, не отправляйте его в буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="40495-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="40495-114">При использовании нескольких выходных потоков все потоки должны содержать точки, а в средство программной прорисовки можно отправить до одного выходного потока.</span><span class="sxs-lookup"><span data-stu-id="40495-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="40495-115">Чаще всего приложение не будет выполнять растрирование потока.</span><span class="sxs-lookup"><span data-stu-id="40495-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="40495-116">После потоковой передачи данных в буфер можно использовать эти данные для отображения любого примитивного типа, а не только типа-примитива, который использовался для заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="40495-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="40495-117">Общее число выходных данных шейдера Geometry ограничено до 1024 скаляров.</span><span class="sxs-lookup"><span data-stu-id="40495-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="40495-118">Если существует несколько потоков, число скаляров вычисляется из самого большого типа потока, умноженного на максимальное число вершин.</span><span class="sxs-lookup"><span data-stu-id="40495-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40495-119">Отличия модели шейдеров 4 от модели шейдеров 5:</span><span class="sxs-lookup"><span data-stu-id="40495-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="40495-120">Модель шейдера 4:</span><span class="sxs-lookup"><span data-stu-id="40495-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="40495-121">Максимальное число скаляров для выходного потока — 64.</span><span class="sxs-lookup"><span data-stu-id="40495-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="40495-122">Маска регистра для каждого компонента должна соответствовать диапазону индекса.</span><span class="sxs-lookup"><span data-stu-id="40495-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="40495-123">Модель шейдера 5:</span><span class="sxs-lookup"><span data-stu-id="40495-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="40495-124">Максимальное число скаляров для выходного потока — 128.</span><span class="sxs-lookup"><span data-stu-id="40495-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="40495-125">Маску регистра для каждого компонента не нужно сопоставлять по диапазону индекса.</span><span class="sxs-lookup"><span data-stu-id="40495-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="40495-126">Динамическое индексирование выходов должно быть допустимым во всех потоках.</span><span class="sxs-lookup"><span data-stu-id="40495-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="40495-127">Режимам интерполяции не требуется сопоставлять для потоков.</span><span class="sxs-lookup"><span data-stu-id="40495-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="40495-128">См. также</span><span class="sxs-lookup"><span data-stu-id="40495-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40495-129">Функции шейдера Geometry</span><span class="sxs-lookup"><span data-stu-id="40495-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





