---
description: 'Метод ID3DXTextureShader:: Сетфлоатаррай — задает массив чисел с плавающей запятой.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'Метод ID3DXTextureShader:: Сетфлоатаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090252"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="7ec75-103">Метод ID3DXTextureShader:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="7ec75-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="7ec75-104">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="7ec75-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ec75-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7ec75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ec75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec75-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ec75-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec75-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec75-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7ec75-109">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="7ec75-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="7ec75-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="7ec75-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ec75-111">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ec75-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec75-112">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ec75-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ec75-113">Массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="7ec75-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="7ec75-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ec75-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec75-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec75-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ec75-116">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="7ec75-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec75-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ec75-117">Return value</span></span>

<span data-ttu-id="7ec75-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ec75-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ec75-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7ec75-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ec75-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="7ec75-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec75-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7ec75-121">Requirements</span></span>



| <span data-ttu-id="7ec75-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7ec75-122">Requirement</span></span> | <span data-ttu-id="7ec75-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7ec75-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec75-124">Header</span><span class="sxs-lookup"><span data-stu-id="7ec75-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7ec75-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec75-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7ec75-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ec75-126">Library</span></span><br/> | <dl> <span data-ttu-id="7ec75-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ec75-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7ec75-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7ec75-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec75-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="7ec75-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
