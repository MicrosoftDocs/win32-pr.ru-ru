---
description: 'ID3DXMATRIXStack: метод:P тельную (D3DX10. h) — добавляет матрицу в стек.'
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: 'ID3DXMATRIXStack: метод:P тельную (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c248fdaed8235c383388a52172021921e2c78d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107921"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="fd9df-103">ID3DXMATRIXStack: метод:P тельную (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="fd9df-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="fd9df-104">Добавляет матрицу в стек.</span><span class="sxs-lookup"><span data-stu-id="fd9df-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd9df-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="fd9df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd9df-106">Parameters</span></span>

<span data-ttu-id="fd9df-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fd9df-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd9df-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd9df-108">Return value</span></span>

<span data-ttu-id="fd9df-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd9df-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd9df-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd9df-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fd9df-111">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fd9df-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9df-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd9df-112">Remarks</span></span>

<span data-ttu-id="fd9df-113">Этот метод увеличивает число элементов в стеке на 1, повторяя текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="fd9df-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="fd9df-114">Стек будет увеличиваться динамически по мере добавления элементов.</span><span class="sxs-lookup"><span data-stu-id="fd9df-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9df-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fd9df-115">Requirements</span></span>



| <span data-ttu-id="fd9df-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fd9df-116">Requirement</span></span> | <span data-ttu-id="fd9df-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fd9df-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9df-118">Header</span><span class="sxs-lookup"><span data-stu-id="fd9df-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fd9df-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd9df-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd9df-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd9df-120">Library</span></span><br/> | <dl> <span data-ttu-id="fd9df-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd9df-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9df-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fd9df-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9df-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="fd9df-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="fd9df-124">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="fd9df-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




