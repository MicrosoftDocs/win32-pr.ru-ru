---
description: Интерфейсы отрисовки для Direct3D состоят из методов, которые визуализируют примитивы из данных вершин, хранящихся в одном или нескольких буферах данных.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Потоки данных вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805728"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="9b2d1-103">Потоки данных вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9b2d1-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="9b2d1-104">Интерфейсы отрисовки для Direct3D состоят из методов, которые визуализируют примитивы из данных вершин, хранящихся в одном или нескольких буферах данных.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="9b2d1-105">Данные вершин состоят из элементов вершин, Объединенных в форму компонентов вершин.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="9b2d1-106">Элементы вершины — наименьшая единица вершины, представляющая сущности, такие как расположение, нормаль или цвет.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="9b2d1-107">Компоненты вершины — это один или несколько элементов вершин, которые хранятся последовательно (чередование на вершину) в одном буфере памяти.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="9b2d1-108">Полная вершина состоит из одного или нескольких компонентов, где каждый компонент находится в отдельном буфере памяти.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="9b2d1-109">Для визуализации примитива выполняется чтение и сборка нескольких компонентов вершин, чтобы обеспечить доступность всех вершин для обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="9b2d1-110">На следующей схеме показан процесс отрисовки примитивов с помощью компонентов вершины.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![Схема процесса отрисовки примитивов с помощью компонентов вершины](images/vertexdata.png)

<span data-ttu-id="9b2d1-112">Отрисовка примитивов состоит из двух этапов.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="9b2d1-113">Сначала настройте один или несколько потоков компонентов вершин. Во-вторых, вызовите метод [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) для отображения из этих потоков.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="9b2d1-114">Идентификация элементов вершин в этих потоках компонентов определяется шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="9b2d1-115">Методы [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) задают смещение в потоках данных вершин таким образом, чтобы произвольное непрерывное подмножество примитивов в пределах одного набора данных вершин можно было визуализировать при каждом вызове Draw.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="9b2d1-116">Это позволяет изменить состояние отрисовки устройства между группами примитивов, отображаемых из тех же буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="9b2d1-117">Поддерживаются как индексированные, так и неиндексированные методы рисования.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="9b2d1-118">Дополнительные сведения см. [в разделе визуализация из буферов вершин и индексов (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="9b2d1-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b2d1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9b2d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2d1-120">Отрисовка примитивов</span><span class="sxs-lookup"><span data-stu-id="9b2d1-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
