---
description: Возвращает глобальное время анимации.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: Метод ID3DXAnimationController::-Time (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703873"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="91621-103">Метод ID3DXAnimationController:: OnTime</span><span class="sxs-lookup"><span data-stu-id="91621-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="91621-104">Возвращает глобальное время анимации.</span><span class="sxs-lookup"><span data-stu-id="91621-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="91621-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91621-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="91621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91621-106">Parameters</span></span>

<span data-ttu-id="91621-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="91621-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91621-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91621-108">Return value</span></span>

<span data-ttu-id="91621-109">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91621-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91621-110">Возвращает глобальное время анимации.</span><span class="sxs-lookup"><span data-stu-id="91621-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="91621-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91621-111">Remarks</span></span>

<span data-ttu-id="91621-112">Анимации разрабатываются с использованием местного времени анимации и смешиваются в глобальном времени с помощью [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="91621-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91621-113">Требования</span><span class="sxs-lookup"><span data-stu-id="91621-113">Requirements</span></span>



| <span data-ttu-id="91621-114">Требование</span><span class="sxs-lookup"><span data-stu-id="91621-114">Requirement</span></span> | <span data-ttu-id="91621-115">Значение</span><span class="sxs-lookup"><span data-stu-id="91621-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91621-116">Header</span><span class="sxs-lookup"><span data-stu-id="91621-116">Header</span></span><br/>  | <dl> <span data-ttu-id="91621-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="91621-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="91621-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91621-118">Library</span></span><br/> | <dl> <span data-ttu-id="91621-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91621-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91621-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91621-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91621-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="91621-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
