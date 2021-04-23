---
description: Возвращает маркер параметра верхнего уровня или параметра-члена структуры путем поиска его семантики с поиском без учета регистра.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Метод ID3DXBaseEffect:: Жетпараметербисемантик (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355880"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="567e7-103">Метод ID3DXBaseEffect:: Жетпараметербисемантик</span><span class="sxs-lookup"><span data-stu-id="567e7-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="567e7-104">Возвращает маркер параметра верхнего уровня или параметра-члена структуры путем поиска его семантики с поиском без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="567e7-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="567e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="567e7-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="567e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="567e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567e7-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="567e7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567e7-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="567e7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="567e7-109">Маркер параметра или **значение NULL** для параметров верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="567e7-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="567e7-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="567e7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="567e7-111">*псемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="567e7-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567e7-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="567e7-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="567e7-113">Строка, содержащая имя семантики.</span><span class="sxs-lookup"><span data-stu-id="567e7-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567e7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="567e7-114">Return value</span></span>

<span data-ttu-id="567e7-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="567e7-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="567e7-116">Возвращает маркер первого параметра, который соответствует заданной семантике, или **значение NULL** , если семантика не была найдена.</span><span class="sxs-lookup"><span data-stu-id="567e7-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="567e7-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="567e7-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="567e7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="567e7-118">Requirements</span></span>



| <span data-ttu-id="567e7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="567e7-119">Requirement</span></span> | <span data-ttu-id="567e7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="567e7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="567e7-121">Header</span><span class="sxs-lookup"><span data-stu-id="567e7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="567e7-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="567e7-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="567e7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="567e7-123">Library</span></span><br/> | <dl> <span data-ttu-id="567e7-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="567e7-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="567e7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="567e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567e7-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="567e7-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
