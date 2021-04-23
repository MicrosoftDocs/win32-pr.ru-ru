---
description: Задает логическое значение.
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: 'Метод ID3DXBaseEffect:: Сетбул (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be137ac210297b9fce12dafaffb6fead61d39512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713455"
---
# <a name="id3dxbaseeffectsetbool-method"></a><span data-ttu-id="8cf9a-103">Метод ID3DXBaseEffect:: Сетбул</span><span class="sxs-lookup"><span data-stu-id="8cf9a-103">ID3DXBaseEffect::SetBool method</span></span>

<span data-ttu-id="8cf9a-104">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="8cf9a-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cf9a-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="8cf9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cf9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf9a-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cf9a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf9a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8cf9a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8cf9a-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8cf9a-109">Unique identifier.</span></span> <span data-ttu-id="8cf9a-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8cf9a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cf9a-111">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8cf9a-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf9a-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cf9a-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cf9a-113">.</span><span class="sxs-lookup"><span data-stu-id="8cf9a-113">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf9a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cf9a-114">Return value</span></span>

<span data-ttu-id="8cf9a-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cf9a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cf9a-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8cf9a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cf9a-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="8cf9a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf9a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8cf9a-118">Requirements</span></span>



| <span data-ttu-id="8cf9a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8cf9a-119">Requirement</span></span> | <span data-ttu-id="8cf9a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf9a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf9a-121">Header</span><span class="sxs-lookup"><span data-stu-id="8cf9a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8cf9a-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf9a-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8cf9a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8cf9a-123">Library</span></span><br/> | <dl> <span data-ttu-id="8cf9a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cf9a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8cf9a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cf9a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf9a-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8cf9a-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8cf9a-127">**Bool**</span><span class="sxs-lookup"><span data-stu-id="8cf9a-127">**GetBool**</span></span>](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 
