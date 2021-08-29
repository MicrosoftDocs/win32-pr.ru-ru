---
description: Перечисление D3DXERR — ошибки представлены отрицательными значениями и не могут быть объединены.
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
ms.openlocfilehash: 2fc6f72ab88a3c85eff592e289364a1f67eb9c220a7592397eda14b8bf4aace6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988514"
---
# <a name="d3dxerr-enumeration"></a>Перечисление D3DXERR

Ошибки представлены отрицательными значениями и не могут быть объединены. Ниже приведен список значений, которые могут возвращаться методами, включенными в библиотеку служебной программы D3DX. Список значений, которые могут быть возвращены, см. в описании отдельных методов. Эти списки не обязательно являются исчерпывающими.

## <a name="syntax"></a>Синтаксис


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



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ каннотмодифиндексбуффер**
</dt> <dd>

Невозможно изменить буфер индексов.

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ инвалидмеш**
</dt> <dd>

Недопустимая сетка.

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ каннотаттрсорт**
</dt> <dd>

Сортировка атрибутов (D3DXMESHOPT \_ аттрсорт) не поддерживается в качестве метода оптимизации.

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ скиннингнотсуппортед**
</dt> <dd>

Выбор обложки не поддерживается.

</dd> <dt>

<span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ туманинфлуенцес**
</dt> <dd>

Указано слишком много влияния.

</dd> <dt>

<span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**
</dt> <dd>

Недопустимые данные.

</dd> <dt>

<span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ лоадедмешаснодата**
</dt> <dd>

Сетка не содержит данных.

</dd> <dt>

<span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ дупликатенамедфрагмент**
</dt> <dd>

Фрагмент с таким именем уже существует.

</dd> <dt>

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ каннотремовеластитем**
</dt> <dd>

Последний элемент не может быть удален.

</dd> </dl>

## <a name="remarks"></a>Remarks

Код устройства \_ факдд используется для создания кодов ошибок, как в следующих макросах.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




