---
description: Ошибки представлены отрицательными значениями и не могут быть объединены.
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: Перечисление D3DX10_ERR (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 098c15999f20a65614d642029b1d1f6e0b600db6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273732"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="24c82-103">\_Перечисление Err D3DX10</span><span class="sxs-lookup"><span data-stu-id="24c82-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="24c82-104">Ошибки представлены отрицательными значениями и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="24c82-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="24c82-105">Ниже приведен список значений, которые могут возвращаться методами, включенными в библиотеку служебной программы D3DX.</span><span class="sxs-lookup"><span data-stu-id="24c82-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="24c82-106">Список значений, которые могут быть возвращены, см. в описании отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="24c82-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="24c82-107">Эти списки не обязательно являются исчерпывающими.</span><span class="sxs-lookup"><span data-stu-id="24c82-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24c82-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="24c82-109">Константы</span><span class="sxs-lookup"><span data-stu-id="24c82-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="24c82-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ Err \_ не \_ может \_ изменить \_ буфер индексов**</span><span class="sxs-lookup"><span data-stu-id="24c82-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-111">Невозможно изменить буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="24c82-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ Err \_ Недопустимая \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="24c82-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-113">Недопустимая сетка.</span><span class="sxs-lookup"><span data-stu-id="24c82-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ Err \_ не \_ может \_ Сортировать attr**</span><span class="sxs-lookup"><span data-stu-id="24c82-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-115">Сортировка атрибутов (D3DXMESHOPT \_ аттрсорт) не поддерживается в качестве метода оптимизации.</span><span class="sxs-lookup"><span data-stu-id="24c82-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**\_ \_ Обложка D3DX10 Err \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="24c82-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-117">Выбор обложки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="24c82-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**\_ \_ Слишком \_ большое \_ влияние на D3DX10 Err**</span><span class="sxs-lookup"><span data-stu-id="24c82-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-119">Указано слишком много влияния.</span><span class="sxs-lookup"><span data-stu-id="24c82-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**\_ \_ Недопустимые \_ данные D3DX10 Err**</span><span class="sxs-lookup"><span data-stu-id="24c82-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-121">Недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="24c82-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**В \_ сети, загруженной в D3DX10 Err, \_ \_ \_ \_ нет \_ данных**</span><span class="sxs-lookup"><span data-stu-id="24c82-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-123">Сетка не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="24c82-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ Err \_ дублирует \_ именованный \_ фрагмент**</span><span class="sxs-lookup"><span data-stu-id="24c82-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-125">Фрагмент с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="24c82-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="24c82-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ Err \_ не может \_ удалить \_ последний \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="24c82-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="24c82-127">Последний элемент не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="24c82-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24c82-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24c82-128">Remarks</span></span>

<span data-ttu-id="24c82-129">Код устройства \_ факдд используется для создания кодов ошибок, как в следующих макросах.</span><span class="sxs-lookup"><span data-stu-id="24c82-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="24c82-130">Требования</span><span class="sxs-lookup"><span data-stu-id="24c82-130">Requirements</span></span>



| <span data-ttu-id="24c82-131">Требование</span><span class="sxs-lookup"><span data-stu-id="24c82-131">Requirement</span></span> | <span data-ttu-id="24c82-132">Значение</span><span class="sxs-lookup"><span data-stu-id="24c82-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="24c82-133">Header</span><span class="sxs-lookup"><span data-stu-id="24c82-133">Header</span></span><br/> | <dl> <span data-ttu-id="24c82-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="24c82-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c82-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24c82-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c82-136">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="24c82-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




