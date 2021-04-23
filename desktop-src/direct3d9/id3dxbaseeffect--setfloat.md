---
description: Устанавливает значение с плавающей запятой.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'Метод ID3DXBaseEffect:: SetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: af955748fff66e67e0e2f5650b869a746168de54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914696"
---
# <a name="id3dxbaseeffectsetfloat-method"></a><span data-ttu-id="2669b-103">Метод ID3DXBaseEffect:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="2669b-103">ID3DXBaseEffect::SetFloat method</span></span>

<span data-ttu-id="2669b-104">Устанавливает значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2669b-104">Sets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2669b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2669b-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="2669b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2669b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2669b-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2669b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2669b-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2669b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2669b-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2669b-109">Unique identifier.</span></span> <span data-ttu-id="2669b-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2669b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2669b-111">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2669b-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2669b-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2669b-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2669b-113">Значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2669b-113">Floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2669b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2669b-114">Return value</span></span>

<span data-ttu-id="2669b-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2669b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2669b-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2669b-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2669b-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2669b-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2669b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2669b-118">Requirements</span></span>



| <span data-ttu-id="2669b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2669b-119">Requirement</span></span> | <span data-ttu-id="2669b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2669b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2669b-121">Header</span><span class="sxs-lookup"><span data-stu-id="2669b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2669b-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2669b-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2669b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2669b-123">Library</span></span><br/> | <dl> <span data-ttu-id="2669b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2669b-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2669b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2669b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2669b-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2669b-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="2669b-127">**GetFloat**</span><span class="sxs-lookup"><span data-stu-id="2669b-127">**GetFloat**</span></span>](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
