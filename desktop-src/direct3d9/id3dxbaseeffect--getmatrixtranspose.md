---
description: Получает трансобъектную матрицу.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355890"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="fd5c4-103">Метод ID3DXBaseEffect:: Жетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="fd5c4-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="fd5c4-104">Получает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd5c4-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="fd5c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd5c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd5c4-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd5c4-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd5c4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fd5c4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fd5c4-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-109">Unique identifier.</span></span> <span data-ttu-id="fd5c4-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fd5c4-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd5c4-111">*пматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fd5c4-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd5c4-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd5c4-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd5c4-113">Возвращает переустановленную матрицу.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-113">Returns a transposed matrix.</span></span> <span data-ttu-id="fd5c4-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fd5c4-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd5c4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd5c4-115">Return value</span></span>

<span data-ttu-id="fd5c4-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd5c4-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd5c4-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fd5c4-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd5c4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd5c4-119">Remarks</span></span>

<span data-ttu-id="fd5c4-120">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="fd5c4-121">Если целевая матрица больше, чем исходная матрица, будут заполнены только верхние левые элементы целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd5c4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fd5c4-122">Requirements</span></span>



| <span data-ttu-id="fd5c4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fd5c4-123">Requirement</span></span> | <span data-ttu-id="fd5c4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fd5c4-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5c4-125">Header</span><span class="sxs-lookup"><span data-stu-id="fd5c4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fd5c4-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd5c4-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fd5c4-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd5c4-127">Library</span></span><br/> | <dl> <span data-ttu-id="fd5c4-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd5c4-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fd5c4-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd5c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5c4-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fd5c4-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fd5c4-131">**сетматрикстранспосе**</span><span class="sxs-lookup"><span data-stu-id="fd5c4-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




