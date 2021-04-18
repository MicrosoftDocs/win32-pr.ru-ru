---
description: Возвращает обработчик событий для события, которое в данный момент выполняется в указанной дорожке анимации.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Метод ID3DXAnimationController:: Жеткурренттраккевент (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713855"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="75255-103">Метод ID3DXAnimationController:: Жеткурренттраккевент</span><span class="sxs-lookup"><span data-stu-id="75255-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="75255-104">Возвращает обработчик событий для события, которое в данный момент выполняется в указанной дорожке анимации.</span><span class="sxs-lookup"><span data-stu-id="75255-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="75255-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75255-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="75255-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75255-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75255-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75255-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75255-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75255-109">Идентификатор трассировки.</span><span class="sxs-lookup"><span data-stu-id="75255-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="75255-110">*Тип события* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75255-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75255-111">Тип: **[ **D3DXEVENT \_ тип**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="75255-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="75255-112">Тип события для запроса.</span><span class="sxs-lookup"><span data-stu-id="75255-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75255-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75255-113">Return value</span></span>

<span data-ttu-id="75255-114">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="75255-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="75255-115">Обработчик событий для события, выполняемого в данный момент в указанной дорожке. Если в указанной дорожке не запущена ни одно событие, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="75255-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="75255-116">Требования</span><span class="sxs-lookup"><span data-stu-id="75255-116">Requirements</span></span>



| <span data-ttu-id="75255-117">Требование</span><span class="sxs-lookup"><span data-stu-id="75255-117">Requirement</span></span> | <span data-ttu-id="75255-118">Значение</span><span class="sxs-lookup"><span data-stu-id="75255-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75255-119">Header</span><span class="sxs-lookup"><span data-stu-id="75255-119">Header</span></span><br/>  | <dl> <span data-ttu-id="75255-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="75255-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="75255-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="75255-121">Library</span></span><br/> | <dl> <span data-ttu-id="75255-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75255-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75255-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75255-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75255-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="75255-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
