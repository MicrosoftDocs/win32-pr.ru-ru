---
description: Задает ключ события, который изменяет частоту воспроизведения анимированной записи.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Метод ID3DXAnimationController:: Кэйтраккспид (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704003"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="4580f-103">Метод ID3DXAnimationController:: Кэйтраккспид</span><span class="sxs-lookup"><span data-stu-id="4580f-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="4580f-104">Задает ключ события, который изменяет частоту воспроизведения анимированной записи.</span><span class="sxs-lookup"><span data-stu-id="4580f-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="4580f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4580f-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="4580f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4580f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4580f-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580f-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580f-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580f-109">Идентификатор изменяемой записи.</span><span class="sxs-lookup"><span data-stu-id="4580f-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="4580f-110">*Невспид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580f-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580f-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580f-112">Новая скорость анимации.</span><span class="sxs-lookup"><span data-stu-id="4580f-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="4580f-113">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580f-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580f-114">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580f-115">Глобальный ключ времени.</span><span class="sxs-lookup"><span data-stu-id="4580f-115">Global time key.</span></span> <span data-ttu-id="4580f-116">Указывает глобальное время, в которое будет происходить изменение.</span><span class="sxs-lookup"><span data-stu-id="4580f-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="4580f-117">*Длительность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580f-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580f-118">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580f-119">Время перехода, которое указывает, как долго будет выполняться плавное преобразование.</span><span class="sxs-lookup"><span data-stu-id="4580f-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="4580f-120">*Переход* \[ на окне\]</span><span class="sxs-lookup"><span data-stu-id="4580f-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580f-121">Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="4580f-122">Указывает тип перехода, используемый для перехода между скоростями.</span><span class="sxs-lookup"><span data-stu-id="4580f-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="4580f-123">См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="4580f-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4580f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4580f-124">Return value</span></span>

<span data-ttu-id="4580f-125">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="4580f-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="4580f-126">Обработчик события с приоритетом события Blend.</span><span class="sxs-lookup"><span data-stu-id="4580f-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="4580f-127">Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.</span><span class="sxs-lookup"><span data-stu-id="4580f-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="4580f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4580f-128">Requirements</span></span>



| <span data-ttu-id="4580f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4580f-129">Requirement</span></span> | <span data-ttu-id="4580f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4580f-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4580f-131">Header</span><span class="sxs-lookup"><span data-stu-id="4580f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4580f-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4580f-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4580f-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4580f-133">Library</span></span><br/> | <dl> <span data-ttu-id="4580f-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4580f-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4580f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4580f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4580f-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4580f-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
