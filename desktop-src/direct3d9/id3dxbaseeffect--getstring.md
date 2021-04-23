---
description: Возвращает строку.
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'Метод ID3DXBaseEffect:: GetString (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713990"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="79284-103">Метод ID3DXBaseEffect:: GetString</span><span class="sxs-lookup"><span data-stu-id="79284-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="79284-104">Возвращает строку.</span><span class="sxs-lookup"><span data-stu-id="79284-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="79284-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79284-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="79284-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79284-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79284-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79284-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="79284-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="79284-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="79284-109">Unique identifier.</span></span> <span data-ttu-id="79284-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="79284-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="79284-111">*ппстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79284-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79284-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="79284-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79284-113">Возвращает строку, определяемую параметром Хпараметер.</span><span class="sxs-lookup"><span data-stu-id="79284-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79284-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79284-114">Return value</span></span>

<span data-ttu-id="79284-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79284-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79284-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="79284-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="79284-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="79284-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="79284-118">Требования</span><span class="sxs-lookup"><span data-stu-id="79284-118">Requirements</span></span>



| <span data-ttu-id="79284-119">Требование</span><span class="sxs-lookup"><span data-stu-id="79284-119">Requirement</span></span> | <span data-ttu-id="79284-120">Значение</span><span class="sxs-lookup"><span data-stu-id="79284-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79284-121">Header</span><span class="sxs-lookup"><span data-stu-id="79284-121">Header</span></span><br/>  | <dl> <span data-ttu-id="79284-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="79284-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="79284-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79284-123">Library</span></span><br/> | <dl> <span data-ttu-id="79284-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79284-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79284-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79284-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79284-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="79284-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="79284-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="79284-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
