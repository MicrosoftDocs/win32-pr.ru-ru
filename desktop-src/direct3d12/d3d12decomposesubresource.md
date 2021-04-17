---
title: Функция D3D12DecomposeSubresource (D3dx12.h)
description: Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Функция D3D12DecomposeSubresource
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713495"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="eebde-104">Функция D3D12DecomposeSubresource</span><span class="sxs-lookup"><span data-stu-id="eebde-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="eebde-105">Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса.</span><span class="sxs-lookup"><span data-stu-id="eebde-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebde-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eebde-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="eebde-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eebde-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebde-108">*Подресурс*</span><span class="sxs-lookup"><span data-stu-id="eebde-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="eebde-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eebde-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eebde-110">Индекс подресурса.</span><span class="sxs-lookup"><span data-stu-id="eebde-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="eebde-111">*миплевелс*</span><span class="sxs-lookup"><span data-stu-id="eebde-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="eebde-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eebde-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eebde-113">Максимальное число уровней mipmap в подресурсе.</span><span class="sxs-lookup"><span data-stu-id="eebde-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="eebde-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="eebde-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="eebde-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eebde-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eebde-116">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="eebde-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="eebde-117">*Мипслице* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="eebde-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="eebde-118">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="eebde-118">Type: **T**</span></span>

<span data-ttu-id="eebde-119">Выводит срез MIP, соответствующий заданному индексу подресурса.</span><span class="sxs-lookup"><span data-stu-id="eebde-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="eebde-120">*Аррайслице* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="eebde-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="eebde-121">Тип: **U**</span><span class="sxs-lookup"><span data-stu-id="eebde-121">Type: **U**</span></span>

<span data-ttu-id="eebde-122">Выводит срез массива, соответствующий заданному индексу подресурса.</span><span class="sxs-lookup"><span data-stu-id="eebde-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="eebde-123">*Планеслице* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="eebde-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="eebde-124">Тип: **V**</span><span class="sxs-lookup"><span data-stu-id="eebde-124">Type: **V**</span></span>

<span data-ttu-id="eebde-125">Выводит срез плоскости, соответствующий заданному индексу подресурса.</span><span class="sxs-lookup"><span data-stu-id="eebde-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebde-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eebde-126">Return value</span></span>

<span data-ttu-id="eebde-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="eebde-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebde-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eebde-128">Remarks</span></span>

<span data-ttu-id="eebde-129">Эта функция определяет, какой срез MIP, срез массива и срез плоскости соответствуют заданному индексу подресурсов.</span><span class="sxs-lookup"><span data-stu-id="eebde-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="eebde-130">Это полезная служебная программа, хотя это и зависит от языка C++.</span><span class="sxs-lookup"><span data-stu-id="eebde-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="eebde-131">Эта функция объявляется следующим образом с параметрами C++ преобразованный для типов **T**, **U** и **V**:</span><span class="sxs-lookup"><span data-stu-id="eebde-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="eebde-132">Требования</span><span class="sxs-lookup"><span data-stu-id="eebde-132">Requirements</span></span>



| <span data-ttu-id="eebde-133">Требование</span><span class="sxs-lookup"><span data-stu-id="eebde-133">Requirement</span></span> | <span data-ttu-id="eebde-134">Значение</span><span class="sxs-lookup"><span data-stu-id="eebde-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eebde-135">Header</span><span class="sxs-lookup"><span data-stu-id="eebde-135">Header</span></span><br/>  | <dl> <span data-ttu-id="eebde-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="eebde-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="eebde-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eebde-137">Library</span></span><br/> | <dl> <span data-ttu-id="eebde-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eebde-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="eebde-139">DLL</span><span class="sxs-lookup"><span data-stu-id="eebde-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="eebde-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eebde-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eebde-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eebde-141">See also</span></span>

[<span data-ttu-id="eebde-142">Вспомогательные функции для D3D12</span><span class="sxs-lookup"><span data-stu-id="eebde-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="eebde-143">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="eebde-143">Subresources</span></span>](subresources.md)
