---
description: Определяет произведение текущей матрицы и заданную матрицу.
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43f80ca26f615e02570f0855b1ba6c2435e11b5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714021"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="b23ef-103">Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b23ef-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="b23ef-104">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="b23ef-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b23ef-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b23ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b23ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23ef-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b23ef-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23ef-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b23ef-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b23ef-109">Указатель на структуру D3DXMATRIX, которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="b23ef-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23ef-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b23ef-110">Return value</span></span>

<span data-ttu-id="b23ef-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b23ef-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b23ef-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b23ef-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b23ef-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b23ef-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b23ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b23ef-114">Remarks</span></span>

<span data-ttu-id="b23ef-115">Этот метод дает право на умножение заданной матрицы в текущую матрицу (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="b23ef-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="b23ef-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="b23ef-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="b23ef-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b23ef-117">Requirements</span></span>



| <span data-ttu-id="b23ef-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b23ef-118">Requirement</span></span> | <span data-ttu-id="b23ef-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b23ef-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b23ef-120">Header</span><span class="sxs-lookup"><span data-stu-id="b23ef-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b23ef-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b23ef-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b23ef-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b23ef-122">Library</span></span><br/> | <dl> <span data-ttu-id="b23ef-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b23ef-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23ef-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b23ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23ef-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b23ef-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b23ef-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="b23ef-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
