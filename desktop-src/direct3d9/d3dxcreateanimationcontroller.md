---
description: Создает объект контроллера анимации.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Функция D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703774"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="d87e2-103">Функция D3DXCreateAnimationController</span><span class="sxs-lookup"><span data-stu-id="d87e2-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="d87e2-104">Создает объект контроллера анимации.</span><span class="sxs-lookup"><span data-stu-id="d87e2-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d87e2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="d87e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d87e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d87e2-107">*Макснуманиматионаутпутс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d87e2-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87e2-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87e2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87e2-109">Максимальное число выводов анимации, которые может поддерживать контроллер.</span><span class="sxs-lookup"><span data-stu-id="d87e2-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="d87e2-110">*Макснуманиматионсетс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d87e2-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87e2-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87e2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87e2-112">Максимальное количество наборов анимации, которые могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="d87e2-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="d87e2-113">*Макснумтраккс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d87e2-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87e2-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87e2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87e2-115">Максимальное количество наборов анимации, которые можно одновременно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="d87e2-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="d87e2-116">*Макснумевентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d87e2-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87e2-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87e2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87e2-118">Максимальное число необработанных событий, которые будут поддерживаться контроллером.</span><span class="sxs-lookup"><span data-stu-id="d87e2-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="d87e2-119">*ппанимконтроллер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d87e2-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d87e2-120">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="d87e2-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="d87e2-121">Указатель на созданный объект контроллера анимации.</span><span class="sxs-lookup"><span data-stu-id="d87e2-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="d87e2-122">См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="d87e2-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d87e2-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d87e2-123">Return value</span></span>

<span data-ttu-id="d87e2-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d87e2-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d87e2-125">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d87e2-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d87e2-126">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d87e2-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d87e2-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d87e2-127">Remarks</span></span>

<span data-ttu-id="d87e2-128">Контроллер анимации управляет микшером анимации.</span><span class="sxs-lookup"><span data-stu-id="d87e2-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="d87e2-129">Контроллер добавляет методы для изменения параметров смешения с течением времени, чтобы обеспечить плавные переходы.</span><span class="sxs-lookup"><span data-stu-id="d87e2-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87e2-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d87e2-130">Requirements</span></span>



| <span data-ttu-id="d87e2-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d87e2-131">Requirement</span></span> | <span data-ttu-id="d87e2-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d87e2-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d87e2-133">Header</span><span class="sxs-lookup"><span data-stu-id="d87e2-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d87e2-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d87e2-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d87e2-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d87e2-135">Library</span></span><br/> | <dl> <span data-ttu-id="d87e2-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d87e2-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d87e2-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d87e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87e2-138">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="d87e2-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
