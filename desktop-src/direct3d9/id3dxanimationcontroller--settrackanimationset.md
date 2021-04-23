---
description: Применяет набор анимации к указанной дорожке.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Метод ID3DXAnimationController:: Сеттракканиматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713889"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="2d9bb-103">Метод ID3DXAnimationController:: Сеттракканиматионсет</span><span class="sxs-lookup"><span data-stu-id="2d9bb-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="2d9bb-104">Применяет набор анимации к указанной дорожке.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d9bb-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="2d9bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d9bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d9bb-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d9bb-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d9bb-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d9bb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d9bb-109">Идентификатор курса, к которому применяется набор анимации.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="2d9bb-110">*панимсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d9bb-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d9bb-111">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="2d9bb-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="2d9bb-112">Указатель на набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) , который должен быть добавлен к дорожке.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d9bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d9bb-113">Return value</span></span>

<span data-ttu-id="2d9bb-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d9bb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d9bb-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2d9bb-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2d9bb-116">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d9bb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d9bb-117">Remarks</span></span>

<span data-ttu-id="2d9bb-118">Этот метод задает для набора анимации заданную запись для смешения.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="2d9bb-119">Набор анимации для каждой записи смешивается в соответствии с толщиной и скоростью записи при вызове [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9bb-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d9bb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2d9bb-120">Requirements</span></span>



| <span data-ttu-id="2d9bb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2d9bb-121">Requirement</span></span> | <span data-ttu-id="2d9bb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2d9bb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9bb-123">Header</span><span class="sxs-lookup"><span data-stu-id="2d9bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2d9bb-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d9bb-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2d9bb-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d9bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="2d9bb-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d9bb-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d9bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d9bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9bb-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2d9bb-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
