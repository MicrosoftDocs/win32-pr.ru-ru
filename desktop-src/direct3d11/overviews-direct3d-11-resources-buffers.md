---
title: Буферы
description: Буферы содержат данные, используемые для описания геометрии, индексирования геометрических данных и констант шейдера. В этом разделе описываются буферы, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.
ms.assetid: 4ab4c9e5-9155-4bfd-b69b-40b3e8cdd4ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c544f00515f25c9c311f6c75fda109d3e88294b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330787"
---
# <a name="buffers"></a><span data-ttu-id="3a91c-104">Буферы</span><span class="sxs-lookup"><span data-stu-id="3a91c-104">Buffers</span></span>

<span data-ttu-id="3a91c-105">Буферы содержат данные, используемые для описания геометрии, индексирования геометрических данных и констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="3a91c-105">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="3a91c-106">В этом разделе описываются буферы, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="3a91c-106">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a91c-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3a91c-107">In this section</span></span>



| <span data-ttu-id="3a91c-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="3a91c-108">Topic</span></span>                                                                                                  | <span data-ttu-id="3a91c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3a91c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a91c-110">Общие сведения о буферах в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3a91c-110">Introduction to Buffers in Direct3D 11</span></span>](overviews-direct3d-11-resources-buffers-intro.md)<br/> | <span data-ttu-id="3a91c-111">Буферный ресурс — это коллекция полностью типизированных данных, сгруппированных в элементы.</span><span class="sxs-lookup"><span data-stu-id="3a91c-111">A buffer resource is a collection of fully typed data grouped into elements.</span></span> <span data-ttu-id="3a91c-112">Буферы можно использовать для хранения самых разных данных, в том числе векторов положений, нормальных векторов, координат текстур (в буфере вершин), индексов (в буфере индексов) или состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="3a91c-112">You can use buffers to store a wide variety of data, including position vectors, normal vectors, texture coordinates in a vertex buffer, indexes in an index buffer, or device state.</span></span> <span data-ttu-id="3a91c-113">Элемент буфера состоит из компонентов числом от 1 до 4.</span><span class="sxs-lookup"><span data-stu-id="3a91c-113">A buffer element is made up of 1 to 4 components.</span></span> <span data-ttu-id="3a91c-114">Элементы буфера могут включать в себя упакованные значения данных (например, значения поверхности R8G8B8A8), единичные 8-разрядные целые числа или четыре 32-разрядных значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="3a91c-114">Buffer elements can include packed data values (like R8G8B8A8 surface values), single 8-bit integers, or four 32-bit floating point values.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3a91c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3a91c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a91c-116">Как создать буфер константы</span><span class="sxs-lookup"><span data-stu-id="3a91c-116">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
</dt> <dt>

[<span data-ttu-id="3a91c-117">Как создать буфер индексов</span><span class="sxs-lookup"><span data-stu-id="3a91c-117">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
</dt> <dt>

[<span data-ttu-id="3a91c-118">Как создать буфер вершин</span><span class="sxs-lookup"><span data-stu-id="3a91c-118">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
</dt> <dt>

[<span data-ttu-id="3a91c-119">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="3a91c-119">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





