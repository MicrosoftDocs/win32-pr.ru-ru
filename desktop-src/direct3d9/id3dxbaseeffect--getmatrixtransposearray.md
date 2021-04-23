---
description: Возвращает массив переданных матриц.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосеаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821500"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="58bfc-103">Метод ID3DXBaseEffect:: Жетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="58bfc-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="58bfc-104">Возвращает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="58bfc-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="58bfc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58bfc-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="58bfc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58bfc-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58bfc-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bfc-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="58bfc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="58bfc-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="58bfc-109">Unique identifier.</span></span> <span data-ttu-id="58bfc-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="58bfc-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="58bfc-111">*пматрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="58bfc-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58bfc-112">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="58bfc-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58bfc-113">Возвращает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="58bfc-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="58bfc-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="58bfc-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="58bfc-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58bfc-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bfc-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58bfc-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58bfc-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="58bfc-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58bfc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58bfc-118">Return value</span></span>

<span data-ttu-id="58bfc-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58bfc-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58bfc-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="58bfc-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="58bfc-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="58bfc-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="58bfc-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58bfc-122">Remarks</span></span>

<span data-ttu-id="58bfc-123">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="58bfc-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="58bfc-124">Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="58bfc-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="58bfc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="58bfc-125">Requirements</span></span>



| <span data-ttu-id="58bfc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="58bfc-126">Requirement</span></span> | <span data-ttu-id="58bfc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="58bfc-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="58bfc-128">Header</span><span class="sxs-lookup"><span data-stu-id="58bfc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="58bfc-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="58bfc-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="58bfc-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="58bfc-130">Library</span></span><br/> | <dl> <span data-ttu-id="58bfc-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58bfc-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="58bfc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58bfc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bfc-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="58bfc-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="58bfc-134">**сетматрикстранспосеаррай**</span><span class="sxs-lookup"><span data-stu-id="58bfc-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
