---
title: Подраспределение в буферах
description: Буферы имеют все функции, необходимые в D3D12 для того, чтобы приложения могли передавать большой диапазон временных данных из ЦП в GPU. В этом разделе рассматриваются четыре распространенных сценария использования ресурсов и буферов и управления ими.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104660"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="8f733-104">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="8f733-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="8f733-105">Буферы имеют все функции, необходимые в D3D12 для того, чтобы приложения могли передавать большой диапазон временных данных из ЦП в GPU.</span><span class="sxs-lookup"><span data-stu-id="8f733-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="8f733-106">В этом разделе рассматриваются четыре распространенных сценария использования ресурсов и буферов и управления ими.</span><span class="sxs-lookup"><span data-stu-id="8f733-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="8f733-107">Как и в случае с D3D11, приложения в D3D12 по-прежнему должны объявлять об использовании памяти при выделении буферов в D3D12 по сравнению с динамическими или промежуточными ресурсами в D3D11, но в D3D12 разработчики имеют больше гибкости и более четкого контроля за использованием памяти.</span><span class="sxs-lookup"><span data-stu-id="8f733-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="8f733-108">Буферы, перераспределение, имеют все функции, необходимые для управления памятью низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="8f733-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8f733-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="8f733-109">In this section</span></span>



| <span data-ttu-id="8f733-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="8f733-110">Topic</span></span>                                                                                        | <span data-ttu-id="8f733-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8f733-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f733-112">Отправка различных типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="8f733-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="8f733-113">Показывает, как использовать один буфер для передачи данных буфера констант и данных буфера вершин в GPU, а также как правильно выделять и размещать данные в буферах.</span><span class="sxs-lookup"><span data-stu-id="8f733-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="8f733-114">Использование одного буфера увеличивает гибкость использования памяти и предоставляет приложениям более строгий контроль использования памяти.</span><span class="sxs-lookup"><span data-stu-id="8f733-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="8f733-115">Также показывает различия между моделями D3D11 и D3D12 для передачи различных типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f733-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="8f733-116">Отправка данных текстуры через буферы</span><span class="sxs-lookup"><span data-stu-id="8f733-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="8f733-117">Передача данных двухмерной или трехмерной текстуры аналогична передаче данных 1D, за исключением того, что приложениям необходимо обратить особое внимание на выравнивание данных, связанное с шагом строки.</span><span class="sxs-lookup"><span data-stu-id="8f733-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="8f733-118">Буферы можно использовать последовательно и параллельно из нескольких частей графического конвейера, и они являются очень гибкими.</span><span class="sxs-lookup"><span data-stu-id="8f733-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="8f733-119">Чтение обратно данных через буфер</span><span class="sxs-lookup"><span data-stu-id="8f733-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="8f733-120">Считывание данных из GPU, таких как запись снимка экрана, предполагает использование кучи Реадбакк.</span><span class="sxs-lookup"><span data-stu-id="8f733-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8f733-121">Управление ресурсами на основе ограждений</span><span class="sxs-lookup"><span data-stu-id="8f733-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="8f733-122">Показывает, как управлять жизненным циклом данных ресурса путем отслеживания хода выполнения GPU через границы.</span><span class="sxs-lookup"><span data-stu-id="8f733-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="8f733-123">Память можно эффективно повторно использовать с ограждениями, тщательно управляя доступностью свободного пространства в памяти, например в реализации кольцевого буфера для отправки кучи.</span><span class="sxs-lookup"><span data-stu-id="8f733-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="8f733-124">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8f733-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f733-125">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="8f733-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





