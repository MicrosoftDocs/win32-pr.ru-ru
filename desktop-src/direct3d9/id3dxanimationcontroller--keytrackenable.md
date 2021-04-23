---
description: Задает ключ события, который включает или отключает запись анимации.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'Метод ID3DXAnimationController:: Кэйтраккенабле (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354253"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="0de01-103">Метод ID3DXAnimationController:: Кэйтраккенабле</span><span class="sxs-lookup"><span data-stu-id="0de01-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="0de01-104">Задает ключ события, который включает или отключает запись анимации.</span><span class="sxs-lookup"><span data-stu-id="0de01-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0de01-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="0de01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0de01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de01-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0de01-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de01-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0de01-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0de01-109">Идентификатор изменяемой анимации.</span><span class="sxs-lookup"><span data-stu-id="0de01-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="0de01-110">*Невенабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0de01-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de01-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0de01-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0de01-112">Включить флаг.</span><span class="sxs-lookup"><span data-stu-id="0de01-112">Enable flag.</span></span> <span data-ttu-id="0de01-113">Задайте значение **true** , чтобы включить анимацию анимации, или **значение false** , чтобы отключить эту запись.</span><span class="sxs-lookup"><span data-stu-id="0de01-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="0de01-114">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0de01-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de01-115">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0de01-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0de01-116">Глобальный ключ времени.</span><span class="sxs-lookup"><span data-stu-id="0de01-116">Global time key.</span></span> <span data-ttu-id="0de01-117">Указывает глобальное время, в которое будет происходить изменение.</span><span class="sxs-lookup"><span data-stu-id="0de01-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de01-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0de01-118">Return value</span></span>

<span data-ttu-id="0de01-119">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="0de01-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="0de01-120">Обработчик события с приоритетом события Blend.</span><span class="sxs-lookup"><span data-stu-id="0de01-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="0de01-121">Если трассировка недопустима, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0de01-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de01-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0de01-122">Requirements</span></span>



| <span data-ttu-id="0de01-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0de01-123">Requirement</span></span> | <span data-ttu-id="0de01-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0de01-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0de01-125">Header</span><span class="sxs-lookup"><span data-stu-id="0de01-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0de01-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0de01-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0de01-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0de01-127">Library</span></span><br/> | <dl> <span data-ttu-id="0de01-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0de01-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0de01-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0de01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de01-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0de01-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
