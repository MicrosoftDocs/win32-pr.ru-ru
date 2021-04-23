---
description: Задает массив чисел с плавающей запятой.
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
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273803"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="d2fe3-103">Метод ID3DXTextureShader:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="d2fe3-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="d2fe3-104">Задает массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fe3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2fe3-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d2fe3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2fe3-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2fe3-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fe3-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d2fe3-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d2fe3-109">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="d2fe3-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="d2fe3-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2fe3-111">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2fe3-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fe3-112">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2fe3-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d2fe3-113">Массив чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="d2fe3-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2fe3-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fe3-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2fe3-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2fe3-116">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2fe3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2fe3-117">Return value</span></span>

<span data-ttu-id="d2fe3-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2fe3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2fe3-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2fe3-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d2fe3-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2fe3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d2fe3-121">Requirements</span></span>



| <span data-ttu-id="d2fe3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d2fe3-122">Requirement</span></span> | <span data-ttu-id="d2fe3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d2fe3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fe3-124">Header</span><span class="sxs-lookup"><span data-stu-id="d2fe3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d2fe3-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2fe3-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d2fe3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2fe3-126">Library</span></span><br/> | <dl> <span data-ttu-id="d2fe3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2fe3-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d2fe3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2fe3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2fe3-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d2fe3-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
