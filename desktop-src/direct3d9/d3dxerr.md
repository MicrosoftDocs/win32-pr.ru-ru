---
description: Ошибки представлены отрицательными значениями и не могут быть объединены.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Перечисление D3DXERR (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273781"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="968f1-103">Перечисление D3DXERR</span><span class="sxs-lookup"><span data-stu-id="968f1-103">D3DXERR enumeration</span></span>

<span data-ttu-id="968f1-104">Ошибки представлены отрицательными значениями и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="968f1-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="968f1-105">Ниже приведен список значений, которые могут возвращаться методами, включенными в библиотеку служебной программы D3DX.</span><span class="sxs-lookup"><span data-stu-id="968f1-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="968f1-106">Список значений, которые могут быть возвращены, см. в описании отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="968f1-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="968f1-107">Эти списки не обязательно являются исчерпывающими.</span><span class="sxs-lookup"><span data-stu-id="968f1-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="968f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="968f1-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="968f1-109">Константы</span><span class="sxs-lookup"><span data-stu-id="968f1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="968f1-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ каннотмодифиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="968f1-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-111">Невозможно изменить буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="968f1-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ инвалидмеш**</span><span class="sxs-lookup"><span data-stu-id="968f1-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-113">Недопустимая сетка.</span><span class="sxs-lookup"><span data-stu-id="968f1-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ каннотаттрсорт**</span><span class="sxs-lookup"><span data-stu-id="968f1-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-115">Сортировка атрибутов (D3DXMESHOPT \_ аттрсорт) не поддерживается в качестве метода оптимизации.</span><span class="sxs-lookup"><span data-stu-id="968f1-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ скиннингнотсуппортед**</span><span class="sxs-lookup"><span data-stu-id="968f1-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-117">Выбор обложки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="968f1-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ туманинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="968f1-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-119">Указано слишком много влияния.</span><span class="sxs-lookup"><span data-stu-id="968f1-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="968f1-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-121">Недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="968f1-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ лоадедмешаснодата**</span><span class="sxs-lookup"><span data-stu-id="968f1-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-123">Сетка не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="968f1-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ дупликатенамедфрагмент**</span><span class="sxs-lookup"><span data-stu-id="968f1-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-125">Фрагмент с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="968f1-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="968f1-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ каннотремовеластитем**</span><span class="sxs-lookup"><span data-stu-id="968f1-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="968f1-127">Последний элемент не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="968f1-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968f1-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="968f1-128">Remarks</span></span>

<span data-ttu-id="968f1-129">Код устройства \_ факдд используется для создания кодов ошибок, как в следующих макросах.</span><span class="sxs-lookup"><span data-stu-id="968f1-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="968f1-130">Требования</span><span class="sxs-lookup"><span data-stu-id="968f1-130">Requirements</span></span>



| <span data-ttu-id="968f1-131">Требование</span><span class="sxs-lookup"><span data-stu-id="968f1-131">Requirement</span></span> | <span data-ttu-id="968f1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="968f1-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="968f1-133">Header</span><span class="sxs-lookup"><span data-stu-id="968f1-133">Header</span></span><br/> | <dl> <span data-ttu-id="968f1-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="968f1-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968f1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="968f1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968f1-136">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="968f1-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




