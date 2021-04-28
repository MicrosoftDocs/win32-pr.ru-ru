---
description: 'Метод ID3DXTextureShader:: Сетвектор — задает вектор 4D.'
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'Метод ID3DXTextureShader:: Сетвектор (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e917e4ff13cf7c03de264542dc1995364f1dc526
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090162"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="22bbd-103">Метод ID3DXTextureShader:: Сетвектор</span><span class="sxs-lookup"><span data-stu-id="22bbd-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="22bbd-104">Задает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="22bbd-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="22bbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22bbd-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="22bbd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22bbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22bbd-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22bbd-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22bbd-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22bbd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22bbd-109">Уникальный идентификатор константы Vector.</span><span class="sxs-lookup"><span data-stu-id="22bbd-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="22bbd-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="22bbd-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="22bbd-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22bbd-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22bbd-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="22bbd-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="22bbd-113">Указатель на вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="22bbd-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="22bbd-114">См. [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="22bbd-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22bbd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22bbd-115">Return value</span></span>

<span data-ttu-id="22bbd-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22bbd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22bbd-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="22bbd-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="22bbd-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="22bbd-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22bbd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="22bbd-119">Requirements</span></span>



| <span data-ttu-id="22bbd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="22bbd-120">Requirement</span></span> | <span data-ttu-id="22bbd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="22bbd-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22bbd-122">Header</span><span class="sxs-lookup"><span data-stu-id="22bbd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="22bbd-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="22bbd-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="22bbd-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22bbd-124">Library</span></span><br/> | <dl> <span data-ttu-id="22bbd-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22bbd-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22bbd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="22bbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22bbd-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="22bbd-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




