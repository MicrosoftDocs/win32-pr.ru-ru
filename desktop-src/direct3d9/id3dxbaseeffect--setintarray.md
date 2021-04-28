---
description: 'Метод ID3DXBaseEffect:: Сетинтаррай — задает массив целых чисел.'
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'Метод ID3DXBaseEffect:: Сетинтаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093762"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="2d541-103">Метод ID3DXBaseEffect:: Сетинтаррай</span><span class="sxs-lookup"><span data-stu-id="2d541-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="2d541-104">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="2d541-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d541-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d541-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2d541-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d541-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d541-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d541-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2d541-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2d541-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2d541-109">Unique identifier.</span></span> <span data-ttu-id="2d541-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2d541-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d541-111">*PN* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d541-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d541-112">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d541-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d541-113">Массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="2d541-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2d541-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d541-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d541-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d541-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d541-116">Число целочисленных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="2d541-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d541-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d541-117">Return value</span></span>

<span data-ttu-id="2d541-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d541-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d541-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2d541-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d541-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2d541-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d541-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2d541-121">Requirements</span></span>



| <span data-ttu-id="2d541-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2d541-122">Requirement</span></span> | <span data-ttu-id="2d541-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2d541-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d541-124">Header</span><span class="sxs-lookup"><span data-stu-id="2d541-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2d541-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d541-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2d541-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d541-126">Library</span></span><br/> | <dl> <span data-ttu-id="2d541-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d541-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d541-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2d541-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d541-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2d541-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2d541-130">**жетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="2d541-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
