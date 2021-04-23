---
description: Задает массив векторов 4D.
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
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664967"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="edee0-103">Метод ID3DXTextureShader:: Сетвектораррай</span><span class="sxs-lookup"><span data-stu-id="edee0-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="edee0-104">Задает массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="edee0-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="edee0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edee0-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="edee0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edee0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edee0-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edee0-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edee0-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="edee0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="edee0-109">Уникальный идентификатор массива констант Vector.</span><span class="sxs-lookup"><span data-stu-id="edee0-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="edee0-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="edee0-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="edee0-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edee0-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edee0-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="edee0-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="edee0-113">Массив векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="edee0-113">Array of 4D vectors.</span></span> <span data-ttu-id="edee0-114">См. [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="edee0-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="edee0-115">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edee0-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edee0-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edee0-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edee0-117">Количество векторов в массиве.</span><span class="sxs-lookup"><span data-stu-id="edee0-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edee0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edee0-118">Return value</span></span>

<span data-ttu-id="edee0-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edee0-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edee0-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="edee0-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="edee0-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="edee0-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="edee0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="edee0-122">Requirements</span></span>



| <span data-ttu-id="edee0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="edee0-123">Requirement</span></span> | <span data-ttu-id="edee0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="edee0-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="edee0-125">Header</span><span class="sxs-lookup"><span data-stu-id="edee0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="edee0-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="edee0-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="edee0-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edee0-127">Library</span></span><br/> | <dl> <span data-ttu-id="edee0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edee0-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="edee0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edee0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edee0-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="edee0-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
