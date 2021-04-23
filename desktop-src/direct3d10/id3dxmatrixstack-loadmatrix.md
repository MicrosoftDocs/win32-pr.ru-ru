---
description: Загружает заданную матрицу в текущую матрицу.
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'Метод ID3DXMATRIXStack:: Лоадматрикс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce6b99abf4c9a82a8b9d1c7643a1098d19e18c15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356013"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="cc147-103">Метод ID3DXMATRIXStack:: Лоадматрикс (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="cc147-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="cc147-104">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="cc147-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc147-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc147-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="cc147-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc147-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc147-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc147-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc147-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc147-109">Указатель на структуру D3DXMATRIX, загруженную в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="cc147-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc147-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc147-110">Return value</span></span>

<span data-ttu-id="cc147-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc147-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc147-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cc147-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc147-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="cc147-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc147-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc147-114">Remarks</span></span>

<span data-ttu-id="cc147-115">Обратите внимание, что этот метод не добавляет элемент в стек; Вместо этого он заменяет текущую матрицу представленной матрицей.</span><span class="sxs-lookup"><span data-stu-id="cc147-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc147-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cc147-116">Requirements</span></span>



| <span data-ttu-id="cc147-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cc147-117">Requirement</span></span> | <span data-ttu-id="cc147-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cc147-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc147-119">Header</span><span class="sxs-lookup"><span data-stu-id="cc147-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc147-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc147-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc147-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc147-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc147-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc147-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc147-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc147-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc147-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="cc147-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="cc147-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="cc147-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
