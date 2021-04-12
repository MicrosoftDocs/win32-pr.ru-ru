---
description: Получить константу из таблицы констант.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Метод ID3DXTextureShader:: Жетконстантелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273805"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="b3ca4-103">Метод ID3DXTextureShader:: Жетконстантелемент</span><span class="sxs-lookup"><span data-stu-id="b3ca4-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="b3ca4-104">Получить константу из таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ca4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3ca4-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="b3ca4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ca4-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3ca4-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ca4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3ca4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3ca4-109">[Маркер](handles.md) массива констант.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="b3ca4-110">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3ca4-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3ca4-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ca4-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3ca4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3ca4-113">Отсчитываемый от нуля индекс элемента в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ca4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3ca4-114">Return value</span></span>

<span data-ttu-id="b3ca4-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b3ca4-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b3ca4-116">Возвращает уникальный идентификатор для константы.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ca4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3ca4-117">Remarks</span></span>

<span data-ttu-id="b3ca4-118">Чтобы получить константу, которая не является частью массива, используйте [**ID3DXTextureShader::-Constant**](id3dxtextureshader--getconstant.md) или [**ID3DXTextureShader:: жетконстантбинаме**](id3dxtextureshader--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="b3ca4-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ca4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b3ca4-119">Requirements</span></span>



| <span data-ttu-id="b3ca4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b3ca4-120">Requirement</span></span> | <span data-ttu-id="b3ca4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b3ca4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ca4-122">Header</span><span class="sxs-lookup"><span data-stu-id="b3ca4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b3ca4-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ca4-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b3ca4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b3ca4-124">Library</span></span><br/> | <dl> <span data-ttu-id="b3ca4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3ca4-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b3ca4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3ca4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ca4-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b3ca4-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
