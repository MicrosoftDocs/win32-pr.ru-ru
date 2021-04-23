---
description: Возвращает маркер прохода путем поиска его имени.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'Метод ID3DXBaseEffect:: Жетпассбинаме (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713993"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="5e761-103">Метод ID3DXBaseEffect:: Жетпассбинаме</span><span class="sxs-lookup"><span data-stu-id="5e761-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="5e761-104">Возвращает маркер прохода путем поиска его имени.</span><span class="sxs-lookup"><span data-stu-id="5e761-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e761-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e761-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="5e761-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e761-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e761-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e761-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5e761-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5e761-109">Маркер родительского метода.</span><span class="sxs-lookup"><span data-stu-id="5e761-109">Handle of the parent technique.</span></span> <span data-ttu-id="5e761-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5e761-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e761-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e761-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e761-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e761-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e761-113">Строка, содержащая имя этапа.</span><span class="sxs-lookup"><span data-stu-id="5e761-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e761-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e761-114">Return value</span></span>

<span data-ttu-id="5e761-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5e761-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5e761-116">Возвращает маркер первого прохода в указанном методе с указанным именем или **значение NULL** , если имя не найдено.</span><span class="sxs-lookup"><span data-stu-id="5e761-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="5e761-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5e761-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e761-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5e761-118">Requirements</span></span>



| <span data-ttu-id="5e761-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5e761-119">Requirement</span></span> | <span data-ttu-id="5e761-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5e761-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e761-121">Header</span><span class="sxs-lookup"><span data-stu-id="5e761-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5e761-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e761-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5e761-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e761-123">Library</span></span><br/> | <dl> <span data-ttu-id="5e761-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e761-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5e761-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e761-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e761-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5e761-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
