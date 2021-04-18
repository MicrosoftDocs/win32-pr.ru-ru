---
description: Извлекает параметры сетки, включенные для этой сетки во время создания.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: Метод ID3DXBaseMesh::-Options (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713863"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="c682d-103">Метод ID3DXBaseMesh:: Options</span><span class="sxs-lookup"><span data-stu-id="c682d-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="c682d-104">Извлекает параметры сетки, включенные для этой сетки во время создания.</span><span class="sxs-lookup"><span data-stu-id="c682d-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c682d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c682d-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="c682d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c682d-106">Parameters</span></span>

<span data-ttu-id="c682d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c682d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c682d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c682d-108">Return value</span></span>

<span data-ttu-id="c682d-109">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c682d-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c682d-110">Возвращает сочетание одного или нескольких из следующих флагов, указывающих параметры, включенные для этой сетки во время создания.</span><span class="sxs-lookup"><span data-stu-id="c682d-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="c682d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c682d-111">Value</span></span>                   | <span data-ttu-id="c682d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c682d-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c682d-113">D3DXMESH- \_ 32-разрядный</span><span class="sxs-lookup"><span data-stu-id="c682d-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="c682d-114">Используйте 32-разрядные индексы.</span><span class="sxs-lookup"><span data-stu-id="c682d-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c682d-115">D3DXMESH \_ донотклип</span><span class="sxs-lookup"><span data-stu-id="c682d-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="c682d-116">Используйте флаг D3DUSAGE \_ донотклип Usage для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="c682d-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="c682d-117">D3DXMESH \_ dynamic</span><span class="sxs-lookup"><span data-stu-id="c682d-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="c682d-118">Эквивалентно указанию D3DXMESH \_ VB \_ dynamic и D3DXMESH \_ , \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="c682d-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="c682d-119">D3DXMESH \_ ртпатчес</span><span class="sxs-lookup"><span data-stu-id="c682d-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="c682d-120">Используйте флаг D3DUSAGE \_ ртпатчес Usage для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="c682d-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="c682d-121">D3DXMESH \_ нпатчес</span><span class="sxs-lookup"><span data-stu-id="c682d-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="c682d-122">Указание этого флага приводит к созданию вершины и буфера индекса сетки с \_ флагом D3DUSAGE нпатчес.</span><span class="sxs-lookup"><span data-stu-id="c682d-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="c682d-123">Это необходимо, если объект сетки должен быть визуализирован с помощью N-Patch улучшения.</span><span class="sxs-lookup"><span data-stu-id="c682d-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="c682d-124">\_Управляемый D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="c682d-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="c682d-125">Эквивалентно указанию \_ \_ управляемого и D3DXMESHного \_ управления D3DXMESH VB \_ .</span><span class="sxs-lookup"><span data-stu-id="c682d-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="c682d-126">\_Точки D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="c682d-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="c682d-127">Используйте \_ флаг использования точек D3DUSAGE для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="c682d-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="c682d-128">\_Динамический D3DXMESH \_</span><span class="sxs-lookup"><span data-stu-id="c682d-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="c682d-129">Используйте \_ флаг динамического использования D3DUSAGE для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="c682d-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="c682d-130">\_ \_ УПРАВЛЯЕМый D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="c682d-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="c682d-131">Используйте \_ управляемый класс памяти D3DPOOL для индексных буферов.</span><span class="sxs-lookup"><span data-stu-id="c682d-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="c682d-132">D3DXMESH \_ \_ системмем</span><span class="sxs-lookup"><span data-stu-id="c682d-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="c682d-133">Используйте \_ класс памяти D3DPOOL системмем для индексных буферов.</span><span class="sxs-lookup"><span data-stu-id="c682d-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="c682d-134">D3DXMESHа ( \_ \_ WRITEONLY)</span><span class="sxs-lookup"><span data-stu-id="c682d-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="c682d-135">Используйте \_ флаг использования D3DUSAGE WRITEONLY для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="c682d-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="c682d-136">D3DXMESH \_ системмем</span><span class="sxs-lookup"><span data-stu-id="c682d-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="c682d-137">Эквивалентно указанию D3DXMESH \_ VB \_ СИСТЕММЕМ и D3DXMESH \_ \_ системмем.</span><span class="sxs-lookup"><span data-stu-id="c682d-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="c682d-138">D3DXMESH \_ VB \_ dynamic</span><span class="sxs-lookup"><span data-stu-id="c682d-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="c682d-139">Используйте \_ флаг динамического использования D3DUSAGE для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="c682d-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="c682d-140">\_ \_ Управляемый VB D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="c682d-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="c682d-141">Используйте \_ управляемый класс памяти D3DPOOL для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="c682d-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="c682d-142">D3DXMESH \_ VB \_ системмем</span><span class="sxs-lookup"><span data-stu-id="c682d-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="c682d-143">Используйте \_ класс памяти D3DPOOL системмем для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="c682d-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="c682d-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="c682d-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="c682d-145">Используйте \_ флаг использования D3DUSAGE WRITEONLY для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="c682d-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="c682d-146">D3DXMESH \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="c682d-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="c682d-147">Эквивалентно указанию D3DXMESH \_ VB \_ WRITEONLY и D3DXMESH с помощью \_ \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="c682d-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="c682d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="c682d-148">Requirements</span></span>



| <span data-ttu-id="c682d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="c682d-149">Requirement</span></span> | <span data-ttu-id="c682d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="c682d-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c682d-151">Header</span><span class="sxs-lookup"><span data-stu-id="c682d-151">Header</span></span><br/>  | <dl> <span data-ttu-id="c682d-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c682d-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c682d-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c682d-153">Library</span></span><br/> | <dl> <span data-ttu-id="c682d-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c682d-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c682d-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c682d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c682d-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="c682d-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
