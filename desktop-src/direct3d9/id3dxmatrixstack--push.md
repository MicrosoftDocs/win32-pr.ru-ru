---
description: Добавляет матрицу в стек.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: 'ID3DXMATRIXStack: метод:P тельную (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1678ad9481a7c76fdb0e92a0c3b2de66d638de71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713552"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="28279-103">ID3DXMATRIXStack: метод:P тельную (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="28279-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="28279-104">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="28279-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="28279-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28279-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="28279-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28279-106">Parameters</span></span>

<span data-ttu-id="28279-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="28279-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28279-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28279-108">Return value</span></span>

<span data-ttu-id="28279-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28279-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28279-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="28279-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="28279-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="28279-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="28279-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28279-112">Remarks</span></span>

<span data-ttu-id="28279-113">Этот метод увеличивает число элементов в стеке на 1, повторяя текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="28279-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="28279-114">Стек будет увеличиваться динамически по мере добавления элементов.</span><span class="sxs-lookup"><span data-stu-id="28279-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="28279-115">Требования</span><span class="sxs-lookup"><span data-stu-id="28279-115">Requirements</span></span>



| <span data-ttu-id="28279-116">Требование</span><span class="sxs-lookup"><span data-stu-id="28279-116">Requirement</span></span> | <span data-ttu-id="28279-117">Значение</span><span class="sxs-lookup"><span data-stu-id="28279-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28279-118">Header</span><span class="sxs-lookup"><span data-stu-id="28279-118">Header</span></span><br/>  | <dl> <span data-ttu-id="28279-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28279-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28279-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28279-120">Library</span></span><br/> | <dl> <span data-ttu-id="28279-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28279-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28279-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28279-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28279-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="28279-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="28279-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="28279-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="28279-125">**ID3DXMATRIXStack::P Op**</span><span class="sxs-lookup"><span data-stu-id="28279-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




