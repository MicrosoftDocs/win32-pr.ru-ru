---
title: пропустить атрибут
description: Атрибут \ Ignore \ указывает, что указатель, содержащийся в структуре или объединении, и на объект, указанный указателем, не передается. Атрибут \ Ignore \ ограничен элементами-указателями структур или объединений.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- игнорировать атрибут MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890513"
---
# <a name="ignore-attribute"></a>пропустить атрибут

Атрибут **\[ Ignore \]** указывает, что указатель, содержащийся в структуре или объединении, и на объект, указанный указателем, не передается. Атрибут **\[ Ignore \]** ограничен элементами-указателями структур или объединений.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*pointer-член-тип* 
</dt> <dd>

Задает тип элемента указателя структуры или объединения.

</dd> <dt>

*имя указателя* 
</dt> <dd>

Задает имя элемента указателя, который должен игнорироваться во время маршалирования.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Значение элемента структуры с атрибутом **\[ Ignore \]** не определено в месте назначения. Параметр **\[** [**in**](in.md) **\]** не определен на удаленном компьютере. Параметр **\[** [**out**](out-idl.md) **\]** не определен на локальном компьютере.

Атрибут **\[ Ignore \]** позволяет предотвратить передачу данных. Это полезно в таких ситуациях, как список с двойным связыванием. В следующем примере представлен список с двойным связыванием, в котором вводятся псевдонимы данных.

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

Присвоение псевдонимов происходит в предыдущем примере, так как та же область памяти доступна из двух различных указателей в функции **p** и **p->Next->**.

Обратите внимание, что **\[ Ignore \]** не может использоваться в качестве атрибута типа.

## <a name="examples"></a>Примеры

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты массива и Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**массивы**](arrays-1.md)
</dt> <dt>

[Массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**окне**](in.md)
</dt> <dt>

[**заполняет**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**однозначно**](unique.md)
</dt> </dl>

 

 