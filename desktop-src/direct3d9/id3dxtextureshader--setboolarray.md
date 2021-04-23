---
description: Задает массив значений типа BOOL.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'Метод ID3DXTextureShader:: Сетбуларрай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694271"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="f2bf7-103">Метод ID3DXTextureShader:: Сетбуларрай</span><span class="sxs-lookup"><span data-stu-id="f2bf7-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="f2bf7-104">Задает массив значений типа BOOL.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bf7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2bf7-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="f2bf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2bf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2bf7-107">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2bf7-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bf7-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f2bf7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f2bf7-109">Уникальный идентификатор массива констант.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="f2bf7-110">См. [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="f2bf7-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2bf7-111">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2bf7-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bf7-112">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2bf7-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f2bf7-113">Массив значений типа BOOL.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="f2bf7-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2bf7-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bf7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2bf7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2bf7-116">Количество значений BOOL в массиве.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2bf7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2bf7-117">Return value</span></span>

<span data-ttu-id="f2bf7-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2bf7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2bf7-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2bf7-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f2bf7-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bf7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f2bf7-121">Requirements</span></span>



| <span data-ttu-id="f2bf7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f2bf7-122">Requirement</span></span> | <span data-ttu-id="f2bf7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f2bf7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bf7-124">Header</span><span class="sxs-lookup"><span data-stu-id="f2bf7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f2bf7-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f2bf7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2bf7-126">Library</span></span><br/> | <dl> <span data-ttu-id="f2bf7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2bf7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2bf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bf7-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f2bf7-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
