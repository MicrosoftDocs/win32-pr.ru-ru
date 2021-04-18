---
description: Задает весовой коэффициент смешения, используемый контроллером анимации.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'Метод ID3DXAnimationController:: Сетприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713890"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="c1e95-103">Метод ID3DXAnimationController:: Сетприоритибленд</span><span class="sxs-lookup"><span data-stu-id="c1e95-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="c1e95-104">Задает весовой коэффициент смешения, используемый контроллером анимации.</span><span class="sxs-lookup"><span data-stu-id="c1e95-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1e95-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="c1e95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1e95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e95-107">*Блендвеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1e95-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e95-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1e95-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1e95-109">Приоритет смешения цветов, используемый контроллером анимации.</span><span class="sxs-lookup"><span data-stu-id="c1e95-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e95-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1e95-110">Return value</span></span>

<span data-ttu-id="c1e95-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1e95-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1e95-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c1e95-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c1e95-113">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c1e95-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e95-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1e95-114">Remarks</span></span>

<span data-ttu-id="c1e95-115">Вес смешения используется для одновременного смешения дорожек высокого и низкого приоритета.</span><span class="sxs-lookup"><span data-stu-id="c1e95-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e95-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c1e95-116">Requirements</span></span>



| <span data-ttu-id="c1e95-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c1e95-117">Requirement</span></span> | <span data-ttu-id="c1e95-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c1e95-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e95-119">Header</span><span class="sxs-lookup"><span data-stu-id="c1e95-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c1e95-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e95-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c1e95-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1e95-121">Library</span></span><br/> | <dl> <span data-ttu-id="c1e95-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1e95-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1e95-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1e95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e95-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c1e95-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="c1e95-125">**жетприоритибленд**</span><span class="sxs-lookup"><span data-stu-id="c1e95-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
