---
title: Вспомогательные функции для D3D12
description: Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Вспомогательные функции
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700603"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="09fa2-105">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="09fa2-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="09fa2-106">Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="09fa2-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="09fa2-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="09fa2-107">In this section</span></span>



| <span data-ttu-id="09fa2-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="09fa2-108">Topic</span></span>                                                                                             | <span data-ttu-id="09fa2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="09fa2-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09fa2-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="09fa2-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="09fa2-111">Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="09fa2-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="09fa2-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="09fa2-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="09fa2-113">Вычисляет индекс подресурсов для текстуры.</span><span class="sxs-lookup"><span data-stu-id="09fa2-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="09fa2-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="09fa2-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="09fa2-115">Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса.</span><span class="sxs-lookup"><span data-stu-id="09fa2-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="09fa2-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="09fa2-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="09fa2-117">Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера ( **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="09fa2-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="09fa2-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="09fa2-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="09fa2-119">Указывает, является ли макет непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="09fa2-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="09fa2-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="09fa2-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="09fa2-121">Возвращает тип подобъекта, соответствующий базовому классу переданного типа подобъекта.</span><span class="sxs-lookup"><span data-stu-id="09fa2-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="09fa2-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="09fa2-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="09fa2-123">Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.</span><span class="sxs-lookup"><span data-stu-id="09fa2-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="09fa2-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="09fa2-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="09fa2-125">Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей.</span><span class="sxs-lookup"><span data-stu-id="09fa2-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="09fa2-126">Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09fa2-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="09fa2-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="09fa2-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="09fa2-128">Возвращает требуемый размер буфера, используемый для передачи данных.</span><span class="sxs-lookup"><span data-stu-id="09fa2-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="09fa2-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="09fa2-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="09fa2-130">Копирует подресурс по строкам.</span><span class="sxs-lookup"><span data-stu-id="09fa2-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="09fa2-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="09fa2-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="09fa2-132">Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="09fa2-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="09fa2-133">**Updatesubresources (выделение кучи)**</span><span class="sxs-lookup"><span data-stu-id="09fa2-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="09fa2-134">Обновляет подресурсы с реализацией выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="09fa2-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="09fa2-135">**Updatesubresources (выделение стека)**</span><span class="sxs-lookup"><span data-stu-id="09fa2-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="09fa2-136">Обновляет подресурсы с реализацией выделения стека.</span><span class="sxs-lookup"><span data-stu-id="09fa2-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="09fa2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="09fa2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09fa2-138">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="09fa2-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="09fa2-139">Вспомогательные структуры и функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="09fa2-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





