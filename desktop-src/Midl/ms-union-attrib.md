---
title: ms_union - атрибут
description: '\_Для управления выравниванием ОНД неинкапсулированных объединений используется ключевое слово \ MS Union \.'
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union атрибута MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068828"
---
# <a name="ms_union-attribute"></a>\_атрибут MS Union

Ключевое слово \[ **MS \_ Union** \] используется для управления выравниванием ОНД неинкапсулированных объединений.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

*тип процедуры* 
</dt> <dd>

Указывает тип возвращаемого значения процедуры, к которой применяется атрибут.

</dd> <dt>

*имя процедуры* 
</dt> <dd>

Указывает имя процедуры.

</dd> <dt>

*Param-List* 
</dt> <dd>

Указывает список параметров процедуры, который может быть пустым.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Никогда не используйте этот параметр или атрибут с новыми интерфейсами. Это функция обратной совместимости. Компилятор MIDL в этой версии Microsoft RPC отражает поведение компилятора использование DCE IDL для неинкапсулированных объединений. Однако, поскольку более ранние версии компилятора MIDL не сделали этого, коммутатор [**/МС \_ Union**](-ms-union.md) обеспечивает совместимость с интерфейсами, созданными в предыдущих версиях компилятора MIDL.

Функцию **MS \_ Union** можно использовать в качестве атрибута интерфейса IDL, атрибута типа IDL или в качестве параметра командной строки ( [**/МС \_ Union**](-ms-union.md)).

## <a name="examples"></a>Примеры

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_объединение/МС**](-ms-union.md)
</dt> </dl>

 

 




