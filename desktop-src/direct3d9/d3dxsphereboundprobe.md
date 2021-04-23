---
description: Определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Функция D3DXSphereBoundProbe (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674695"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="adc6c-103">Функция D3DXSphereBoundProbe (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="adc6c-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="adc6c-104">Определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.</span><span class="sxs-lookup"><span data-stu-id="adc6c-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adc6c-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="adc6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adc6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc6c-107">*пцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adc6c-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="adc6c-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="adc6c-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая центральную координату сферы.</span><span class="sxs-lookup"><span data-stu-id="adc6c-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-110">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adc6c-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="adc6c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="adc6c-112">Радиус сферы.</span><span class="sxs-lookup"><span data-stu-id="adc6c-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-113">*прайпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adc6c-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="adc6c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="adc6c-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая координату начала луча.</span><span class="sxs-lookup"><span data-stu-id="adc6c-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="adc6c-116">*прайдиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="adc6c-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc6c-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="adc6c-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="adc6c-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="adc6c-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="adc6c-119">Этот вектор не должен быть (0, 0, 0), но не требует нормализации.</span><span class="sxs-lookup"><span data-stu-id="adc6c-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc6c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adc6c-120">Return value</span></span>

<span data-ttu-id="adc6c-121">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="adc6c-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="adc6c-122">Возвращает **значение true** , если луч пересекает объем ограничивающего прямоугольника сферы.</span><span class="sxs-lookup"><span data-stu-id="adc6c-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="adc6c-123">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="adc6c-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="adc6c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adc6c-124">Remarks</span></span>

<span data-ttu-id="adc6c-125">**D3DXSphereBoundProbe** определяет, пересекает ли луч объем ограничивающего прямоугольника сферы, а не только поверхность сферы.</span><span class="sxs-lookup"><span data-stu-id="adc6c-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc6c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="adc6c-126">Requirements</span></span>



| <span data-ttu-id="adc6c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="adc6c-127">Requirement</span></span> | <span data-ttu-id="adc6c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="adc6c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adc6c-129">Header</span><span class="sxs-lookup"><span data-stu-id="adc6c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="adc6c-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc6c-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="adc6c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="adc6c-131">Library</span></span><br/> | <dl> <span data-ttu-id="adc6c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adc6c-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="adc6c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adc6c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc6c-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="adc6c-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
