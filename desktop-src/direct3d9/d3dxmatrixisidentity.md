---
description: Определяет, является ли матрица матрицей идентификаторов.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: Функция D3DXMatrixIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355433"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="aae49-103">Функция D3DXMatrixIsIdentity</span><span class="sxs-lookup"><span data-stu-id="aae49-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="aae49-104">Определяет, является ли матрица матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="aae49-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aae49-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="aae49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aae49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae49-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aae49-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae49-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="aae49-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aae49-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая будет протестирована для идентификации.</span><span class="sxs-lookup"><span data-stu-id="aae49-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae49-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aae49-110">Return value</span></span>

<span data-ttu-id="aae49-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae49-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aae49-112">Если матрица является матрицей идентификаторов, эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="aae49-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="aae49-113">В противном случае эта функция возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="aae49-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae49-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aae49-114">Requirements</span></span>



| <span data-ttu-id="aae49-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aae49-115">Requirement</span></span> | <span data-ttu-id="aae49-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aae49-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae49-117">Header</span><span class="sxs-lookup"><span data-stu-id="aae49-117">Header</span></span><br/>  | <dl> <span data-ttu-id="aae49-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae49-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aae49-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aae49-119">Library</span></span><br/> | <dl> <span data-ttu-id="aae49-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aae49-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aae49-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae49-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae49-122">Математические функции</span><span class="sxs-lookup"><span data-stu-id="aae49-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="aae49-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="aae49-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 
