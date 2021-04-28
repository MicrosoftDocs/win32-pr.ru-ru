---
description: 'Метод ID3DXTextureShader:: SetFloat — задает число с плавающей запятой.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'Метод ID3DXTextureShader:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6230b0736cb3bc623b0413f7b5a1cb9635f00e07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107172"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="ed44f-103">Метод ID3DXTextureShader:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="ed44f-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="ed44f-104">Задает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed44f-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed44f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed44f-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="ed44f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed44f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed44f-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed44f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed44f-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ed44f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ed44f-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="ed44f-109">Unique identifier to the constant.</span></span> <span data-ttu-id="ed44f-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ed44f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed44f-111">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ed44f-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed44f-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed44f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed44f-113">Число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ed44f-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed44f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed44f-114">Return value</span></span>

<span data-ttu-id="ed44f-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed44f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed44f-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ed44f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed44f-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ed44f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed44f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ed44f-118">Requirements</span></span>



| <span data-ttu-id="ed44f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ed44f-119">Requirement</span></span> | <span data-ttu-id="ed44f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ed44f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed44f-121">Header</span><span class="sxs-lookup"><span data-stu-id="ed44f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ed44f-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed44f-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ed44f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed44f-123">Library</span></span><br/> | <dl> <span data-ttu-id="ed44f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed44f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed44f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ed44f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed44f-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ed44f-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
