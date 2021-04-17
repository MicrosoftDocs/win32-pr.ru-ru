---
description: Задает вектор 4D.
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
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664968"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="a0aac-103">Метод ID3DXTextureShader:: Сетвектор</span><span class="sxs-lookup"><span data-stu-id="a0aac-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="a0aac-104">Задает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="a0aac-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0aac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0aac-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="a0aac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0aac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0aac-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0aac-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0aac-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a0aac-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a0aac-109">Уникальный идентификатор константы Vector.</span><span class="sxs-lookup"><span data-stu-id="a0aac-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="a0aac-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a0aac-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0aac-111">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0aac-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0aac-112">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a0aac-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a0aac-113">Указатель на вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="a0aac-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="a0aac-114">См. [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="a0aac-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0aac-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0aac-115">Return value</span></span>

<span data-ttu-id="a0aac-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0aac-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0aac-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a0aac-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a0aac-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a0aac-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0aac-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a0aac-119">Requirements</span></span>



| <span data-ttu-id="a0aac-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a0aac-120">Requirement</span></span> | <span data-ttu-id="a0aac-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a0aac-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0aac-122">Header</span><span class="sxs-lookup"><span data-stu-id="a0aac-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a0aac-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0aac-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a0aac-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0aac-124">Library</span></span><br/> | <dl> <span data-ttu-id="a0aac-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0aac-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a0aac-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0aac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0aac-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a0aac-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




