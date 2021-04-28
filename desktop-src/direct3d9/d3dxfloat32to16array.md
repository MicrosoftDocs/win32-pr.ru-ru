---
description: Функция D3DXFloat32To16Array (D3dx9math. h) — преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Функция D3DXFloat32To16Array (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc00df150c48e285d5478eb9b11df6c5203d6bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094262"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="0375b-103">Функция D3DXFloat32To16Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0375b-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="0375b-104">Преобразует массив из 32-разрядных чисел с плавающей запятой в 16-битные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0375b-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0375b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0375b-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0375b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0375b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0375b-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0375b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0375b-108">Тип: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="0375b-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0375b-109">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0375b-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0375b-110">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0375b-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0375b-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0375b-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0375b-112">Указатель на массив из 32 разрядов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0375b-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0375b-113">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="0375b-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0375b-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0375b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0375b-115">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="0375b-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0375b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0375b-116">Return value</span></span>

<span data-ttu-id="0375b-117">Тип: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="0375b-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0375b-118">Указатель на массив 16-разрядных элементов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0375b-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0375b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0375b-119">Requirements</span></span>



| <span data-ttu-id="0375b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0375b-120">Requirement</span></span> | <span data-ttu-id="0375b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0375b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0375b-122">Header</span><span class="sxs-lookup"><span data-stu-id="0375b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0375b-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0375b-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0375b-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0375b-124">Library</span></span><br/> | <dl> <span data-ttu-id="0375b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0375b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0375b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0375b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0375b-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0375b-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
