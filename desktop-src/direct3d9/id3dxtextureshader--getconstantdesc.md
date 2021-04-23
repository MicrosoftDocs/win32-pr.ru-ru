---
description: Возвращает указатель на массив констант в таблице констант.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'Метод ID3DXTextureShader:: Жетконстантдеск (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703936"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="06513-103">Метод ID3DXTextureShader:: Жетконстантдеск</span><span class="sxs-lookup"><span data-stu-id="06513-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="06513-104">Возвращает указатель на массив констант в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="06513-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="06513-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06513-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="06513-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06513-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06513-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06513-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="06513-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="06513-109">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="06513-109">Unique identifier to a constant.</span></span> <span data-ttu-id="06513-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="06513-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="06513-111">*пдеск* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="06513-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06513-112">Тип: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="06513-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="06513-113">Возвращает указатель на массив описаний.</span><span class="sxs-lookup"><span data-stu-id="06513-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="06513-114">См. [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="06513-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="06513-115">*pCount* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="06513-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06513-116">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06513-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06513-117">Указанный вход должен быть максимальным размером массива.</span><span class="sxs-lookup"><span data-stu-id="06513-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="06513-118">Выходные данные — это количество элементов, заполняемых в массиве при возврате функции.</span><span class="sxs-lookup"><span data-stu-id="06513-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06513-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06513-119">Return value</span></span>

<span data-ttu-id="06513-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06513-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06513-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="06513-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06513-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="06513-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="06513-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06513-123">Remarks</span></span>

<span data-ttu-id="06513-124">В таблице константы пробы могут появляться более одного раза, поэтому этот метод может возвращать массив описаний с разными индексами регистров.</span><span class="sxs-lookup"><span data-stu-id="06513-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="06513-125">Требования</span><span class="sxs-lookup"><span data-stu-id="06513-125">Requirements</span></span>



| <span data-ttu-id="06513-126">Требование</span><span class="sxs-lookup"><span data-stu-id="06513-126">Requirement</span></span> | <span data-ttu-id="06513-127">Значение</span><span class="sxs-lookup"><span data-stu-id="06513-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06513-128">Header</span><span class="sxs-lookup"><span data-stu-id="06513-128">Header</span></span><br/>  | <dl> <span data-ttu-id="06513-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="06513-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="06513-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06513-130">Library</span></span><br/> | <dl> <span data-ttu-id="06513-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06513-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="06513-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06513-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06513-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="06513-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="06513-134">**ID3DXTextureShader:: DESC**</span><span class="sxs-lookup"><span data-stu-id="06513-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
