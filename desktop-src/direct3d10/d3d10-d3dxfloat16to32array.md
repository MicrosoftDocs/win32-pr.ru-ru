---
description: Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.
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
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354990"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="0dccb-103">Функция D3DXFloat16To32Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0dccb-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="0dccb-104">Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0dccb-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dccb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dccb-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0dccb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dccb-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dccb-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dccb-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dccb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0dccb-109">Указатель на массив 32-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0dccb-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0dccb-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dccb-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dccb-111">Тип: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="0dccb-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0dccb-112">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0dccb-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0dccb-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0dccb-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dccb-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dccb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dccb-115">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="0dccb-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dccb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dccb-116">Return value</span></span>

<span data-ttu-id="0dccb-117">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dccb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0dccb-118">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0dccb-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dccb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0dccb-119">Requirements</span></span>



| <span data-ttu-id="0dccb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0dccb-120">Requirement</span></span> | <span data-ttu-id="0dccb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0dccb-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dccb-122">Header</span><span class="sxs-lookup"><span data-stu-id="0dccb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0dccb-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dccb-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0dccb-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0dccb-124">Library</span></span><br/> | <dl> <span data-ttu-id="0dccb-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dccb-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0dccb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dccb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dccb-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0dccb-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
