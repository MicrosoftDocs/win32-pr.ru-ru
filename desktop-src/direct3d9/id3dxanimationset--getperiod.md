---
description: Возвращает период набора анимации.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Метод ID3DXAnimationSet:: period (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694325"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="6bdf0-103">Метод ID3DXAnimationSet:: period</span><span class="sxs-lookup"><span data-stu-id="6bdf0-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="6bdf0-104">Возвращает период набора анимации.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bdf0-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="6bdf0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bdf0-106">Parameters</span></span>

<span data-ttu-id="6bdf0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bdf0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bdf0-108">Return value</span></span>

<span data-ttu-id="6bdf0-109">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bdf0-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bdf0-110">Период набора анимации.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bdf0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bdf0-111">Remarks</span></span>

<span data-ttu-id="6bdf0-112">Период — это диапазон времени, в течение которого действуют ключевые кадры анимации.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="6bdf0-113">Для циклических анимаций это период цикла.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="6bdf0-114">Единицы времени, в которых указаны ключевые кадры (например, секунды), определяются приложением.</span><span class="sxs-lookup"><span data-stu-id="6bdf0-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdf0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6bdf0-115">Requirements</span></span>



| <span data-ttu-id="6bdf0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6bdf0-116">Requirement</span></span> | <span data-ttu-id="6bdf0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6bdf0-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdf0-118">Header</span><span class="sxs-lookup"><span data-stu-id="6bdf0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6bdf0-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bdf0-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6bdf0-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6bdf0-120">Library</span></span><br/> | <dl> <span data-ttu-id="6bdf0-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bdf0-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6bdf0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bdf0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bdf0-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="6bdf0-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
