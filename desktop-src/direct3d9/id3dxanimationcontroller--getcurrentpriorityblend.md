---
description: Возвращает маркер события для события приоритета Blend, выполняющегося в данный момент.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'Метод ID3DXAnimationController:: Жеткуррентприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355793"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="2cd33-103">Метод ID3DXAnimationController:: Жеткуррентприоритибленд</span><span class="sxs-lookup"><span data-stu-id="2cd33-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="2cd33-104">Возвращает маркер события для события приоритета Blend, выполняющегося в данный момент.</span><span class="sxs-lookup"><span data-stu-id="2cd33-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cd33-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="2cd33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cd33-106">Parameters</span></span>

<span data-ttu-id="2cd33-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2cd33-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cd33-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cd33-108">Return value</span></span>

<span data-ttu-id="2cd33-109">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="2cd33-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="2cd33-110">Обработчик событий для текущего выполняемого события смешения приоритетов.</span><span class="sxs-lookup"><span data-stu-id="2cd33-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="2cd33-111">Возвращается **значение NULL** , если в данный момент не выполняется событие приоритета Blend.</span><span class="sxs-lookup"><span data-stu-id="2cd33-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd33-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2cd33-112">Requirements</span></span>



| <span data-ttu-id="2cd33-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2cd33-113">Requirement</span></span> | <span data-ttu-id="2cd33-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2cd33-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd33-115">Header</span><span class="sxs-lookup"><span data-stu-id="2cd33-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2cd33-116"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd33-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2cd33-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2cd33-117">Library</span></span><br/> | <dl> <span data-ttu-id="2cd33-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cd33-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2cd33-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cd33-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd33-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2cd33-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




