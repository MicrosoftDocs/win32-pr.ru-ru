---
description: Определяет произведение текущей матрицы и заданную матрицу.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'Метод ID3DXMATRIXStack:: Мултматрикс (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713554"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="69f7a-103">Метод ID3DXMATRIXStack:: Мултматрикс (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="69f7a-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="69f7a-104">Определяет произведение текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="69f7a-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69f7a-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="69f7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f7a-107">*пмат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69f7a-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f7a-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="69f7a-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="69f7a-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которую необходимо умножить на текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="69f7a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f7a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69f7a-110">Return value</span></span>

<span data-ttu-id="69f7a-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69f7a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69f7a-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="69f7a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69f7a-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="69f7a-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f7a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69f7a-114">Remarks</span></span>

<span data-ttu-id="69f7a-115">Этот метод дает право на умножение заданной матрицы в текущую матрицу (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="69f7a-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="69f7a-116">Этот метод не добавляет элемент в стек, он заменяет текущую матрицу на продукт текущей матрицы и заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="69f7a-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f7a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="69f7a-117">Requirements</span></span>



| <span data-ttu-id="69f7a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="69f7a-118">Requirement</span></span> | <span data-ttu-id="69f7a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="69f7a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69f7a-120">Header</span><span class="sxs-lookup"><span data-stu-id="69f7a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="69f7a-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f7a-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="69f7a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69f7a-122">Library</span></span><br/> | <dl> <span data-ttu-id="69f7a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69f7a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69f7a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69f7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f7a-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="69f7a-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="69f7a-126">**ID3DXMATRIXStack:: Мултматрикслокал**</span><span class="sxs-lookup"><span data-stu-id="69f7a-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




