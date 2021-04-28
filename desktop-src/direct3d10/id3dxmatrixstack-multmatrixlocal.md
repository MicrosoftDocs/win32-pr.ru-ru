---
description: 'Метод ID3DXMATRIXStack:: Мултматрикслокал (D3DX10. h) — определяет продукт данной матрицы и текущую матрицу.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'Метод ID3DXMATRIXStack:: Мултматрикслокал (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107952"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="284ce-103">Метод ID3DXMATRIXStack:: Мултматрикслокал (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="284ce-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="284ce-104">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="284ce-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="284ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="284ce-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="284ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="284ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284ce-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="284ce-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="284ce-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="284ce-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="284ce-109">Указатель на структуру D3DXMATRIX, которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="284ce-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284ce-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="284ce-110">Return value</span></span>

<span data-ttu-id="284ce-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="284ce-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="284ce-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="284ce-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="284ce-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="284ce-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="284ce-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="284ce-114">Remarks</span></span>

<span data-ttu-id="284ce-115">Этот метод Left — Умножает заданную матрицу на текущую матрицу (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="284ce-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="284ce-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт заданной матрицы и текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="284ce-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="284ce-117">Требования</span><span class="sxs-lookup"><span data-stu-id="284ce-117">Requirements</span></span>



| <span data-ttu-id="284ce-118">Требование</span><span class="sxs-lookup"><span data-stu-id="284ce-118">Requirement</span></span> | <span data-ttu-id="284ce-119">Значение</span><span class="sxs-lookup"><span data-stu-id="284ce-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="284ce-120">Header</span><span class="sxs-lookup"><span data-stu-id="284ce-120">Header</span></span><br/>  | <dl> <span data-ttu-id="284ce-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="284ce-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="284ce-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="284ce-122">Library</span></span><br/> | <dl> <span data-ttu-id="284ce-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="284ce-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284ce-124">См. также</span><span class="sxs-lookup"><span data-stu-id="284ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284ce-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="284ce-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="284ce-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="284ce-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
