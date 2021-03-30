---
description: Создает правильную матрицу с просмотром правой части.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Функция D3DXMatrixLookAtRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f09b57d46c6c5dea51c9b55ce6fe507d5bfe415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354203"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="7c08d-103">Функция D3DXMatrixLookAtRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7c08d-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="7c08d-104">Создает правильную матрицу с просмотром правой части.</span><span class="sxs-lookup"><span data-stu-id="7c08d-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c08d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c08d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="7c08d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c08d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c08d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7c08d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c08d-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c08d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c08d-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="7c08d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7c08d-110">*пэйе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c08d-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c08d-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c08d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7c08d-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую точку глаза.</span><span class="sxs-lookup"><span data-stu-id="7c08d-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="7c08d-113">Это значение используется при переводе.</span><span class="sxs-lookup"><span data-stu-id="7c08d-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="7c08d-114">*pAt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c08d-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c08d-115">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c08d-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7c08d-116">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую цель поиска на камере.</span><span class="sxs-lookup"><span data-stu-id="7c08d-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="7c08d-117">*спасенной* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c08d-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c08d-118">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c08d-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7c08d-119">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую текущий мир (обычно \[ 0, 1, 0) \] .</span><span class="sxs-lookup"><span data-stu-id="7c08d-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c08d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c08d-120">Return value</span></span>

<span data-ttu-id="7c08d-121">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c08d-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c08d-122">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является правой рукой и выглядит в матрице.</span><span class="sxs-lookup"><span data-stu-id="7c08d-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c08d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c08d-123">Remarks</span></span>

<span data-ttu-id="7c08d-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="7c08d-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7c08d-125">Таким образом, функция **D3DXMatrixLookAtRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7c08d-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7c08d-126">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c08d-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="7c08d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7c08d-127">Requirements</span></span>



| <span data-ttu-id="7c08d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7c08d-128">Requirement</span></span> | <span data-ttu-id="7c08d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7c08d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c08d-130">Header</span><span class="sxs-lookup"><span data-stu-id="7c08d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="7c08d-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c08d-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7c08d-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c08d-132">Library</span></span><br/> | <dl> <span data-ttu-id="7c08d-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c08d-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c08d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c08d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c08d-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7c08d-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7c08d-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="7c08d-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




