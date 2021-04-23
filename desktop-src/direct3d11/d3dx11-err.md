---
title: Перечисление D3DX11_ERR (D3DX11. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Ошибки представлены отрицательными значениями и не могут быть объединены.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Перечисление D3DX11_ERR Direct3D 11
- Указатель перечисления LPD3DX11_ERR Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998690"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="a970e-106">\_Перечисление Err D3DX11</span><span class="sxs-lookup"><span data-stu-id="a970e-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="a970e-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="a970e-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="a970e-108">Ошибки представлены отрицательными значениями и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="a970e-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="a970e-109">Ниже приведен список значений, которые могут возвращаться методами, включенными в библиотеку служебной программы D3DX.</span><span class="sxs-lookup"><span data-stu-id="a970e-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="a970e-110">Список значений, которые могут быть возвращены, см. в описании отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="a970e-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="a970e-111">Эти списки не обязательно являются исчерпывающими.</span><span class="sxs-lookup"><span data-stu-id="a970e-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a970e-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a970e-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="a970e-113">Константы</span><span class="sxs-lookup"><span data-stu-id="a970e-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a970e-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ не \_ может \_ изменить \_ буфер индексов**</span><span class="sxs-lookup"><span data-stu-id="a970e-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-115">Невозможно изменить буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="a970e-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ Err \_ Недопустимая \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="a970e-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-117">Недопустимая сетка.</span><span class="sxs-lookup"><span data-stu-id="a970e-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ не \_ может \_ Сортировать attr**</span><span class="sxs-lookup"><span data-stu-id="a970e-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-119">Сортировка атрибутов (D3DXMESHOPT \_ аттрсорт) не поддерживается в качестве метода оптимизации.</span><span class="sxs-lookup"><span data-stu-id="a970e-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_ \_ Обложка D3DX11 Err \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="a970e-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-121">Выбор обложки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a970e-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**\_ \_ Слишком \_ большое \_ влияние на D3DX11 Err**</span><span class="sxs-lookup"><span data-stu-id="a970e-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-123">Указано слишком много влияния.</span><span class="sxs-lookup"><span data-stu-id="a970e-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**\_ \_ Недопустимые \_ данные D3DX11 Err**</span><span class="sxs-lookup"><span data-stu-id="a970e-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-125">Недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="a970e-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**В \_ сети, загруженной в D3DX11 Err, \_ \_ \_ \_ нет \_ данных**</span><span class="sxs-lookup"><span data-stu-id="a970e-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-127">Сетка не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="a970e-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ Err \_ дублирует \_ именованный \_ фрагмент**</span><span class="sxs-lookup"><span data-stu-id="a970e-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-129">Фрагмент с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="a970e-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a970e-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ не может \_ удалить \_ последний \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="a970e-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="a970e-131">Последний элемент не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="a970e-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a970e-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="a970e-132">Remarks</span></span>

<span data-ttu-id="a970e-133">Код устройства \_ факдд используется для создания кодов ошибок, как в следующих макросах.</span><span class="sxs-lookup"><span data-stu-id="a970e-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="a970e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a970e-134">Requirements</span></span>



| <span data-ttu-id="a970e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a970e-135">Requirement</span></span> | <span data-ttu-id="a970e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a970e-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a970e-137">Header</span><span class="sxs-lookup"><span data-stu-id="a970e-137">Header</span></span><br/> | <dl> <span data-ttu-id="a970e-138"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="a970e-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a970e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a970e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a970e-140">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="a970e-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





