---
title: Стадия Stream-Output
description: Целью этапа потокового вывода является непрерывный вывод (или потоковая) данных вершин с этапа шейдера геометрии (или этапа вершинного шейдера, если этап Geometry-Shader неактивен) в один или несколько буферов в памяти (см. начало работы с этапом Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- Стадия вывода потока (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488574"
---
# <a name="stream-output-stage"></a><span data-ttu-id="e95c3-104">Стадия Stream-Output</span><span class="sxs-lookup"><span data-stu-id="e95c3-104">Stream-Output Stage</span></span>

<span data-ttu-id="e95c3-105">Целью этапа потокового вывода является непрерывный вывод (или потоковая) данных вершин с этапа шейдера геометрии (или этапа вершинного шейдера, если этап Geometry-Shader неактивен) в один или несколько буферов в памяти (см. [Начало работы с этапом Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="e95c3-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="e95c3-106">Этап потокового вывода (SO) находится в конвейере сразу после этапа создания шейдера geometry и непосредственно перед этапом растрирования, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e95c3-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![схема расположения этапа потокового вывода в конвейере](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="e95c3-108">Данные поточно переданные в память можно считать обратно в конвейер в последующем проходе отрисовки или скопировать в промежуточный ресурс (для его считывания центральным процессором).</span><span class="sxs-lookup"><span data-stu-id="e95c3-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="e95c3-109">Объем данных в потоке может быть разным; API [**ссылку ID3D11DeviceContext::D равауто**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) предназначен для работы с данными без необходимости запроса (GPU) о объеме записанных данных.</span><span class="sxs-lookup"><span data-stu-id="e95c3-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="e95c3-110">Если линейка треугольника или линии привязана к этапу входного ассемблера, то каждая полоса преобразуется в список до их потоковой передачи. Вершины всегда записываются как полные примитивы (например, 3 вершины за раз для треугольников); неполные примитивы никогда не выводятся из потоков. Типы-примитивы с соседкой отбросить соседство перед выходом потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="e95c3-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="e95c3-111">Существует два способа подать данные потокового вывода в конвейер:</span><span class="sxs-lookup"><span data-stu-id="e95c3-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="e95c3-112">Потоковая передача выходных данных может быть возвращена на этапе ассемблера ввода.</span><span class="sxs-lookup"><span data-stu-id="e95c3-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="e95c3-113">Потоковая передача данных может быть прочитана программируемыми шейдерами с помощью функций Load (например, [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span><span class="sxs-lookup"><span data-stu-id="e95c3-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="e95c3-114">Чтобы использовать буфер в качестве ресурса потокового вывода, создайте буфер с помощью флага [**\_ \_ \_ Output потока привязки D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="e95c3-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="e95c3-115">Этап потокового вывода поддерживает до 4 буферов одновременно.</span><span class="sxs-lookup"><span data-stu-id="e95c3-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="e95c3-116">Если вы выполняете потоковую передачу данных в несколько буферов, каждый буфер можно записать только один элемент (до 4 компонент) данных каждой вершины, с шагом подразумеваемых данных равным ширине элемента в каждом буфере (это совместимо со способом, которым буферы одного элемента можно привязать для ввода в этапы шейдеров).</span><span class="sxs-lookup"><span data-stu-id="e95c3-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="e95c3-117">Кроме того, если буферы имеют различные размеры, запись будет остановлена, как только заполнится один из буферов.</span><span class="sxs-lookup"><span data-stu-id="e95c3-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="e95c3-118">Если вы выполняете потоковую передачу данных в один буфер, то он может сохранить до 64 скалярных компонент индивидуальных данных вершины (256 байт или меньше) или же шаг вершины может иметь размер до 2048 байт.</span><span class="sxs-lookup"><span data-stu-id="e95c3-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e95c3-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e95c3-119">In this section</span></span>



| <span data-ttu-id="e95c3-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="e95c3-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="e95c3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e95c3-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e95c3-122">Начало работы с этапом Stream-Output</span><span class="sxs-lookup"><span data-stu-id="e95c3-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="e95c3-123">В этом разделе описывается использование шейдера Geometry с стадией вывода потока.</span><span class="sxs-lookup"><span data-stu-id="e95c3-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e95c3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e95c3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e95c3-125">Графический конвейер</span><span class="sxs-lookup"><span data-stu-id="e95c3-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="e95c3-126">Этапы конвейера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e95c3-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

