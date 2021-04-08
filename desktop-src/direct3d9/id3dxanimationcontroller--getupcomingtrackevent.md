---
description: Возвращает обработчик события для следующего события, запланированного на выполнение после указанного события в дорожке анимации.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Метод ID3DXAnimationController:: Жетупкомингтраккевент (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000318"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="9848c-103">Метод ID3DXAnimationController:: Жетупкомингтраккевент</span><span class="sxs-lookup"><span data-stu-id="9848c-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="9848c-104">Возвращает обработчик события для следующего события, запланированного на выполнение после указанного события в дорожке анимации.</span><span class="sxs-lookup"><span data-stu-id="9848c-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="9848c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9848c-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="9848c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9848c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9848c-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9848c-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9848c-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9848c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9848c-109">Идентификатор трассировки.</span><span class="sxs-lookup"><span data-stu-id="9848c-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9848c-110">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9848c-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9848c-111">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="9848c-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="9848c-112">Обработчик событий для указанного события, после которого будет осуществляться поиск следующего события.</span><span class="sxs-lookup"><span data-stu-id="9848c-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="9848c-113">Если задано **значение NULL**, метод вернет следующее запланированное событие.</span><span class="sxs-lookup"><span data-stu-id="9848c-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9848c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9848c-114">Return value</span></span>

<span data-ttu-id="9848c-115">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="9848c-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="9848c-116">Обработчик события для следующего события, запланированного для выполнения в указанной дорожке. Если новое событие не запланировано, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="9848c-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="9848c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9848c-117">Remarks</span></span>

<span data-ttu-id="9848c-118">Этот метод можно использовать итеративно для нахождения нужного события путем многократной передачи **значения NULL** для Хевент.</span><span class="sxs-lookup"><span data-stu-id="9848c-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="9848c-119">Не переполняйте дальнейшие действия после того, как метод возвращал **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9848c-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9848c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9848c-120">Requirements</span></span>



| <span data-ttu-id="9848c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9848c-121">Requirement</span></span> | <span data-ttu-id="9848c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9848c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9848c-123">Header</span><span class="sxs-lookup"><span data-stu-id="9848c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9848c-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9848c-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9848c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9848c-125">Library</span></span><br/> | <dl> <span data-ttu-id="9848c-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9848c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9848c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9848c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9848c-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="9848c-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
