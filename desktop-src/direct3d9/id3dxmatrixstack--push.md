---
description: 'ID3DXMATRIXStack: метод:P тельную (D3dx9math. h) — добавляет матрицу в стек.'
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
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093511"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="f2434-103">ID3DXMATRIXStack: метод:P тельную (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f2434-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="f2434-104">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="f2434-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2434-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2434-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="f2434-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2434-106">Parameters</span></span>

<span data-ttu-id="f2434-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f2434-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2434-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2434-108">Return value</span></span>

<span data-ttu-id="f2434-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2434-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2434-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f2434-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2434-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f2434-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2434-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2434-112">Remarks</span></span>

<span data-ttu-id="f2434-113">Этот метод увеличивает число элементов в стеке на 1, повторяя текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="f2434-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="f2434-114">Стек будет увеличиваться динамически по мере добавления элементов.</span><span class="sxs-lookup"><span data-stu-id="f2434-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2434-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f2434-115">Requirements</span></span>



| <span data-ttu-id="f2434-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f2434-116">Requirement</span></span> | <span data-ttu-id="f2434-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f2434-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2434-118">Header</span><span class="sxs-lookup"><span data-stu-id="f2434-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f2434-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2434-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2434-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2434-120">Library</span></span><br/> | <dl> <span data-ttu-id="f2434-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2434-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2434-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f2434-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2434-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="f2434-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f2434-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="f2434-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="f2434-125">**ID3DXMATRIXStack::P Op**</span><span class="sxs-lookup"><span data-stu-id="f2434-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




