---
description: Функция D3DXMatrixLookAtLH (D3dx9math. h) — выполняет построение матрицы слева направого вида.
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: Функция D3DXMatrixLookAtLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a423e700c4a42e2ae7f7e522d83a5a4bd9bf3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107592"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="9893a-103">Функция D3DXMatrixLookAtLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9893a-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="9893a-104">Строит левую таблицу, которая выглядит в левой части.</span><span class="sxs-lookup"><span data-stu-id="9893a-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9893a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9893a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="9893a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9893a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9893a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9893a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9893a-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9893a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9893a-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9893a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9893a-110">*пэйе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9893a-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9893a-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9893a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9893a-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую точку глаза.</span><span class="sxs-lookup"><span data-stu-id="9893a-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="9893a-113">Это значение используется при переводе.</span><span class="sxs-lookup"><span data-stu-id="9893a-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="9893a-114">*pAt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9893a-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9893a-115">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9893a-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9893a-116">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую цель поиска на камере.</span><span class="sxs-lookup"><span data-stu-id="9893a-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="9893a-117">*спасенной* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9893a-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9893a-118">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9893a-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9893a-119">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую текущий мир (обычно \[ 0, 1, 0) \] .</span><span class="sxs-lookup"><span data-stu-id="9893a-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9893a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9893a-120">Return value</span></span>

<span data-ttu-id="9893a-121">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9893a-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9893a-122">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является левой и выглядит матрицей.</span><span class="sxs-lookup"><span data-stu-id="9893a-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9893a-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="9893a-123">Remarks</span></span>

<span data-ttu-id="9893a-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9893a-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9893a-125">Таким образом, функция **D3DXMatrixLookAtLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9893a-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9893a-126">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="9893a-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="9893a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9893a-127">Requirements</span></span>



| <span data-ttu-id="9893a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9893a-128">Requirement</span></span> | <span data-ttu-id="9893a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9893a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9893a-130">Header</span><span class="sxs-lookup"><span data-stu-id="9893a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9893a-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9893a-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9893a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9893a-132">Library</span></span><br/> | <dl> <span data-ttu-id="9893a-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9893a-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9893a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9893a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9893a-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9893a-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9893a-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="9893a-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




