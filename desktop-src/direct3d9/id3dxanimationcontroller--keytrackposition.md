---
description: Задает ключ события, который изменяет местное время анимации.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Метод ID3DXAnimationController:: Кэйтраккпоситион (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355510"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="8c8fd-103">Метод ID3DXAnimationController:: Кэйтраккпоситион</span><span class="sxs-lookup"><span data-stu-id="8c8fd-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="8c8fd-104">Задает ключ события, который изменяет местное время анимации.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c8fd-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="8c8fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c8fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8fd-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c8fd-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8fd-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c8fd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c8fd-109">Идентификатор изменяемой записи.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="8c8fd-110">*Невпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c8fd-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8fd-111">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c8fd-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c8fd-112">Новое местное время в дорожке анимации.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="8c8fd-113">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c8fd-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8fd-114">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c8fd-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c8fd-115">Глобальный ключ времени.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-115">Global time key.</span></span> <span data-ttu-id="8c8fd-116">Указывает глобальное время, в которое будет происходить изменение.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8fd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c8fd-117">Return value</span></span>

<span data-ttu-id="8c8fd-118">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8c8fd-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8c8fd-119">Обработчик события с приоритетом события Blend.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="8c8fd-120">**Значение NULL** возвращается, если трассировка недопустима, или если событие Free недоступно.</span><span class="sxs-lookup"><span data-stu-id="8c8fd-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8fd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8c8fd-121">Requirements</span></span>



| <span data-ttu-id="8c8fd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8c8fd-122">Requirement</span></span> | <span data-ttu-id="8c8fd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8c8fd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8fd-124">Header</span><span class="sxs-lookup"><span data-stu-id="8c8fd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8c8fd-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8fd-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8c8fd-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c8fd-126">Library</span></span><br/> | <dl> <span data-ttu-id="8c8fd-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c8fd-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c8fd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c8fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8fd-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8c8fd-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
