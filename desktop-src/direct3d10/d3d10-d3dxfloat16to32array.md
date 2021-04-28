---
description: Функция D3DXFloat16To32Array (D3DX10Math. h) — преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Функция D3DXFloat16To32Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ae624fb05ce10447bd3b9082e171dc01224baaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113292"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="5b093-103">Функция D3DXFloat16To32Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5b093-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="5b093-104">Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5b093-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b093-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b093-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="5b093-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b093-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b093-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b093-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b093-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5b093-109">Указатель на массив 32-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5b093-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="5b093-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b093-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b093-111">Тип: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b093-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="5b093-112">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5b093-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="5b093-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5b093-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b093-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b093-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b093-115">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="5b093-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b093-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b093-116">Return value</span></span>

<span data-ttu-id="5b093-117">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b093-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5b093-118">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5b093-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b093-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5b093-119">Requirements</span></span>



| <span data-ttu-id="5b093-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5b093-120">Requirement</span></span> | <span data-ttu-id="5b093-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5b093-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b093-122">Header</span><span class="sxs-lookup"><span data-stu-id="5b093-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5b093-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b093-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5b093-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b093-124">Library</span></span><br/> | <dl> <span data-ttu-id="5b093-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b093-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b093-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5b093-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b093-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5b093-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
