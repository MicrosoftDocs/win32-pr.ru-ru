---
description: Задает вес записи. Вес используется для определения способа смешения нескольких дорожек.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'Метод ID3DXAnimationController:: Сеттракквеигхт (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821508"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="2a315-104">Метод ID3DXAnimationController:: Сеттракквеигхт</span><span class="sxs-lookup"><span data-stu-id="2a315-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="2a315-105">Задает вес записи.</span><span class="sxs-lookup"><span data-stu-id="2a315-105">Sets the track weight.</span></span> <span data-ttu-id="2a315-106">Вес используется для определения способа смешения нескольких дорожек.</span><span class="sxs-lookup"><span data-stu-id="2a315-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a315-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a315-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="2a315-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a315-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a315-109">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a315-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a315-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a315-111">Идентификатор записи, для которой нужно задать весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="2a315-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="2a315-112">*Вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a315-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a315-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a315-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a315-114">Значение веса.</span><span class="sxs-lookup"><span data-stu-id="2a315-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a315-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a315-115">Return value</span></span>

<span data-ttu-id="2a315-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a315-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a315-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2a315-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a315-118">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2a315-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a315-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2a315-119">Requirements</span></span>



| <span data-ttu-id="2a315-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2a315-120">Requirement</span></span> | <span data-ttu-id="2a315-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2a315-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a315-122">Header</span><span class="sxs-lookup"><span data-stu-id="2a315-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2a315-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a315-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2a315-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a315-124">Library</span></span><br/> | <dl> <span data-ttu-id="2a315-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a315-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a315-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a315-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a315-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2a315-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
