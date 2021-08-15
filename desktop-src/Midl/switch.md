---
title: переключить атрибут
description: Ключевое слово Switch выбирает discriminant для инкапсулированного \_ объединения.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- параметр атрибута MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422b52a339a83cbaf59a9d65c0ed0e4e7e41533dcbf0be962147327145588a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013552"
---
# <a name="switch-attribute"></a>переключить атрибут

Ключевое слово **switch** выбирает discriminant для [**инкапсулированного \_ объединения**](encapsulated-unions.md).

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Тип переключателя* 
</dt> <dd>

Задает тип [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) или идентификатор, который разрешается в один из этих типов.

</dd> <dt>

*имя коммутатора* 
</dt> <dd>

Задает имя переменной *типа Switch-Type* , которая выступает в качестве discriminant объединения.

</dd> </dl>

## <a name="examples"></a>Примеры

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Неинкапсулированные объединения](nonencapsulated-unions.md)
</dt> <dt>

[**параметр \_ имеет**](switch-is.md)
</dt> <dt>

[**Тип коммутатора \_**](switch-type.md)
</dt> <dt>

[**наборов**](union.md)
</dt> </dl>

 

 




