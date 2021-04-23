---
description: Задает строку.
ms.assetid: 7e8eef70-85ee-461d-bf8c-44cda5f184cd
title: 'Метод ID3DXBaseEffect:: SetString (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a7c4f86c6b7fa78c869eb1d5bd49634ec4b496d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720860"
---
# <a name="id3dxbaseeffectsetstring-method"></a><span data-ttu-id="f3329-103">Метод ID3DXBaseEffect:: SetString</span><span class="sxs-lookup"><span data-stu-id="f3329-103">ID3DXBaseEffect::SetString method</span></span>

<span data-ttu-id="f3329-104">Задает строку.</span><span class="sxs-lookup"><span data-stu-id="f3329-104">Sets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3329-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3329-105">Syntax</span></span>


```C++
HRESULT SetString(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pString
);
```



## <a name="parameters"></a><span data-ttu-id="f3329-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3329-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3329-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3329-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f3329-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f3329-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f3329-109">Unique identifier.</span></span> <span data-ttu-id="f3329-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f3329-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3329-111">*пстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3329-111">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3329-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3329-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3329-113">Строка, которую необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="f3329-113">String to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3329-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3329-114">Return value</span></span>

<span data-ttu-id="f3329-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3329-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3329-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f3329-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f3329-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f3329-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3329-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f3329-118">Requirements</span></span>



| <span data-ttu-id="f3329-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f3329-119">Requirement</span></span> | <span data-ttu-id="f3329-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f3329-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3329-121">Header</span><span class="sxs-lookup"><span data-stu-id="f3329-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f3329-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3329-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f3329-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3329-123">Library</span></span><br/> | <dl> <span data-ttu-id="f3329-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3329-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f3329-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3329-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3329-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f3329-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f3329-127">**GetString**</span><span class="sxs-lookup"><span data-stu-id="f3329-127">**GetString**</span></span>](id3dxbaseeffect--getstring.md)
</dt> </dl>

 

 
