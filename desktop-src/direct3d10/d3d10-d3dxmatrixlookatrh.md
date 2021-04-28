---
description: Функция D3DXMatrixLookAtRH (D3DX10Math. h) — создает таблицу с правой стороны и просмотром.
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Функция D3DXMatrixLookAtRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0380207124e4a446b6303dbb377d116b8ae058ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103452"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="578b7-103">Функция D3DXMatrixLookAtRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="578b7-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="578b7-104">Создает правильную матрицу с просмотром правой части.</span><span class="sxs-lookup"><span data-stu-id="578b7-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="578b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="578b7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="578b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="578b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578b7-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="578b7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="578b7-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="578b7-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="578b7-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="578b7-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="578b7-110">*пэйе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="578b7-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578b7-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="578b7-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="578b7-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющий точку глаза.</span><span class="sxs-lookup"><span data-stu-id="578b7-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="578b7-113">Это значение используется при переводе.</span><span class="sxs-lookup"><span data-stu-id="578b7-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="578b7-114">*pAt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="578b7-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578b7-115">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="578b7-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="578b7-116">Указатель на структуру D3DXVECTOR3, определяющую цель поиска на камере.</span><span class="sxs-lookup"><span data-stu-id="578b7-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="578b7-117">*спасенной* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="578b7-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578b7-118">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="578b7-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="578b7-119">Указатель на структуру D3DXVECTOR3, определяющую текущий мир (обычно \[ 0, 1, 0) \] .</span><span class="sxs-lookup"><span data-stu-id="578b7-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578b7-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="578b7-120">Return value</span></span>

<span data-ttu-id="578b7-121">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="578b7-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="578b7-122">Указатель на структуру D3DXMATRIX, которая является правой рукой и выглядит в матрице.</span><span class="sxs-lookup"><span data-stu-id="578b7-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="578b7-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="578b7-123">Remarks</span></span>

<span data-ttu-id="578b7-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="578b7-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="578b7-125">Таким образом, функция D3DXMatrixLookAtRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="578b7-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="578b7-126">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="578b7-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="578b7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="578b7-127">Requirements</span></span>



| <span data-ttu-id="578b7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="578b7-128">Requirement</span></span> | <span data-ttu-id="578b7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="578b7-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="578b7-130">Header</span><span class="sxs-lookup"><span data-stu-id="578b7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="578b7-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="578b7-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="578b7-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="578b7-132">Library</span></span><br/> | <dl> <span data-ttu-id="578b7-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="578b7-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="578b7-134">См. также</span><span class="sxs-lookup"><span data-stu-id="578b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578b7-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="578b7-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
