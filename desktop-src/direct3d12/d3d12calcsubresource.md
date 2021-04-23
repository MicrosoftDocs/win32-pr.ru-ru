---
title: Функция D3D12CalcSubresource (D3dx12. h)
description: Вычисляет индекс подресурсов для текстуры.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Функция D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703664"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="2aa46-104">Функция D3D12CalcSubresource</span><span class="sxs-lookup"><span data-stu-id="2aa46-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="2aa46-105">Вычисляет индекс подресурсов для текстуры.</span><span class="sxs-lookup"><span data-stu-id="2aa46-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa46-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2aa46-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="2aa46-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2aa46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa46-108">*мипслице*</span><span class="sxs-lookup"><span data-stu-id="2aa46-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa46-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-110">Отсчитываемый от нуля индекс для адреса уровня mipmap. 0 означает первый, наиболее подробный уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="2aa46-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="2aa46-111">*аррайслице*</span><span class="sxs-lookup"><span data-stu-id="2aa46-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa46-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-113">Отсчитываемый от нуля индекс для уровня массива, по которому производится адресация; всегда используйте 0 для 3D-текстур.</span><span class="sxs-lookup"><span data-stu-id="2aa46-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="2aa46-114">*планеслице*</span><span class="sxs-lookup"><span data-stu-id="2aa46-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa46-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-116">Отсчитываемый от нуля индекс для уровня плоскости, по которому производится адресация.</span><span class="sxs-lookup"><span data-stu-id="2aa46-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="2aa46-117">*миплевелс*</span><span class="sxs-lookup"><span data-stu-id="2aa46-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa46-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-119">Число уровней mipmap в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="2aa46-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="2aa46-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="2aa46-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="2aa46-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-122">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="2aa46-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa46-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2aa46-123">Return value</span></span>

<span data-ttu-id="2aa46-124">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2aa46-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2aa46-125">Индекс, который равен Мипслице + (Аррайслице \* миплевелс).</span><span class="sxs-lookup"><span data-stu-id="2aa46-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa46-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2aa46-126">Remarks</span></span>

<span data-ttu-id="2aa46-127">Буфер является неструктурированным ресурсом и, следовательно, определяется как содержащий один подресурс.</span><span class="sxs-lookup"><span data-stu-id="2aa46-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="2aa46-128">Для интерфейсов API, которые принимают буферы, не требуется индекс подресурса.</span><span class="sxs-lookup"><span data-stu-id="2aa46-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="2aa46-129">Текстура с другой стороны очень структурирована.</span><span class="sxs-lookup"><span data-stu-id="2aa46-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="2aa46-130">Каждый объект текстуры может содержать один или несколько подресурсов в зависимости от размера массива и количества mipmap уровней.</span><span class="sxs-lookup"><span data-stu-id="2aa46-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="2aa46-131">Для томов (трехмерных) все срезы для данного уровня mipmap являются одним индексом подресурса.</span><span class="sxs-lookup"><span data-stu-id="2aa46-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa46-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2aa46-132">Requirements</span></span>



| <span data-ttu-id="2aa46-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2aa46-133">Requirement</span></span> | <span data-ttu-id="2aa46-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2aa46-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa46-135">Header</span><span class="sxs-lookup"><span data-stu-id="2aa46-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2aa46-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa46-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2aa46-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2aa46-137">Library</span></span><br/> | <dl> <span data-ttu-id="2aa46-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2aa46-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2aa46-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2aa46-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="2aa46-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aa46-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa46-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2aa46-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa46-142">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="2aa46-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2aa46-143">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="2aa46-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

