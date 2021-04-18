---
description: Определяет произведение заданной матрицы и текущей матрицы.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'Метод ID3DXMATRIXStack:: Мултматрикслокал (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713553"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="138ec-103">Метод ID3DXMATRIXStack:: Мултматрикслокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="138ec-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="138ec-104">Определяет произведение заданной матрицы и текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="138ec-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="138ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="138ec-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="138ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="138ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138ec-107">*пмат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="138ec-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="138ec-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="138ec-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="138ec-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="138ec-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="138ec-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="138ec-110">Return value</span></span>

<span data-ttu-id="138ec-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="138ec-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="138ec-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="138ec-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="138ec-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="138ec-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="138ec-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="138ec-114">Remarks</span></span>

<span data-ttu-id="138ec-115">Этот метод Left — Умножает заданную матрицу на текущую матрицу (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="138ec-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="138ec-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт заданной матрицы и текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="138ec-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="138ec-117">Требования</span><span class="sxs-lookup"><span data-stu-id="138ec-117">Requirements</span></span>



| <span data-ttu-id="138ec-118">Требование</span><span class="sxs-lookup"><span data-stu-id="138ec-118">Requirement</span></span> | <span data-ttu-id="138ec-119">Значение</span><span class="sxs-lookup"><span data-stu-id="138ec-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="138ec-120">Header</span><span class="sxs-lookup"><span data-stu-id="138ec-120">Header</span></span><br/>  | <dl> <span data-ttu-id="138ec-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="138ec-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="138ec-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="138ec-122">Library</span></span><br/> | <dl> <span data-ttu-id="138ec-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="138ec-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="138ec-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="138ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138ec-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="138ec-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="138ec-126">**ID3DXMATRIXStack:: Мултматрикс**</span><span class="sxs-lookup"><span data-stu-id="138ec-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




