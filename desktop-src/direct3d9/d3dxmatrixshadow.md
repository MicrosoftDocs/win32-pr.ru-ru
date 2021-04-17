---
description: Строит матрицу, которая выполняет сведение геометрии в плоскость.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Функция D3DXMatrixShadow (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685002"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="487e9-103">Функция D3DXMatrixShadow (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="487e9-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="487e9-104">Строит матрицу, которая выполняет сведение геометрии в плоскость.</span><span class="sxs-lookup"><span data-stu-id="487e9-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="487e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="487e9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="487e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="487e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487e9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="487e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="487e9-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="487e9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="487e9-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="487e9-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="487e9-110">*плигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="487e9-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="487e9-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="487e9-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="487e9-112">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , описывающую расположение источника освещения.</span><span class="sxs-lookup"><span data-stu-id="487e9-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="487e9-113">*пплане* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="487e9-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="487e9-114">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="487e9-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="487e9-115">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="487e9-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="487e9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="487e9-116">Return value</span></span>

<span data-ttu-id="487e9-117">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="487e9-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="487e9-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая выполняет сведение геометрии в плоскость.</span><span class="sxs-lookup"><span data-stu-id="487e9-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="487e9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="487e9-119">Remarks</span></span>

<span data-ttu-id="487e9-120">Функция **D3DXMatrixShadow** выполняет сведение геометрии в плоскость, как при приведении тени от светлой.</span><span class="sxs-lookup"><span data-stu-id="487e9-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="487e9-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="487e9-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="487e9-122">Таким образом, функция **D3DXMatrixShadow** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="487e9-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="487e9-123">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="487e9-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="487e9-124">Если компонент w-component имеет значение 0, луч от начала до светлого цвета представляет направленный источник.</span><span class="sxs-lookup"><span data-stu-id="487e9-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="487e9-125">Если значение равно 1, то светлой является точечным.</span><span class="sxs-lookup"><span data-stu-id="487e9-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="487e9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="487e9-126">Requirements</span></span>



| <span data-ttu-id="487e9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="487e9-127">Requirement</span></span> | <span data-ttu-id="487e9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="487e9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="487e9-129">Header</span><span class="sxs-lookup"><span data-stu-id="487e9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="487e9-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="487e9-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="487e9-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="487e9-131">Library</span></span><br/> | <dl> <span data-ttu-id="487e9-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="487e9-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="487e9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="487e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487e9-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="487e9-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




