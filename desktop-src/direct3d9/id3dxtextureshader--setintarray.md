---
description: Задает массив целых чисел.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'Метод ID3DXTextureShader:: Сетинтаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713716"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="bb6fa-103">Метод ID3DXTextureShader:: Сетинтаррай</span><span class="sxs-lookup"><span data-stu-id="bb6fa-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="bb6fa-104">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb6fa-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="bb6fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6fa-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb6fa-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6fa-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bb6fa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bb6fa-109">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="bb6fa-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="bb6fa-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb6fa-111">*PN* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb6fa-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6fa-112">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb6fa-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bb6fa-113">Массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="bb6fa-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb6fa-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6fa-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb6fa-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb6fa-116">Число целочисленных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6fa-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb6fa-117">Return value</span></span>

<span data-ttu-id="bb6fa-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb6fa-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb6fa-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb6fa-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bb6fa-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6fa-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bb6fa-121">Requirements</span></span>



| <span data-ttu-id="bb6fa-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bb6fa-122">Requirement</span></span> | <span data-ttu-id="bb6fa-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bb6fa-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="bb6fa-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb6fa-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6fa-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bb6fa-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb6fa-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb6fa-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb6fa-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bb6fa-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb6fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6fa-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bb6fa-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
