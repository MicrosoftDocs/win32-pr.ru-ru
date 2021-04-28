---
description: 'Метод ID3DXTextureShader:: Сетвектораррай — задает массив векторов 4D.'
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'Метод ID3DXTextureShader:: Сетвектораррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0878594baa8828c9cca4eca8dd2c20f225fb530e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090192"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="e532c-103">Метод ID3DXTextureShader:: Сетвектораррай</span><span class="sxs-lookup"><span data-stu-id="e532c-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="e532c-104">Задает массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="e532c-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e532c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e532c-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="e532c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e532c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e532c-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e532c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e532c-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e532c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e532c-109">Уникальный идентификатор массива констант Vector.</span><span class="sxs-lookup"><span data-stu-id="e532c-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="e532c-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e532c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e532c-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e532c-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e532c-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e532c-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e532c-113">Массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="e532c-113">Array of 4D vectors.</span></span> <span data-ttu-id="e532c-114">См. [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="e532c-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="e532c-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e532c-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e532c-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e532c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e532c-117">Количество векторов в массиве.</span><span class="sxs-lookup"><span data-stu-id="e532c-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e532c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e532c-118">Return value</span></span>

<span data-ttu-id="e532c-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e532c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e532c-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e532c-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e532c-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e532c-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e532c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e532c-122">Requirements</span></span>



| <span data-ttu-id="e532c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e532c-123">Requirement</span></span> | <span data-ttu-id="e532c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e532c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e532c-125">Header</span><span class="sxs-lookup"><span data-stu-id="e532c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e532c-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e532c-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e532c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e532c-127">Library</span></span><br/> | <dl> <span data-ttu-id="e532c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e532c-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e532c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e532c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e532c-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e532c-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
