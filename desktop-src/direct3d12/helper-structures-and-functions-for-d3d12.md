---
title: Вспомогательные структуры и функции для D3D12
description: Эти вспомогательные структуры и вспомогательные функции объявляются в d3dx12. h.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Вспомогательные функции
- Вспомогательные структуры
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105719059"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="d896e-106">Вспомогательные структуры и функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="d896e-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="d896e-107">Эти вспомогательные структуры и вспомогательные функции объявляются в **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d896e-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="d896e-108">Эти вспомогательные структуры можно использовать для создания и инициализации структур Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d896e-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="d896e-109">Эти вспомогательные структуры ведут себя как классы C++.</span><span class="sxs-lookup"><span data-stu-id="d896e-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="d896e-110">Каждая вспомогательная структура обычно имеет конструктор по умолчанию, явный конструктор, деструктор и оператор CAST для связанной структуры D3D12.</span><span class="sxs-lookup"><span data-stu-id="d896e-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="d896e-111">Каждая вспомогательная структура имеет префикс "C" и связана со структурой D3D12, в которой отсутствует префикс "C".</span><span class="sxs-lookup"><span data-stu-id="d896e-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="d896e-112">Большинство вспомогательных структур содержат методы членов инициализации, некоторые содержат функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="d896e-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="d896e-113">**d3dx12. h** доступен отдельно от заголовков Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d896e-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="d896e-114">Вы можете скачать **d3dx12. h** из [вспомогательной библиотеки D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span><span class="sxs-lookup"><span data-stu-id="d896e-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d896e-115">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d896e-115">In this section</span></span>



| <span data-ttu-id="d896e-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="d896e-116">Topic</span></span>                                                                     | <span data-ttu-id="d896e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d896e-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d896e-118">Вспомогательные интерфейсы для D3D12</span><span class="sxs-lookup"><span data-stu-id="d896e-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="d896e-119">Эти вспомогательные интерфейсы особенно полезны при обработке подресурсов и объявляются в **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d896e-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="d896e-120">Вспомогательные структуры для D3D12</span><span class="sxs-lookup"><span data-stu-id="d896e-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="d896e-121">Эти вспомогательные структуры помогают инициализировать многие из структур Direct3D 12 и объявляются в **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d896e-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="d896e-122">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="d896e-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="d896e-123">Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d896e-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d896e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d896e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d896e-125">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d896e-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





