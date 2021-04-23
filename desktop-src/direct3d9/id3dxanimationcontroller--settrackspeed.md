---
description: Задает скорость записи. Скорость записи аналогична множителю, который используется для ускорения или снижения скорости воспроизведения.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'Метод ID3DXAnimationController:: Сеттраккспид (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355953"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="be561-104">Метод ID3DXAnimationController:: Сеттраккспид</span><span class="sxs-lookup"><span data-stu-id="be561-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="be561-105">Задает скорость записи.</span><span class="sxs-lookup"><span data-stu-id="be561-105">Sets the track speed.</span></span> <span data-ttu-id="be561-106">Скорость записи аналогична множителю, который используется для ускорения или снижения скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="be561-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="be561-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be561-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="be561-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be561-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be561-109">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be561-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be561-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be561-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be561-111">Идентификатор записи, для которой задается скорость.</span><span class="sxs-lookup"><span data-stu-id="be561-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="be561-112">*Скорость передачи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be561-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be561-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be561-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be561-114">Новая скорость.</span><span class="sxs-lookup"><span data-stu-id="be561-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be561-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be561-115">Return value</span></span>

<span data-ttu-id="be561-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be561-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be561-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="be561-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be561-118">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be561-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="be561-119">Требования</span><span class="sxs-lookup"><span data-stu-id="be561-119">Requirements</span></span>



| <span data-ttu-id="be561-120">Требование</span><span class="sxs-lookup"><span data-stu-id="be561-120">Requirement</span></span> | <span data-ttu-id="be561-121">Значение</span><span class="sxs-lookup"><span data-stu-id="be561-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be561-122">Header</span><span class="sxs-lookup"><span data-stu-id="be561-122">Header</span></span><br/>  | <dl> <span data-ttu-id="be561-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="be561-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="be561-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be561-124">Library</span></span><br/> | <dl> <span data-ttu-id="be561-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be561-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be561-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be561-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be561-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="be561-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
