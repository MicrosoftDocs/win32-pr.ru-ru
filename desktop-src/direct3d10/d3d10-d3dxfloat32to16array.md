---
description: Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Функция D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694267"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="655ea-103">Функция D3DXFloat32To16Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="655ea-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="655ea-104">Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="655ea-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="655ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="655ea-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="655ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="655ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="655ea-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="655ea-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="655ea-108">Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="655ea-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="655ea-109">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="655ea-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="655ea-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="655ea-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="655ea-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="655ea-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="655ea-112">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="655ea-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="655ea-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="655ea-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="655ea-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="655ea-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="655ea-115">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="655ea-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="655ea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="655ea-116">Return value</span></span>

<span data-ttu-id="655ea-117">Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="655ea-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="655ea-118">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="655ea-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="655ea-119">Требования</span><span class="sxs-lookup"><span data-stu-id="655ea-119">Requirements</span></span>



| <span data-ttu-id="655ea-120">Требование</span><span class="sxs-lookup"><span data-stu-id="655ea-120">Requirement</span></span> | <span data-ttu-id="655ea-121">Значение</span><span class="sxs-lookup"><span data-stu-id="655ea-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="655ea-122">Header</span><span class="sxs-lookup"><span data-stu-id="655ea-122">Header</span></span><br/>  | <dl> <span data-ttu-id="655ea-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="655ea-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="655ea-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="655ea-124">Library</span></span><br/> | <dl> <span data-ttu-id="655ea-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="655ea-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="655ea-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="655ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="655ea-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="655ea-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
