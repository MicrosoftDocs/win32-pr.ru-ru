---
description: Возвращает маркер прохода.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'Метод ID3DXBaseEffect:: Pass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424518"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="2206a-103">Метод ID3DXBaseEffect:: Pass</span><span class="sxs-lookup"><span data-stu-id="2206a-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="2206a-104">Возвращает маркер прохода.</span><span class="sxs-lookup"><span data-stu-id="2206a-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="2206a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2206a-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="2206a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2206a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2206a-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2206a-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2206a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2206a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2206a-109">Маркер родительского метода.</span><span class="sxs-lookup"><span data-stu-id="2206a-109">Handle of the parent technique.</span></span> <span data-ttu-id="2206a-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2206a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2206a-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2206a-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2206a-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2206a-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2206a-113">Индекс для прохода.</span><span class="sxs-lookup"><span data-stu-id="2206a-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2206a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2206a-114">Return value</span></span>

<span data-ttu-id="2206a-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2206a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2206a-116">Возвращает маркер указанного прохода внутри указанного метода или **значение NULL** , если индекс был недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2206a-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="2206a-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2206a-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2206a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2206a-118">Requirements</span></span>



| <span data-ttu-id="2206a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2206a-119">Requirement</span></span> | <span data-ttu-id="2206a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2206a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2206a-121">Header</span><span class="sxs-lookup"><span data-stu-id="2206a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2206a-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2206a-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2206a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2206a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2206a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2206a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2206a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2206a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2206a-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2206a-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
