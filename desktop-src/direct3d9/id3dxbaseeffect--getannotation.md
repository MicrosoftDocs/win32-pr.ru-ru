---
description: Возвращает маркер заметки.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: Метод ID3DXBaseEffect::-annotation (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714000"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="83436-103">Метод ID3DXBaseEffect:: annotation</span><span class="sxs-lookup"><span data-stu-id="83436-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="83436-104">Возвращает маркер заметки.</span><span class="sxs-lookup"><span data-stu-id="83436-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="83436-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83436-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="83436-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83436-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83436-107">*хобжект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83436-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83436-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="83436-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="83436-109">Маркер метода, этапа или параметра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="83436-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="83436-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="83436-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="83436-111">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83436-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83436-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83436-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83436-113">Индекс заметки.</span><span class="sxs-lookup"><span data-stu-id="83436-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83436-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83436-114">Return value</span></span>

<span data-ttu-id="83436-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="83436-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="83436-116">Возвращает маркер указанной заметки или **значение NULL** , если индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="83436-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="83436-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="83436-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="83436-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83436-118">Remarks</span></span>

<span data-ttu-id="83436-119">Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или.</span><span class="sxs-lookup"><span data-stu-id="83436-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="83436-120">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="83436-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83436-121">Требования</span><span class="sxs-lookup"><span data-stu-id="83436-121">Requirements</span></span>



| <span data-ttu-id="83436-122">Требование</span><span class="sxs-lookup"><span data-stu-id="83436-122">Requirement</span></span> | <span data-ttu-id="83436-123">Значение</span><span class="sxs-lookup"><span data-stu-id="83436-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83436-124">Header</span><span class="sxs-lookup"><span data-stu-id="83436-124">Header</span></span><br/>  | <dl> <span data-ttu-id="83436-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="83436-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="83436-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83436-126">Library</span></span><br/> | <dl> <span data-ttu-id="83436-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83436-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="83436-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83436-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83436-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="83436-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
