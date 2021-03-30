---
description: Задает смешение ключей событий для указанной записи анимации.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Метод ID3DXAnimationController:: Кэйприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354260"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="d054f-103">Метод ID3DXAnimationController:: Кэйприоритибленд</span><span class="sxs-lookup"><span data-stu-id="d054f-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="d054f-104">Задает смешение ключей событий для указанной записи анимации.</span><span class="sxs-lookup"><span data-stu-id="d054f-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="d054f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d054f-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="d054f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d054f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d054f-107">*Невблендвеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d054f-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d054f-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d054f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d054f-109">Число от 0 до 1, используемое для одновременного смешения дорожек.</span><span class="sxs-lookup"><span data-stu-id="d054f-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="d054f-110">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d054f-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d054f-111">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d054f-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d054f-112">Глобальное время для запуска Blend.</span><span class="sxs-lookup"><span data-stu-id="d054f-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="d054f-113">*Длительность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d054f-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d054f-114">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d054f-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d054f-115">Глобальная длительность смешения времени.</span><span class="sxs-lookup"><span data-stu-id="d054f-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="d054f-116">*Переход* \[ на окне\]</span><span class="sxs-lookup"><span data-stu-id="d054f-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d054f-117">Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d054f-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="d054f-118">Указывает тип перехода, используемый в течение смешения.</span><span class="sxs-lookup"><span data-stu-id="d054f-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="d054f-119">См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="d054f-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d054f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d054f-120">Return value</span></span>

<span data-ttu-id="d054f-121">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="d054f-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="d054f-122">Обработчик события с приоритетом события Blend.</span><span class="sxs-lookup"><span data-stu-id="d054f-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="d054f-123">Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.</span><span class="sxs-lookup"><span data-stu-id="d054f-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="d054f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d054f-124">Remarks</span></span>

<span data-ttu-id="d054f-125">Контроллер анимации смешивается в три этапа: курсы с низким приоритетом смешиваются, сначала накладываются курсы с высоким приоритетом, а затем результаты обеих моделей смешиваются.</span><span class="sxs-lookup"><span data-stu-id="d054f-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="d054f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d054f-126">Requirements</span></span>



| <span data-ttu-id="d054f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d054f-127">Requirement</span></span> | <span data-ttu-id="d054f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d054f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d054f-129">Header</span><span class="sxs-lookup"><span data-stu-id="d054f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d054f-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d054f-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d054f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d054f-131">Library</span></span><br/> | <dl> <span data-ttu-id="d054f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d054f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d054f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d054f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d054f-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d054f-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="d054f-135">**сетприоритибленд**</span><span class="sxs-lookup"><span data-stu-id="d054f-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
