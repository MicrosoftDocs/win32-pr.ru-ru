---
description: Возвращает маркер заметки путем поиска ее имени.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Метод ID3DXBaseEffect:: Жетаннотатионбинаме (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694322"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="e3f34-103">Метод ID3DXBaseEffect:: Жетаннотатионбинаме</span><span class="sxs-lookup"><span data-stu-id="e3f34-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="e3f34-104">Возвращает маркер заметки путем поиска ее имени.</span><span class="sxs-lookup"><span data-stu-id="e3f34-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f34-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3f34-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="e3f34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f34-107">*хобжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3f34-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f34-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e3f34-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e3f34-109">Маркер метода, этапа или параметра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="e3f34-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="e3f34-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e3f34-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3f34-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3f34-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f34-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3f34-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3f34-113">Строка, содержащая имя заметки.</span><span class="sxs-lookup"><span data-stu-id="e3f34-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f34-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3f34-114">Return value</span></span>

<span data-ttu-id="e3f34-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e3f34-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e3f34-116">Возвращает маркер указанной заметки или **значение NULL** , если имя не найдено.</span><span class="sxs-lookup"><span data-stu-id="e3f34-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="e3f34-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e3f34-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f34-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e3f34-118">Requirements</span></span>



| <span data-ttu-id="e3f34-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e3f34-119">Requirement</span></span> | <span data-ttu-id="e3f34-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e3f34-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f34-121">Header</span><span class="sxs-lookup"><span data-stu-id="e3f34-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e3f34-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f34-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e3f34-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3f34-123">Library</span></span><br/> | <dl> <span data-ttu-id="e3f34-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3f34-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e3f34-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3f34-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f34-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e3f34-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
