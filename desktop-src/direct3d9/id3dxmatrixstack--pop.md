---
description: Удаляет текущую матрицу из верхней части стека.
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
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081848"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="ab076-103">ID3DXMATRIXStack::P метод op (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ab076-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="ab076-104">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="ab076-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab076-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab076-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="ab076-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab076-106">Parameters</span></span>

<span data-ttu-id="ab076-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ab076-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab076-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab076-108">Return value</span></span>

<span data-ttu-id="ab076-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab076-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab076-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ab076-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab076-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab076-111">Remarks</span></span>

<span data-ttu-id="ab076-112">Обратите внимание, что этот метод уменьшает число элементов в стеке на 1, фактически удаляя текущую матрицу из верхней части стека и повышая матрицу до верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="ab076-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="ab076-113">Если текущее число элементов в стеке равно 0, этот метод возвращает данные без выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="ab076-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="ab076-114">Если текущее число элементов в стеке равно 1, то этот метод очищает стек.</span><span class="sxs-lookup"><span data-stu-id="ab076-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab076-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ab076-115">Requirements</span></span>



| <span data-ttu-id="ab076-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ab076-116">Requirement</span></span> | <span data-ttu-id="ab076-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ab076-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab076-118">Header</span><span class="sxs-lookup"><span data-stu-id="ab076-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ab076-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab076-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab076-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ab076-120">Library</span></span><br/> | <dl> <span data-ttu-id="ab076-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab076-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab076-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab076-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab076-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ab076-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ab076-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="ab076-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="ab076-125">**ID3DXMATRIXStack::P тельную**</span><span class="sxs-lookup"><span data-stu-id="ab076-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




