---
description: Этот интерфейс инкапсулирует минимальную функциональность, необходимую для набора анимации контроллером анимации.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Интерфейс ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273961"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="24806-103">Интерфейс ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="24806-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="24806-104">Этот интерфейс инкапсулирует минимальную функциональность, необходимую для набора анимации контроллером анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="24806-105">Опытным пользователям может потребоваться реализовать этот интерфейс в соответствии со своими потребностями. Однако большинству пользователей, тем не менее, должны быть достаточно производных интерфейсов [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) и [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="24806-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="24806-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="24806-106">Members</span></span>

<span data-ttu-id="24806-107">Интерфейс **ID3DXAnimationSet** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="24806-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24806-108">**ID3DXAnimationSet** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24806-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="24806-109">Методы</span><span class="sxs-lookup"><span data-stu-id="24806-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24806-110">Методы</span><span class="sxs-lookup"><span data-stu-id="24806-110">Methods</span></span>

<span data-ttu-id="24806-111">Интерфейс **ID3DXAnimationSet** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="24806-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="24806-112">Метод</span><span class="sxs-lookup"><span data-stu-id="24806-112">Method</span></span>                                                                        | <span data-ttu-id="24806-113">Описание</span><span class="sxs-lookup"><span data-stu-id="24806-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="24806-114">**жетаниматиониндексбинаме**</span><span class="sxs-lookup"><span data-stu-id="24806-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="24806-115">Возвращает индекс анимации по ее имени.</span><span class="sxs-lookup"><span data-stu-id="24806-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="24806-116">**жетаниматионнамебиндекс**</span><span class="sxs-lookup"><span data-stu-id="24806-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="24806-117">Возвращает имя анимации по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="24806-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="24806-118">**Метод Callback**</span><span class="sxs-lookup"><span data-stu-id="24806-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="24806-119">Возвращает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="24806-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="24806-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="24806-121">Возвращает имя набора анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="24806-122">**жетнуманиматионс**</span><span class="sxs-lookup"><span data-stu-id="24806-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="24806-123">Возвращает число анимаций в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="24806-124">**Период**</span><span class="sxs-lookup"><span data-stu-id="24806-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="24806-125">Возвращает период набора анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="24806-126">**жетпериодикпоситион**</span><span class="sxs-lookup"><span data-stu-id="24806-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="24806-127">Возвращает значение времени в локальном интервале в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="24806-128">**жетсрт**</span><span class="sxs-lookup"><span data-stu-id="24806-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="24806-129">Возвращает значения масштаба, вращения и перевода набора анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24806-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24806-130">Remarks</span></span>

<span data-ttu-id="24806-131">Набор анимации состоит из анимации для многих узлов в одной и той же анимации.</span><span class="sxs-lookup"><span data-stu-id="24806-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="24806-132">Тип LPD3DXANIMATIONSET определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="24806-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="24806-133">Требования</span><span class="sxs-lookup"><span data-stu-id="24806-133">Requirements</span></span>



| <span data-ttu-id="24806-134">Требование</span><span class="sxs-lookup"><span data-stu-id="24806-134">Requirement</span></span> | <span data-ttu-id="24806-135">Значение</span><span class="sxs-lookup"><span data-stu-id="24806-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24806-136">Header</span><span class="sxs-lookup"><span data-stu-id="24806-136">Header</span></span><br/>  | <dl> <span data-ttu-id="24806-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="24806-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="24806-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24806-138">Library</span></span><br/> | <dl> <span data-ttu-id="24806-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24806-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24806-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24806-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24806-141">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="24806-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
