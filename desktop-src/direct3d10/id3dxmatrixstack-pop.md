---
description: Удаляет текущую матрицу из верхней части стека.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: ID3DXMATRIXStack::P метод op (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714020"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="8e124-103">ID3DXMATRIXStack::P метод op (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="8e124-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="8e124-104">Удаляет текущую матрицу из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="8e124-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e124-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e124-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="8e124-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e124-106">Parameters</span></span>

<span data-ttu-id="8e124-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8e124-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e124-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e124-108">Return value</span></span>

<span data-ttu-id="8e124-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e124-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e124-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8e124-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e124-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e124-111">Remarks</span></span>

<span data-ttu-id="8e124-112">Обратите внимание, что этот метод уменьшает число элементов в стеке на 1, фактически удаляя текущую матрицу из верхней части стека и повышая матрицу до верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="8e124-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="8e124-113">Если текущее число элементов в стеке равно 0, этот метод возвращает данные без выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="8e124-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="8e124-114">Если текущее число элементов в стеке равно 1, то этот метод очищает стек.</span><span class="sxs-lookup"><span data-stu-id="8e124-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e124-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8e124-115">Requirements</span></span>



| <span data-ttu-id="8e124-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8e124-116">Requirement</span></span> | <span data-ttu-id="8e124-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8e124-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e124-118">Header</span><span class="sxs-lookup"><span data-stu-id="8e124-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8e124-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e124-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e124-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e124-120">Library</span></span><br/> | <dl> <span data-ttu-id="8e124-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e124-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e124-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e124-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e124-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8e124-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8e124-124">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="8e124-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




