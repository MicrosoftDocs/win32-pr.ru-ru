---
title: Функция Мемкписубресаурце (D3dx12. h)
description: Копирует подресурс по строкам.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Функция Мемкписубресаурце
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694230"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="059ce-104">Функция Мемкписубресаурце</span><span class="sxs-lookup"><span data-stu-id="059ce-104">MemcpySubresource function</span></span>

<span data-ttu-id="059ce-105">Копирует подресурс по строкам.</span><span class="sxs-lookup"><span data-stu-id="059ce-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="059ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="059ce-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="059ce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="059ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="059ce-108">*пдест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="059ce-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="059ce-109">Тип: **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="059ce-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="059ce-110">Указатель на структуру [**D3D12 \_ MEMCPY \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) , описывающую назначение операции копирования в память.</span><span class="sxs-lookup"><span data-stu-id="059ce-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="059ce-111">*pSrc* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="059ce-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="059ce-112">Тип: **\* const [**D3D12 \_ \_ данные о подресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**</span><span class="sxs-lookup"><span data-stu-id="059ce-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="059ce-113">Указатель на структуру [**\_ \_ данных подресурса D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) , которая описывает источник операции копирования в память.</span><span class="sxs-lookup"><span data-stu-id="059ce-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="059ce-114">*ровсизеинбитес*</span><span class="sxs-lookup"><span data-stu-id="059ce-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="059ce-115">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="059ce-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="059ce-116">Размер каждой строки в байтах.</span><span class="sxs-lookup"><span data-stu-id="059ce-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="059ce-117">*нумровс*</span><span class="sxs-lookup"><span data-stu-id="059ce-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="059ce-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="059ce-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="059ce-119">Количество строк.</span><span class="sxs-lookup"><span data-stu-id="059ce-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="059ce-120">*нумслицес*</span><span class="sxs-lookup"><span data-stu-id="059ce-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="059ce-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="059ce-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="059ce-122">Количество срезов.</span><span class="sxs-lookup"><span data-stu-id="059ce-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="059ce-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="059ce-123">Return value</span></span>

<span data-ttu-id="059ce-124">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="059ce-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="059ce-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="059ce-125">Remarks</span></span>

<span data-ttu-id="059ce-126">Также рассмотрим следующие методы.</span><span class="sxs-lookup"><span data-stu-id="059ce-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="059ce-127">**ID3D12Resource:: Вритетосубресаурце**</span><span class="sxs-lookup"><span data-stu-id="059ce-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="059ce-128">**ID3D12Resource:: Реадфромсубресаурце**</span><span class="sxs-lookup"><span data-stu-id="059ce-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="059ce-129">**ID3D12GraphicsCommandList:: Копиресаурце**</span><span class="sxs-lookup"><span data-stu-id="059ce-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="059ce-130">Требования</span><span class="sxs-lookup"><span data-stu-id="059ce-130">Requirements</span></span>



| <span data-ttu-id="059ce-131">Требование</span><span class="sxs-lookup"><span data-stu-id="059ce-131">Requirement</span></span> | <span data-ttu-id="059ce-132">Значение</span><span class="sxs-lookup"><span data-stu-id="059ce-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="059ce-133">Header</span><span class="sxs-lookup"><span data-stu-id="059ce-133">Header</span></span><br/>  | <dl> <span data-ttu-id="059ce-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="059ce-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="059ce-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="059ce-135">Library</span></span><br/> | <dl> <span data-ttu-id="059ce-136"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="059ce-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="059ce-137">DLL</span><span class="sxs-lookup"><span data-stu-id="059ce-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="059ce-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="059ce-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="059ce-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="059ce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059ce-140">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="059ce-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="059ce-141">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="059ce-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

