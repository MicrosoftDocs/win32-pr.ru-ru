---
description: 'Метод ID3DXBaseEffect:: сетматрикс — задает трансобъектную матрицу.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'Метод ID3DXBaseEffect:: Сетматрикс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097502"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="f687a-103">Метод ID3DXBaseEffect:: Сетматрикс</span><span class="sxs-lookup"><span data-stu-id="f687a-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="f687a-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="f687a-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f687a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f687a-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="f687a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f687a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f687a-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f687a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f687a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f687a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f687a-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f687a-109">Unique identifier.</span></span> <span data-ttu-id="f687a-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f687a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f687a-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f687a-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f687a-112">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f687a-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f687a-113">Указатель на матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="f687a-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="f687a-114">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="f687a-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f687a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f687a-115">Return value</span></span>

<span data-ttu-id="f687a-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f687a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f687a-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f687a-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f687a-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f687a-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f687a-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="f687a-119">Remarks</span></span>

<span data-ttu-id="f687a-120">Неперенесенная матрица содержит основные данные строки.</span><span class="sxs-lookup"><span data-stu-id="f687a-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="f687a-121">Иными словами, каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="f687a-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="f687a-122">Если целевая матрица меньше, чем исходная матрица, дополнительные компоненты исходной матрицы будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="f687a-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f687a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f687a-123">Requirements</span></span>



| <span data-ttu-id="f687a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f687a-124">Requirement</span></span> | <span data-ttu-id="f687a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f687a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f687a-126">Header</span><span class="sxs-lookup"><span data-stu-id="f687a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f687a-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f687a-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f687a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f687a-128">Library</span></span><br/> | <dl> <span data-ttu-id="f687a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f687a-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f687a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f687a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f687a-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f687a-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f687a-132">**Матрица**</span><span class="sxs-lookup"><span data-stu-id="f687a-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




