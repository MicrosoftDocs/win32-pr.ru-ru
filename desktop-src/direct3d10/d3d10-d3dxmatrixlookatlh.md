---
description: Строит левую таблицу, которая выглядит в левой части.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: Функция D3DXMatrixLookAtLH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a5a7ffa8750fb08174f45b1069f103bfe08be1f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548079"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="78555-103">Функция D3DXMatrixLookAtLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="78555-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="78555-104">Строит левую таблицу, которая выглядит в левой части.</span><span class="sxs-lookup"><span data-stu-id="78555-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="78555-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78555-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="78555-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78555-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="78555-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78555-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="78555-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78555-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="78555-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="78555-110">*пэйе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78555-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78555-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="78555-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="78555-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющий точку глаза.</span><span class="sxs-lookup"><span data-stu-id="78555-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="78555-113">Это значение используется при переводе.</span><span class="sxs-lookup"><span data-stu-id="78555-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="78555-114">*pAt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78555-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78555-115">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="78555-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="78555-116">Указатель на структуру D3DXVECTOR3, определяющую цель поиска на камере.</span><span class="sxs-lookup"><span data-stu-id="78555-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="78555-117">*спасенной* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78555-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78555-118">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="78555-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="78555-119">Указатель на структуру D3DXVECTOR3, определяющую текущий мир (обычно \[ 0, 1, 0) \] .</span><span class="sxs-lookup"><span data-stu-id="78555-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78555-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78555-120">Return value</span></span>

<span data-ttu-id="78555-121">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="78555-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78555-122">Указатель на структуру D3DXMATRIX, которая является левой и выглядит матрицей.</span><span class="sxs-lookup"><span data-stu-id="78555-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="78555-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78555-123">Remarks</span></span>

<span data-ttu-id="78555-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="78555-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="78555-125">Таким образом, функция D3DXMatrixLookAtLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="78555-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="78555-126">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="78555-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="78555-127">Требования</span><span class="sxs-lookup"><span data-stu-id="78555-127">Requirements</span></span>



| <span data-ttu-id="78555-128">Требование</span><span class="sxs-lookup"><span data-stu-id="78555-128">Requirement</span></span> | <span data-ttu-id="78555-129">Значение</span><span class="sxs-lookup"><span data-stu-id="78555-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78555-130">Header</span><span class="sxs-lookup"><span data-stu-id="78555-130">Header</span></span><br/>  | <dl> <span data-ttu-id="78555-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78555-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="78555-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78555-132">Library</span></span><br/> | <dl> <span data-ttu-id="78555-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78555-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78555-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78555-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78555-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="78555-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
