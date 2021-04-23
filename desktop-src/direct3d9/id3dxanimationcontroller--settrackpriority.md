---
description: Задает приоритет смешивания для указанного направления анимации.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Метод ID3DXAnimationController:: Сеттраккприорити (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714013"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="96394-103">Метод ID3DXAnimationController:: Сеттраккприорити</span><span class="sxs-lookup"><span data-stu-id="96394-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="96394-104">Задает приоритет смешивания для указанного направления анимации.</span><span class="sxs-lookup"><span data-stu-id="96394-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="96394-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96394-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="96394-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96394-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96394-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96394-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96394-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96394-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96394-109">Идентификатор трассировки.</span><span class="sxs-lookup"><span data-stu-id="96394-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="96394-110">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96394-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96394-111">Тип: **[ **D3DXPRIORITY \_ тип**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="96394-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="96394-112">Контроль приоритета.</span><span class="sxs-lookup"><span data-stu-id="96394-112">Track priority.</span></span> <span data-ttu-id="96394-113">Этому параметру следует присвоить одну из констант [**\_ типа D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="96394-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96394-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96394-114">Return value</span></span>

<span data-ttu-id="96394-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96394-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96394-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="96394-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="96394-117">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="96394-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="96394-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="96394-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="96394-119">Требования</span><span class="sxs-lookup"><span data-stu-id="96394-119">Requirements</span></span>



| <span data-ttu-id="96394-120">Требование</span><span class="sxs-lookup"><span data-stu-id="96394-120">Requirement</span></span> | <span data-ttu-id="96394-121">Значение</span><span class="sxs-lookup"><span data-stu-id="96394-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96394-122">Header</span><span class="sxs-lookup"><span data-stu-id="96394-122">Header</span></span><br/>  | <dl> <span data-ttu-id="96394-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="96394-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="96394-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96394-124">Library</span></span><br/> | <dl> <span data-ttu-id="96394-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96394-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96394-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96394-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96394-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="96394-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
