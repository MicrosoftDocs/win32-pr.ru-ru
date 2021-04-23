---
description: Задает массив указателей для нонтранспосед матриц.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Метод ID3DXBaseEffect:: Сетматрикспоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000306"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="63479-103">Метод ID3DXBaseEffect:: Сетматрикспоинтераррай</span><span class="sxs-lookup"><span data-stu-id="63479-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="63479-104">Задает массив указателей для нонтранспосед матриц.</span><span class="sxs-lookup"><span data-stu-id="63479-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="63479-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63479-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="63479-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63479-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63479-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63479-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="63479-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="63479-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="63479-109">Unique identifier.</span></span> <span data-ttu-id="63479-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="63479-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="63479-111">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63479-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63479-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="63479-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="63479-113">Массив указателей на матрицы нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="63479-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="63479-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="63479-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="63479-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63479-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63479-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63479-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63479-117">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="63479-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63479-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63479-118">Return value</span></span>

<span data-ttu-id="63479-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63479-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63479-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="63479-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="63479-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="63479-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="63479-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63479-122">Remarks</span></span>

<span data-ttu-id="63479-123">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="63479-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="63479-124">Если целевые матрицы меньше исходных матриц, то дополнительные компоненты исходных матриц будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="63479-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="63479-125">Требования</span><span class="sxs-lookup"><span data-stu-id="63479-125">Requirements</span></span>



| <span data-ttu-id="63479-126">Требование</span><span class="sxs-lookup"><span data-stu-id="63479-126">Requirement</span></span> | <span data-ttu-id="63479-127">Значение</span><span class="sxs-lookup"><span data-stu-id="63479-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63479-128">Header</span><span class="sxs-lookup"><span data-stu-id="63479-128">Header</span></span><br/>  | <dl> <span data-ttu-id="63479-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="63479-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="63479-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63479-130">Library</span></span><br/> | <dl> <span data-ttu-id="63479-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63479-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="63479-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63479-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63479-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="63479-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="63479-134">**жетматриксаррай**</span><span class="sxs-lookup"><span data-stu-id="63479-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
