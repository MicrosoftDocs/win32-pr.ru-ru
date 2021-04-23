---
description: Получает текущий приоритет смешения цветов, используемый контроллером анимации.
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: 'Метод ID3DXAnimationController:: Жетприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c27e4c6d2cc706b30f2be99030e7bb4a5bccf209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720925"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a><span data-ttu-id="9dd78-103">Метод ID3DXAnimationController:: Жетприоритибленд</span><span class="sxs-lookup"><span data-stu-id="9dd78-103">ID3DXAnimationController::GetPriorityBlend method</span></span>

<span data-ttu-id="9dd78-104">Получает текущий приоритет смешения цветов, используемый контроллером анимации.</span><span class="sxs-lookup"><span data-stu-id="9dd78-104">Gets the current priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd78-105">Syntax</span></span>


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="9dd78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd78-106">Parameters</span></span>

<span data-ttu-id="9dd78-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9dd78-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9dd78-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dd78-108">Return value</span></span>

<span data-ttu-id="9dd78-109">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dd78-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dd78-110">Возвращает коэффициент смешения текущего приоритета.</span><span class="sxs-lookup"><span data-stu-id="9dd78-110">Returns the current priority blending weight.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd78-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9dd78-111">Remarks</span></span>

<span data-ttu-id="9dd78-112">Коэффициент смешения приоритетов используется для объединения дорожек высокого и низкого приоритета.</span><span class="sxs-lookup"><span data-stu-id="9dd78-112">The priority blending weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd78-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9dd78-113">Requirements</span></span>



| <span data-ttu-id="9dd78-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9dd78-114">Requirement</span></span> | <span data-ttu-id="9dd78-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9dd78-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd78-116">Header</span><span class="sxs-lookup"><span data-stu-id="9dd78-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9dd78-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd78-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9dd78-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9dd78-118">Library</span></span><br/> | <dl> <span data-ttu-id="9dd78-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dd78-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9dd78-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dd78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd78-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="9dd78-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="9dd78-122">**сетприоритибленд**</span><span class="sxs-lookup"><span data-stu-id="9dd78-122">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
