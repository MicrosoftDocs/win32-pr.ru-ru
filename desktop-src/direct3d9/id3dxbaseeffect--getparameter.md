---
description: Возвращает маркер параметра верхнего уровня или параметра-члена структуры.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: Метод ID3DXBaseEffect::-Parameter (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081944"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="beb4d-103">Метод ID3DXBaseEffect:: Parameter</span><span class="sxs-lookup"><span data-stu-id="beb4d-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="beb4d-104">Возвращает маркер параметра верхнего уровня или параметра-члена структуры.</span><span class="sxs-lookup"><span data-stu-id="beb4d-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beb4d-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="beb4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="beb4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb4d-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb4d-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="beb4d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="beb4d-109">Маркер параметра или **значение NULL** для параметров верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="beb4d-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="beb4d-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="beb4d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="beb4d-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb4d-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="beb4d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="beb4d-113">Индекс параметра.</span><span class="sxs-lookup"><span data-stu-id="beb4d-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb4d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb4d-114">Return value</span></span>

<span data-ttu-id="beb4d-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="beb4d-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="beb4d-116">Возвращает маркер указанного параметра или **значение NULL** , если индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="beb4d-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="beb4d-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="beb4d-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="beb4d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="beb4d-118">Requirements</span></span>



| <span data-ttu-id="beb4d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="beb4d-119">Requirement</span></span> | <span data-ttu-id="beb4d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="beb4d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4d-121">Header</span><span class="sxs-lookup"><span data-stu-id="beb4d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="beb4d-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="beb4d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="beb4d-123">Library</span></span><br/> | <dl> <span data-ttu-id="beb4d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="beb4d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beb4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4d-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="beb4d-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
