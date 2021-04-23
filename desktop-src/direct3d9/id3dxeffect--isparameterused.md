---
description: Определяет, используется ли параметр методом.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'Метод ID3DXEffect:: Испараметерусед (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157147"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="8c3da-103">Метод ID3DXEffect:: Испараметерусед</span><span class="sxs-lookup"><span data-stu-id="8c3da-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="8c3da-104">Определяет, используется ли параметр методом.</span><span class="sxs-lookup"><span data-stu-id="8c3da-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c3da-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="8c3da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c3da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3da-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c3da-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3da-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8c3da-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8c3da-109">Уникальный идентификатор параметра.</span><span class="sxs-lookup"><span data-stu-id="8c3da-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="8c3da-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8c3da-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c3da-111">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c3da-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3da-112">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8c3da-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8c3da-113">Уникальный идентификатор для метода.</span><span class="sxs-lookup"><span data-stu-id="8c3da-113">Unique identifier for the technique.</span></span> <span data-ttu-id="8c3da-114">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8c3da-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3da-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c3da-115">Return value</span></span>

<span data-ttu-id="8c3da-116">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c3da-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c3da-117">Возвращает **значение true** , если параметр используется, и возвращает **значение false** , если параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="8c3da-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8c3da-118">Requirements</span></span>



| <span data-ttu-id="8c3da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8c3da-119">Requirement</span></span> | <span data-ttu-id="8c3da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8c3da-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3da-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c3da-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8c3da-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c3da-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8c3da-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c3da-123">Library</span></span><br/> | <dl> <span data-ttu-id="8c3da-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c3da-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c3da-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c3da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3da-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8c3da-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
