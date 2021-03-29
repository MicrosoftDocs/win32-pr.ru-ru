---
description: Задает массив целых чисел.
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
ms.openlocfilehash: f76ff0d7f4bcc68d7cce85f3d02f2bc207a5f4b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647805"
---
# <a name="id3dxbaseeffectsetintarray-method"></a><span data-ttu-id="c8166-103">Метод ID3DXBaseEffect:: Сетинтаррай</span><span class="sxs-lookup"><span data-stu-id="c8166-103">ID3DXBaseEffect::SetIntArray method</span></span>

<span data-ttu-id="c8166-104">Задает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="c8166-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8166-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8166-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c8166-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8166-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8166-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8166-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8166-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c8166-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c8166-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c8166-109">Unique identifier.</span></span> <span data-ttu-id="c8166-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c8166-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8166-111">*PN* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8166-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8166-112">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8166-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8166-113">Массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="c8166-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="c8166-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8166-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8166-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8166-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8166-116">Число целочисленных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="c8166-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8166-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8166-117">Return value</span></span>

<span data-ttu-id="c8166-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8166-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8166-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c8166-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c8166-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c8166-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8166-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c8166-121">Requirements</span></span>



| <span data-ttu-id="c8166-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c8166-122">Requirement</span></span> | <span data-ttu-id="c8166-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c8166-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8166-124">Header</span><span class="sxs-lookup"><span data-stu-id="c8166-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c8166-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8166-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c8166-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8166-126">Library</span></span><br/> | <dl> <span data-ttu-id="c8166-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8166-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c8166-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8166-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8166-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c8166-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c8166-130">**жетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="c8166-130">**GetIntArray**</span></span>](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
