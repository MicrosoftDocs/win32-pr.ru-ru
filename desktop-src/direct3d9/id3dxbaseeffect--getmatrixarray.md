---
description: Возвращает массив матриц нонтранспосед.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'Метод ID3DXBaseEffect:: Жетматриксаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703991"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a><span data-ttu-id="e616f-103">Метод ID3DXBaseEffect:: Жетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="e616f-103">ID3DXBaseEffect::GetMatrixArray method</span></span>

<span data-ttu-id="e616f-104">Возвращает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="e616f-104">Gets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e616f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e616f-105">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="e616f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e616f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e616f-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e616f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e616f-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e616f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e616f-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e616f-109">Unique identifier.</span></span> <span data-ttu-id="e616f-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e616f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e616f-111">*пматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e616f-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e616f-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e616f-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e616f-113">Возвращает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="e616f-113">Returns an array of nontransposed matrices.</span></span> <span data-ttu-id="e616f-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e616f-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e616f-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e616f-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e616f-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e616f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e616f-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="e616f-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e616f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e616f-118">Return value</span></span>

<span data-ttu-id="e616f-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e616f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e616f-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e616f-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e616f-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e616f-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e616f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e616f-122">Remarks</span></span>

<span data-ttu-id="e616f-123">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="e616f-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="e616f-124">Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e616f-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e616f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e616f-125">Requirements</span></span>



| <span data-ttu-id="e616f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e616f-126">Requirement</span></span> | <span data-ttu-id="e616f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e616f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e616f-128">Header</span><span class="sxs-lookup"><span data-stu-id="e616f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e616f-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e616f-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e616f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e616f-130">Library</span></span><br/> | <dl> <span data-ttu-id="e616f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e616f-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e616f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e616f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e616f-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e616f-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="e616f-134">**сетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="e616f-134">**SetMatrixArray**</span></span>](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
