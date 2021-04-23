---
description: Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой. Обычно используется для определения того, находится ли заданная точка в теневом виде.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Метод ID3DXPRTEngine:: Шадоврайинтерсектс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081885"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="e12dc-104">Метод ID3DXPRTEngine:: Шадоврайинтерсектс</span><span class="sxs-lookup"><span data-stu-id="e12dc-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="e12dc-105">Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой.</span><span class="sxs-lookup"><span data-stu-id="e12dc-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="e12dc-106">Обычно используется для определения того, находится ли заданная точка в теневом виде.</span><span class="sxs-lookup"><span data-stu-id="e12dc-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="e12dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e12dc-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="e12dc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e12dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e12dc-109">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e12dc-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e12dc-110">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e12dc-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e12dc-111">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="e12dc-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="e12dc-112">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e12dc-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e12dc-113">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e12dc-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e12dc-114">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается нормализованное направление луча.</span><span class="sxs-lookup"><span data-stu-id="e12dc-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e12dc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e12dc-115">Return value</span></span>

<span data-ttu-id="e12dc-116">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e12dc-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e12dc-117">Возвращает **значение true** , если луч пересекает текущую сетку; в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e12dc-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e12dc-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e12dc-118">Remarks</span></span>

<span data-ttu-id="e12dc-119">Используйте [**ID3DXPRTEngine:: сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md) , чтобы задать минимальное и максимальное расстояние пересечения с лучом.</span><span class="sxs-lookup"><span data-stu-id="e12dc-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="e12dc-120">Этот метод выполняется быстрее, чем [**ID3DXPRTEngine:: клосестрайинтерсектс**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="e12dc-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e12dc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e12dc-121">Requirements</span></span>



| <span data-ttu-id="e12dc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e12dc-122">Requirement</span></span> | <span data-ttu-id="e12dc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e12dc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e12dc-124">Header</span><span class="sxs-lookup"><span data-stu-id="e12dc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e12dc-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e12dc-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e12dc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e12dc-126">Library</span></span><br/> | <dl> <span data-ttu-id="e12dc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e12dc-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e12dc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e12dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12dc-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e12dc-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e12dc-130">**ID3DXPRTEngine:: Клосестрайинтерсектс**</span><span class="sxs-lookup"><span data-stu-id="e12dc-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="e12dc-131">**ID3DXPRTEngine:: Сетминмаксинтерсектион**</span><span class="sxs-lookup"><span data-stu-id="e12dc-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
