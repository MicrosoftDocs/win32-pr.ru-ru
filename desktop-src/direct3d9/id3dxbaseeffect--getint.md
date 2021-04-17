---
description: Возвращает целое число.
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: 'Метод ID3DXBaseEffect:: GetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c0fe1fa01260be936b9d7f8be394d0c43a781680
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703993"
---
# <a name="id3dxbaseeffectgetint-method"></a><span data-ttu-id="cd2fa-103">Метод ID3DXBaseEffect:: GetInt</span><span class="sxs-lookup"><span data-stu-id="cd2fa-103">ID3DXBaseEffect::GetInt method</span></span>

<span data-ttu-id="cd2fa-104">Возвращает целое число.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-104">Gets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd2fa-105">Syntax</span></span>


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a><span data-ttu-id="cd2fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd2fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2fa-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd2fa-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fa-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cd2fa-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-109">Unique identifier.</span></span> <span data-ttu-id="cd2fa-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="cd2fa-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2fa-111">*PN* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cd2fa-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fa-112">Тип: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd2fa-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cd2fa-113">Возвращает целое число.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-113">Returns an integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2fa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd2fa-114">Return value</span></span>

<span data-ttu-id="cd2fa-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd2fa-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd2fa-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd2fa-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="cd2fa-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2fa-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cd2fa-118">Requirements</span></span>



| <span data-ttu-id="cd2fa-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cd2fa-119">Requirement</span></span> | <span data-ttu-id="cd2fa-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2fa-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2fa-121">Header</span><span class="sxs-lookup"><span data-stu-id="cd2fa-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd2fa-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fa-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cd2fa-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd2fa-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd2fa-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fa-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cd2fa-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd2fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2fa-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="cd2fa-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cd2fa-127">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="cd2fa-127">**SetInt**</span></span>](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 
