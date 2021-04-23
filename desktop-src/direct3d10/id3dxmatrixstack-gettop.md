---
description: Извлекает текущую матрицу в верхней части стека.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'Метод ID3DXMATRIXStack:: GetTop (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704011"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="0ee20-103">Метод ID3DXMATRIXStack:: GetTop (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="0ee20-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="0ee20-104">Извлекает текущую матрицу в верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="0ee20-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee20-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="0ee20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ee20-106">Parameters</span></span>

<span data-ttu-id="0ee20-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ee20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ee20-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ee20-108">Return value</span></span>

<span data-ttu-id="0ee20-109">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ee20-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0ee20-110">Этот метод возвращает указатель на структуру D3DXMATRIX, представляющую текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="0ee20-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee20-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ee20-111">Remarks</span></span>

<span data-ttu-id="0ee20-112">Указатель D3DXMATRIX, возвращаемый этим методом, не обязательно должен быть допустимым после последующих операций с стеком.</span><span class="sxs-lookup"><span data-stu-id="0ee20-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="0ee20-113">Обратите внимание, что этот метод не удаляет текущую матрицу из верхней части стека; Вместо этого он просто возвращает текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="0ee20-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee20-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee20-114">Requirements</span></span>



| <span data-ttu-id="0ee20-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee20-115">Requirement</span></span> | <span data-ttu-id="0ee20-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee20-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee20-117">Header</span><span class="sxs-lookup"><span data-stu-id="0ee20-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0ee20-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee20-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ee20-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ee20-119">Library</span></span><br/> | <dl> <span data-ttu-id="0ee20-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ee20-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee20-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee20-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="0ee20-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0ee20-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="0ee20-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
