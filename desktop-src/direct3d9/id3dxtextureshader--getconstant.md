---
description: Возвращает константу путем поиска своего индекса.
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
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703938"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="2a88f-103">Метод ID3DXTextureShader:: with Constant</span><span class="sxs-lookup"><span data-stu-id="2a88f-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="2a88f-104">Возвращает константу путем поиска своего индекса.</span><span class="sxs-lookup"><span data-stu-id="2a88f-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a88f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a88f-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="2a88f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a88f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a88f-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a88f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a88f-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2a88f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2a88f-109">[Маркер](handles.md) родительской структуры данных.</span><span class="sxs-lookup"><span data-stu-id="2a88f-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="2a88f-110">Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2a88f-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a88f-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a88f-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a88f-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a88f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a88f-113">Отсчитываемый от нуля индекс константы.</span><span class="sxs-lookup"><span data-stu-id="2a88f-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a88f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a88f-114">Return value</span></span>

<span data-ttu-id="2a88f-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2a88f-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2a88f-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="2a88f-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a88f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a88f-117">Remarks</span></span>

<span data-ttu-id="2a88f-118">Чтобы получить константу из массива констант, используйте [**ID3DXTextureShader:: жетконстантелемент**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a88f-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a88f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2a88f-119">Requirements</span></span>



| <span data-ttu-id="2a88f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2a88f-120">Requirement</span></span> | <span data-ttu-id="2a88f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2a88f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a88f-122">Header</span><span class="sxs-lookup"><span data-stu-id="2a88f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2a88f-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a88f-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2a88f-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a88f-124">Library</span></span><br/> | <dl> <span data-ttu-id="2a88f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a88f-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2a88f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a88f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a88f-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2a88f-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
