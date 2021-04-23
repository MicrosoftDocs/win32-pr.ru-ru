---
description: Возвращает обработчик события для следующего приоритетного события Blend, которое было запланировано после указанного события.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Метод ID3DXAnimationController:: Жетупкомингприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424322"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="85f66-103">Метод ID3DXAnimationController:: Жетупкомингприоритибленд</span><span class="sxs-lookup"><span data-stu-id="85f66-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="85f66-104">Возвращает обработчик события для следующего приоритетного события Blend, которое было запланировано после указанного события.</span><span class="sxs-lookup"><span data-stu-id="85f66-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f66-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85f66-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="85f66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f66-107">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85f66-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-108">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="85f66-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="85f66-109">Обработчик событий для указанного события, после которого будет осуществляться поиск следующего события с приоритетом Blend.</span><span class="sxs-lookup"><span data-stu-id="85f66-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="85f66-110">Если задано **значение NULL**, метод вернет следующее запланированное событие смешения приоритета.</span><span class="sxs-lookup"><span data-stu-id="85f66-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f66-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85f66-111">Return value</span></span>

<span data-ttu-id="85f66-112">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="85f66-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="85f66-113">Обработчик события для следующего запланированного события смешения приоритета.</span><span class="sxs-lookup"><span data-stu-id="85f66-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="85f66-114">Если не запланировано новое событие смешения приоритета, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="85f66-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f66-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85f66-115">Remarks</span></span>

<span data-ttu-id="85f66-116">Этот метод можно использовать итеративно для нахождения требуемого события смешения приоритета путем многократной передачи **значения NULL** для Хевент.</span><span class="sxs-lookup"><span data-stu-id="85f66-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="85f66-117">Не переполняйте дальнейшие действия после того, как метод возвращал **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="85f66-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85f66-118">Требования</span><span class="sxs-lookup"><span data-stu-id="85f66-118">Requirements</span></span>



| <span data-ttu-id="85f66-119">Требование</span><span class="sxs-lookup"><span data-stu-id="85f66-119">Requirement</span></span> | <span data-ttu-id="85f66-120">Значение</span><span class="sxs-lookup"><span data-stu-id="85f66-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85f66-121">Header</span><span class="sxs-lookup"><span data-stu-id="85f66-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85f66-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f66-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="85f66-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85f66-123">Library</span></span><br/> | <dl> <span data-ttu-id="85f66-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85f66-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85f66-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85f66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f66-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="85f66-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




