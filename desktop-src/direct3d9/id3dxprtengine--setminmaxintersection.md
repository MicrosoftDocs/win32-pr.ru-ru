---
description: Устанавливает минимальное и максимальное расстояние пересечения между трехмерными объектами.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Метод ID3DXPRTEngine:: Сетминмаксинтерсектион (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355150"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="19552-103">Метод ID3DXPRTEngine:: Сетминмаксинтерсектион</span><span class="sxs-lookup"><span data-stu-id="19552-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="19552-104">Устанавливает минимальное и максимальное расстояние пересечения между трехмерными объектами.</span><span class="sxs-lookup"><span data-stu-id="19552-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="19552-105">Эти значения расстояния можно использовать для управления минимальным или максимальным расстоянием, в течение которых объекты могут быть темными или отражать освещение.</span><span class="sxs-lookup"><span data-stu-id="19552-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="19552-106">Например, метод можно использовать для ограничения затенения ближайших функций трехмерной модели.</span><span class="sxs-lookup"><span data-stu-id="19552-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="19552-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19552-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="19552-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="19552-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19552-109">*фмин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19552-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19552-110">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19552-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19552-111">Минимальное расстояние пересечения.</span><span class="sxs-lookup"><span data-stu-id="19552-111">Minimum intersection distance.</span></span> <span data-ttu-id="19552-112">Должно быть положительным и меньшим, чем fMax.</span><span class="sxs-lookup"><span data-stu-id="19552-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="19552-113">*fMax* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19552-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19552-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19552-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19552-115">Максимальное расстояние пересечения.</span><span class="sxs-lookup"><span data-stu-id="19552-115">Maximum intersection distance.</span></span> <span data-ttu-id="19552-116">Если 0,0 f, будет использоваться предыдущее значение; в противном случае должен быть больше Фмин.</span><span class="sxs-lookup"><span data-stu-id="19552-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19552-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19552-117">Return value</span></span>

<span data-ttu-id="19552-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19552-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19552-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="19552-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19552-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19552-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="19552-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19552-121">Remarks</span></span>

<span data-ttu-id="19552-122">Этот метод не может использоваться в моделировании предварительно вычисленных радианценых передач (PRT), которые выполняются в GPU.</span><span class="sxs-lookup"><span data-stu-id="19552-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="19552-123">См. раздел [**ID3DXPRTEngine:: компутедиректлигхтингшгпу**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="19552-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19552-124">Требования</span><span class="sxs-lookup"><span data-stu-id="19552-124">Requirements</span></span>



| <span data-ttu-id="19552-125">Требование</span><span class="sxs-lookup"><span data-stu-id="19552-125">Requirement</span></span> | <span data-ttu-id="19552-126">Значение</span><span class="sxs-lookup"><span data-stu-id="19552-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19552-127">Header</span><span class="sxs-lookup"><span data-stu-id="19552-127">Header</span></span><br/>  | <dl> <span data-ttu-id="19552-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="19552-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19552-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="19552-129">Library</span></span><br/> | <dl> <span data-ttu-id="19552-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19552-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19552-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19552-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19552-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="19552-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
