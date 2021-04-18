---
description: Задает ключ события, который изменяет вес анимированной анимации. Вес используется как множитель при объединении нескольких дорожек.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'Метод ID3DXAnimationController:: Кэйтракквеигхт (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713896"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="511a6-103">Метод ID3DXAnimationController:: Кэйтракквеигхт</span><span class="sxs-lookup"><span data-stu-id="511a6-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="511a6-104">Задает ключ события, который изменяет вес анимированной анимации. Вес используется как множитель при объединении нескольких дорожек.</span><span class="sxs-lookup"><span data-stu-id="511a6-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="511a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="511a6-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="511a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="511a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511a6-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="511a6-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="511a6-109">Идентификатор изменяемой записи.</span><span class="sxs-lookup"><span data-stu-id="511a6-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-110">*Неввеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="511a6-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="511a6-112">Новый вес курса.</span><span class="sxs-lookup"><span data-stu-id="511a6-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-113">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="511a6-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-114">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="511a6-115">Глобальный ключ времени.</span><span class="sxs-lookup"><span data-stu-id="511a6-115">Global time key.</span></span> <span data-ttu-id="511a6-116">Указывает глобальное время, в которое будет происходить изменение.</span><span class="sxs-lookup"><span data-stu-id="511a6-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-117">*Длительность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="511a6-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-118">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="511a6-119">Время перехода, которое указывает, как долго будет выполняться плавное преобразование.</span><span class="sxs-lookup"><span data-stu-id="511a6-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="511a6-120">*Переход* \[ на окне\]</span><span class="sxs-lookup"><span data-stu-id="511a6-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="511a6-121">Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="511a6-122">Указывает тип перехода, используемый для перехода между весовыми коэффициентами.</span><span class="sxs-lookup"><span data-stu-id="511a6-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="511a6-123">См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="511a6-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511a6-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="511a6-124">Return value</span></span>

<span data-ttu-id="511a6-125">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="511a6-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="511a6-126">Обработчик события с приоритетом события Blend.</span><span class="sxs-lookup"><span data-stu-id="511a6-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="511a6-127">Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.</span><span class="sxs-lookup"><span data-stu-id="511a6-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="511a6-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="511a6-128">Remarks</span></span>

<span data-ttu-id="511a6-129">Вес используется в качестве множителя для определения того, какую часть этой дорожки следует объединить с другими дорожками.</span><span class="sxs-lookup"><span data-stu-id="511a6-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="511a6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="511a6-130">Requirements</span></span>



| <span data-ttu-id="511a6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="511a6-131">Requirement</span></span> | <span data-ttu-id="511a6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="511a6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="511a6-133">Header</span><span class="sxs-lookup"><span data-stu-id="511a6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="511a6-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="511a6-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="511a6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="511a6-135">Library</span></span><br/> | <dl> <span data-ttu-id="511a6-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="511a6-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="511a6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="511a6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511a6-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="511a6-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
