---
description: Определяет произведение заданной матрицы и текущей матрицы.
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
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273969"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="0f8c6-103">Метод ID3DXMATRIXStack:: Мултматрикслокал (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="0f8c6-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="0f8c6-104">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="0f8c6-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f8c6-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0f8c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f8c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8c6-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f8c6-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8c6-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f8c6-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0f8c6-109">Указатель на структуру D3DXMATRIX, которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="0f8c6-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f8c6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f8c6-110">Return value</span></span>

<span data-ttu-id="0f8c6-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f8c6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f8c6-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0f8c6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f8c6-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0f8c6-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8c6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f8c6-114">Remarks</span></span>

<span data-ttu-id="0f8c6-115">Этот метод Left — Умножает заданную матрицу на текущую матрицу (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="0f8c6-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="0f8c6-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт заданной матрицы и текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="0f8c6-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8c6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0f8c6-117">Requirements</span></span>



| <span data-ttu-id="0f8c6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0f8c6-118">Requirement</span></span> | <span data-ttu-id="0f8c6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0f8c6-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8c6-120">Header</span><span class="sxs-lookup"><span data-stu-id="0f8c6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0f8c6-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f8c6-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f8c6-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f8c6-122">Library</span></span><br/> | <dl> <span data-ttu-id="0f8c6-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f8c6-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f8c6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f8c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8c6-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="0f8c6-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0f8c6-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="0f8c6-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
