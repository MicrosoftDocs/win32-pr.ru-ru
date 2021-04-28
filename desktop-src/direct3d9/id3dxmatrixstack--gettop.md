---
description: 'Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h) — получает текущую матрицу в верхней части стека.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093582"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="b44e5-103">Метод ID3DXMATRIXStack:: GetTop (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b44e5-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="b44e5-104">Извлекает текущую матрицу в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="b44e5-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b44e5-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="b44e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b44e5-106">Parameters</span></span>

<span data-ttu-id="b44e5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b44e5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b44e5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b44e5-108">Return value</span></span>

<span data-ttu-id="b44e5-109">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b44e5-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b44e5-110">Этот метод возвращает указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="b44e5-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b44e5-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b44e5-111">Remarks</span></span>

<span data-ttu-id="b44e5-112">Указатель [**D3DXMATRIX**](d3dxmatrix.md) , возвращаемый этим методом, не обязательно должен быть допустимым после последующих операций с стеком.</span><span class="sxs-lookup"><span data-stu-id="b44e5-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="b44e5-113">Обратите внимание, что этот метод не удаляет текущую матрицу из верхней части стека; Вместо этого он просто возвращает текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="b44e5-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="b44e5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b44e5-114">Requirements</span></span>



| <span data-ttu-id="b44e5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b44e5-115">Requirement</span></span> | <span data-ttu-id="b44e5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b44e5-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b44e5-117">Header</span><span class="sxs-lookup"><span data-stu-id="b44e5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b44e5-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b44e5-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b44e5-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b44e5-119">Library</span></span><br/> | <dl> <span data-ttu-id="b44e5-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b44e5-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b44e5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b44e5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44e5-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="b44e5-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b44e5-123">**ID3DXMATRIXStack::P Op**</span><span class="sxs-lookup"><span data-stu-id="b44e5-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="b44e5-124">**ID3DXMATRIXStack::P тельную**</span><span class="sxs-lookup"><span data-stu-id="b44e5-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




