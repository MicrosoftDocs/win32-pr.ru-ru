---
description: Возвращает число наборов анимации, зарегистрированных в данный момент в контроллере анимации.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Метод ID3DXAnimationController:: Жетнуманиматионсетс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713481"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="e4df3-103">Метод ID3DXAnimationController:: Жетнуманиматионсетс</span><span class="sxs-lookup"><span data-stu-id="e4df3-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="e4df3-104">Возвращает число наборов анимации, зарегистрированных в данный момент в контроллере анимации.</span><span class="sxs-lookup"><span data-stu-id="e4df3-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4df3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4df3-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="e4df3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4df3-106">Parameters</span></span>

<span data-ttu-id="e4df3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e4df3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4df3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4df3-108">Return value</span></span>

<span data-ttu-id="e4df3-109">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4df3-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4df3-110">Количество наборов анимации.</span><span class="sxs-lookup"><span data-stu-id="e4df3-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4df3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4df3-111">Remarks</span></span>

<span data-ttu-id="e4df3-112">Контроллер содержит любое количество наборов и дорожек анимации.</span><span class="sxs-lookup"><span data-stu-id="e4df3-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="e4df3-113">Наборы анимации можно зарегистрировать с помощью [**регистераниматионаутпут**](id3dxanimationcontroller--registeranimationoutput.md).</span><span class="sxs-lookup"><span data-stu-id="e4df3-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="e4df3-114">Контроллер анимации, созданный при вызове [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) , будет автоматически регистрировать загруженные наборы анимации.</span><span class="sxs-lookup"><span data-stu-id="e4df3-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4df3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e4df3-115">Requirements</span></span>



| <span data-ttu-id="e4df3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e4df3-116">Requirement</span></span> | <span data-ttu-id="e4df3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e4df3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4df3-118">Header</span><span class="sxs-lookup"><span data-stu-id="e4df3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e4df3-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4df3-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e4df3-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4df3-120">Library</span></span><br/> | <dl> <span data-ttu-id="e4df3-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4df3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4df3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4df3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4df3-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e4df3-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
