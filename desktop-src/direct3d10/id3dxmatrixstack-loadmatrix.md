---
description: 'Метод ID3DXMATRIXStack:: Лоадматрикс (D3DX10. h) — загружает заданную матрицу в текущую матрицу.'
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
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107962"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="2db56-103">Метод ID3DXMATRIXStack:: Лоадматрикс (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2db56-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="2db56-104">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2db56-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2db56-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2db56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2db56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db56-107">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2db56-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2db56-108">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2db56-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2db56-109">Указатель на структуру D3DXMATRIX, загруженную в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2db56-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db56-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2db56-110">Return value</span></span>

<span data-ttu-id="2db56-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2db56-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2db56-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2db56-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2db56-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2db56-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db56-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="2db56-114">Remarks</span></span>

<span data-ttu-id="2db56-115">Обратите внимание, что этот метод не добавляет элемент в стек; Вместо этого он заменяет текущую матрицу представленной матрицей.</span><span class="sxs-lookup"><span data-stu-id="2db56-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db56-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2db56-116">Requirements</span></span>



| <span data-ttu-id="2db56-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2db56-117">Requirement</span></span> | <span data-ttu-id="2db56-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2db56-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2db56-119">Header</span><span class="sxs-lookup"><span data-stu-id="2db56-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2db56-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db56-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2db56-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2db56-121">Library</span></span><br/> | <dl> <span data-ttu-id="2db56-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2db56-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2db56-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2db56-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db56-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2db56-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2db56-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="2db56-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
