---
description: Функция D3DXFloat16To32Array (D3dx9math. h) — преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Функция D3DXFloat16To32Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107602"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="0b77c-103">Функция D3DXFloat16To32Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0b77c-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="0b77c-104">Преобразует массив 16-разрядных элементов с плавающей запятой в 32-разрядное число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b77c-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b77c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b77c-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0b77c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b77c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b77c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0b77c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b77c-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b77c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b77c-109">Указатель на массив 32-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b77c-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0b77c-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b77c-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b77c-111">Тип: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b77c-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0b77c-112">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b77c-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0b77c-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0b77c-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b77c-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b77c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b77c-115">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="0b77c-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b77c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b77c-116">Return value</span></span>

<span data-ttu-id="0b77c-117">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b77c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b77c-118">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b77c-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b77c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0b77c-119">Requirements</span></span>



| <span data-ttu-id="0b77c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0b77c-120">Requirement</span></span> | <span data-ttu-id="0b77c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0b77c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b77c-122">Header</span><span class="sxs-lookup"><span data-stu-id="0b77c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0b77c-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b77c-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0b77c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b77c-124">Library</span></span><br/> | <dl> <span data-ttu-id="0b77c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b77c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b77c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0b77c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b77c-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0b77c-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
