---
description: ID3DXMATRIXStack::P метод op (D3dx9math. h) — удаляет текущую матрицу из верхней части стека.
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: ID3DXMATRIXStack::P метод op (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093510"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="d077d-103">ID3DXMATRIXStack::P метод op (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d077d-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="d077d-104">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="d077d-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d077d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d077d-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="d077d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d077d-106">Parameters</span></span>

<span data-ttu-id="d077d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d077d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d077d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d077d-108">Return value</span></span>

<span data-ttu-id="d077d-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d077d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d077d-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d077d-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d077d-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d077d-111">Remarks</span></span>

<span data-ttu-id="d077d-112">Обратите внимание, что этот метод уменьшает число элементов в стеке на 1, фактически удаляя текущую матрицу из верхней части стека и повышая матрицу до верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="d077d-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="d077d-113">Если текущее число элементов в стеке равно 0, этот метод возвращает данные без выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="d077d-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="d077d-114">Если текущее число элементов в стеке равно 1, то этот метод очищает стек.</span><span class="sxs-lookup"><span data-stu-id="d077d-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="d077d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d077d-115">Requirements</span></span>



| <span data-ttu-id="d077d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d077d-116">Requirement</span></span> | <span data-ttu-id="d077d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d077d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d077d-118">Header</span><span class="sxs-lookup"><span data-stu-id="d077d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d077d-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d077d-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d077d-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d077d-120">Library</span></span><br/> | <dl> <span data-ttu-id="d077d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d077d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d077d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d077d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d077d-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d077d-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d077d-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="d077d-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="d077d-125">**ID3DXMATRIXStack::P тельную**</span><span class="sxs-lookup"><span data-stu-id="d077d-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




