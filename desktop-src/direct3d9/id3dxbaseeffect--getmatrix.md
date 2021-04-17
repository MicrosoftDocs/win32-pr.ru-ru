---
description: Возвращает матрицу нонтранспосед.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'Метод ID3DXBaseEffect:: Matrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703992"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="378a1-103">Метод ID3DXBaseEffect:: Matrix</span><span class="sxs-lookup"><span data-stu-id="378a1-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="378a1-104">Возвращает матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="378a1-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="378a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="378a1-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="378a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="378a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378a1-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="378a1-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378a1-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="378a1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="378a1-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="378a1-109">Unique identifier.</span></span> <span data-ttu-id="378a1-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="378a1-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="378a1-111">*пматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="378a1-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="378a1-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="378a1-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="378a1-113">Возвращает матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="378a1-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="378a1-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="378a1-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378a1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="378a1-115">Return value</span></span>

<span data-ttu-id="378a1-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="378a1-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="378a1-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="378a1-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="378a1-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="378a1-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="378a1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="378a1-119">Remarks</span></span>

<span data-ttu-id="378a1-120">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="378a1-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="378a1-121">Если целевая матрица больше, чем исходная матрица, будут заполнены только верхние левые компоненты целевой матрицы, а остальные компоненты будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="378a1-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="378a1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="378a1-122">Requirements</span></span>



| <span data-ttu-id="378a1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="378a1-123">Requirement</span></span> | <span data-ttu-id="378a1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="378a1-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="378a1-125">Header</span><span class="sxs-lookup"><span data-stu-id="378a1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="378a1-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="378a1-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="378a1-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="378a1-127">Library</span></span><br/> | <dl> <span data-ttu-id="378a1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="378a1-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="378a1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="378a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378a1-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="378a1-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="378a1-131">**сетматрикс**</span><span class="sxs-lookup"><span data-stu-id="378a1-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




