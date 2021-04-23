---
description: Возвращает маркер метода.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'Метод ID3DXBaseEffect:: Method (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157251"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="f859a-103">Метод ID3DXBaseEffect:: Method</span><span class="sxs-lookup"><span data-stu-id="f859a-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="f859a-104">Возвращает маркер метода.</span><span class="sxs-lookup"><span data-stu-id="f859a-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="f859a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f859a-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f859a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f859a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f859a-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f859a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f859a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f859a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f859a-109">Индекс методики.</span><span class="sxs-lookup"><span data-stu-id="f859a-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f859a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f859a-110">Return value</span></span>

<span data-ttu-id="f859a-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f859a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f859a-112">Возвращает маркер указанного метода или **значение NULL** , если индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f859a-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="f859a-113">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f859a-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f859a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f859a-114">Requirements</span></span>



| <span data-ttu-id="f859a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f859a-115">Requirement</span></span> | <span data-ttu-id="f859a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f859a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f859a-117">Header</span><span class="sxs-lookup"><span data-stu-id="f859a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f859a-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f859a-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f859a-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f859a-119">Library</span></span><br/> | <dl> <span data-ttu-id="f859a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f859a-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f859a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f859a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f859a-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f859a-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
