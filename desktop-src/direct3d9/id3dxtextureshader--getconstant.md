---
description: Метод ID3DXTextureShader::-Constant — возвращает константу путем поиска своего индекса.
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Метод ID3DXTextureShader::-Constant (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117672"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="20b5d-103">Метод ID3DXTextureShader:: with Constant</span><span class="sxs-lookup"><span data-stu-id="20b5d-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="20b5d-104">Возвращает константу путем поиска своего индекса.</span><span class="sxs-lookup"><span data-stu-id="20b5d-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20b5d-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="20b5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b5d-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20b5d-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b5d-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="20b5d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="20b5d-109">[Маркер](handles.md) родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="20b5d-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="20b5d-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="20b5d-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="20b5d-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20b5d-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b5d-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20b5d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20b5d-113">Отсчитываемый от нуля индекс константы.</span><span class="sxs-lookup"><span data-stu-id="20b5d-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b5d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20b5d-114">Return value</span></span>

<span data-ttu-id="20b5d-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="20b5d-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="20b5d-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="20b5d-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="20b5d-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="20b5d-117">Remarks</span></span>

<span data-ttu-id="20b5d-118">Чтобы получить константу из массива констант, используйте [**ID3DXTextureShader:: жетконстантелемент**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="20b5d-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20b5d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="20b5d-119">Requirements</span></span>



| <span data-ttu-id="20b5d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="20b5d-120">Requirement</span></span> | <span data-ttu-id="20b5d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="20b5d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b5d-122">Header</span><span class="sxs-lookup"><span data-stu-id="20b5d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="20b5d-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b5d-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="20b5d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20b5d-124">Library</span></span><br/> | <dl> <span data-ttu-id="20b5d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20b5d-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20b5d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="20b5d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b5d-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="20b5d-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
