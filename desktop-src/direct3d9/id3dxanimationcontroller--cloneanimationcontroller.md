---
description: Выполняет клонирование или копирование контроллера анимации.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Метод ID3DXAnimationController:: Клонеаниматионконтроллер (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355800"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="bf07f-103">Метод ID3DXAnimationController:: Клонеаниматионконтроллер</span><span class="sxs-lookup"><span data-stu-id="bf07f-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="bf07f-104">Выполняет клонирование или копирование контроллера анимации.</span><span class="sxs-lookup"><span data-stu-id="bf07f-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf07f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf07f-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="bf07f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf07f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf07f-107">*Макснуманиматионаутпутс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf07f-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07f-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf07f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf07f-109">Максимальное число выводов анимации, которые может поддерживать контроллер.</span><span class="sxs-lookup"><span data-stu-id="bf07f-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="bf07f-110">*Макснуманиматионсетс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf07f-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07f-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf07f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf07f-112">Максимальное число наборов анимации, которое может поддерживать контроллер.</span><span class="sxs-lookup"><span data-stu-id="bf07f-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="bf07f-113">*Макснумтраккс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf07f-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07f-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf07f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf07f-115">Максимальное число дорожек, которое может поддерживать контроллер.</span><span class="sxs-lookup"><span data-stu-id="bf07f-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="bf07f-116">*Макснумевентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf07f-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07f-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf07f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf07f-118">Максимальное число событий, которое может поддерживать контроллер.</span><span class="sxs-lookup"><span data-stu-id="bf07f-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="bf07f-119">*ппанимконтроллер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf07f-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf07f-120">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf07f-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="bf07f-121">Адрес указателя на клонированный контроллер анимации [**ID3DXAnimationController**](id3dxanimationcontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="bf07f-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf07f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf07f-122">Return value</span></span>

<span data-ttu-id="bf07f-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf07f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf07f-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="bf07f-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf07f-125">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bf07f-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf07f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bf07f-126">Requirements</span></span>



| <span data-ttu-id="bf07f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bf07f-127">Requirement</span></span> | <span data-ttu-id="bf07f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bf07f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf07f-129">Header</span><span class="sxs-lookup"><span data-stu-id="bf07f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bf07f-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf07f-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bf07f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf07f-131">Library</span></span><br/> | <dl> <span data-ttu-id="bf07f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf07f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf07f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf07f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf07f-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="bf07f-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
