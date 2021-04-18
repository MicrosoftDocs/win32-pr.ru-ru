---
description: Возвращает маркер метода путем поиска его имени.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'Метод ID3DXBaseEffect:: Жеттечникуебинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713989"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="f8dcc-103">Метод ID3DXBaseEffect:: Жеттечникуебинаме</span><span class="sxs-lookup"><span data-stu-id="f8dcc-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="f8dcc-104">Возвращает маркер метода путем поиска его имени.</span><span class="sxs-lookup"><span data-stu-id="f8dcc-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8dcc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8dcc-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="f8dcc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8dcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8dcc-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8dcc-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8dcc-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8dcc-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8dcc-109">Строка, содержащая имя метода.</span><span class="sxs-lookup"><span data-stu-id="f8dcc-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8dcc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8dcc-110">Return value</span></span>

<span data-ttu-id="f8dcc-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f8dcc-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f8dcc-112">Возвращает маркер первого метода с указанным именем или **значение NULL** , если имя не найдено.</span><span class="sxs-lookup"><span data-stu-id="f8dcc-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="f8dcc-113">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f8dcc-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dcc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f8dcc-114">Requirements</span></span>



| <span data-ttu-id="f8dcc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f8dcc-115">Requirement</span></span> | <span data-ttu-id="f8dcc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f8dcc-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dcc-117">Header</span><span class="sxs-lookup"><span data-stu-id="f8dcc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f8dcc-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8dcc-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f8dcc-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8dcc-119">Library</span></span><br/> | <dl> <span data-ttu-id="f8dcc-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8dcc-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f8dcc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8dcc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dcc-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f8dcc-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
