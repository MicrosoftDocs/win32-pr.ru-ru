---
description: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h) — определяет продукт текущей матрицы и заданную матрицу.'
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
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107972"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="e4682-103">Метод ID3DXMATRIXStack:: Мултматрикс (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="e4682-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="e4682-104">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e4682-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4682-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4682-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e4682-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4682-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4682-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4682-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4682-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4682-109">Указатель на структуру D3DXMATRIX, которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="e4682-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4682-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4682-110">Return value</span></span>

<span data-ttu-id="e4682-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4682-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4682-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e4682-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4682-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e4682-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4682-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="e4682-114">Remarks</span></span>

<span data-ttu-id="e4682-115">Этот метод дает право на умножение заданной матрицы в текущую матрицу (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="e4682-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="e4682-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e4682-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4682-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e4682-117">Requirements</span></span>



| <span data-ttu-id="e4682-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e4682-118">Requirement</span></span> | <span data-ttu-id="e4682-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e4682-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4682-120">Header</span><span class="sxs-lookup"><span data-stu-id="e4682-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e4682-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4682-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4682-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4682-122">Library</span></span><br/> | <dl> <span data-ttu-id="e4682-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4682-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4682-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e4682-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4682-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="e4682-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e4682-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="e4682-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
