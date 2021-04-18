---
title: атрибут void
description: Базовый тип void указывает на процедуру без аргументов или процедуру, которая не возвращает результирующее значение.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void Attribute, MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661667"
---
# <a name="void-attribute"></a>атрибут void

Базовый тип **void** указывает на процедуру без аргументов или процедуру, которая не возвращает результирующее значение.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя функции* 
</dt> <dd>

Задает имя удаленной процедуры.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Указывает список параметров, передаваемых в функцию вместе со связанными типами параметров и атрибутами параметров.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Указывает имя типа, возвращаемого функцией.

</dd> <dt>

*Контекстный-Handle-тип* 
</dt> <dd>

Указывает имя типа, который принимает **\[** атрибут [**\_ Handle**](context-handle.md) **\]** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Тип указателя **void \***, который в C описывает универсальный указатель, который может быть приведен для представления любого типа указателя, ограничен в MIDL для его использования с ключевым словом **\[ \_ Handle \] context** .

## <a name="examples"></a>Примеры

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**Контекстный \_ маркер**](context-handle.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




