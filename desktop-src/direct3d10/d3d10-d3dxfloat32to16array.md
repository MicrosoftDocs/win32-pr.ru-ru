---
description: Функция D3DXFloat32To16Array (D3DX10Math. h) — преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.
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
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103522"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="ed27a-103">Функция D3DXFloat32To16Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ed27a-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="ed27a-104">Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed27a-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed27a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed27a-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="ed27a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed27a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed27a-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed27a-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed27a-108">Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed27a-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="ed27a-109">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed27a-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="ed27a-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed27a-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed27a-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ed27a-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed27a-112">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed27a-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="ed27a-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ed27a-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed27a-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed27a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed27a-115">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="ed27a-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed27a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed27a-116">Return value</span></span>

<span data-ttu-id="ed27a-117">Тип: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed27a-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="ed27a-118">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed27a-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed27a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ed27a-119">Requirements</span></span>



| <span data-ttu-id="ed27a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ed27a-120">Requirement</span></span> | <span data-ttu-id="ed27a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ed27a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed27a-122">Header</span><span class="sxs-lookup"><span data-stu-id="ed27a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ed27a-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed27a-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ed27a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed27a-124">Library</span></span><br/> | <dl> <span data-ttu-id="ed27a-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed27a-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed27a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ed27a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed27a-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="ed27a-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
