---
title: switch_type - атрибут
description: Атрибут \ Switch \_ Type \ определяет тип переменной, используемой в качестве discriminant объединения. Тип переключателя может быть целым числом, символом, логическим значением или типом перечисления.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type атрибута MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889691"
---
# <a name="switch_type-attribute"></a>\_атрибут типа Switch

Атрибут **\[ \_ типа \] switch** определяет тип переменной, используемой в качестве discriminant объединения. Тип переключателя может быть целым числом, символом, логическим значением или типом перечисления.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*спецификатор типа-Switch* 
</dt> <dd>

Задает тип [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)или [**enum**](enum.md) или идентификатор такого типа.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В то время как атрибут **\[ \_ типа \] switch** определяет тип переменной, параметр **\[** [**\_ —**](switch-is.md) **\]** Attribute указывает имя параметра, который является discriminant объединения. Атрибут **\[ \_ типа \] switch** применяется к параметрам или элементам структур или объединений.

Объединение и его discriminant должны быть указаны на том же логическом уровне. Если Union является параметром, discriminant объединения должен быть другим параметром. Если объединение является полем структуры, discriminant должно быть другим полем структуры на том же уровне, что и поле Union.

## <a name="examples"></a>Примеры

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Логическая**](boolean.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Инкапсулированные объединения](encapsulated-unions.md)
</dt> <dt>

[**перечисления**](enum.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[Неинкапсулированные объединения](nonencapsulated-unions.md)
</dt> <dt>

[**параметр \_ имеет**](switch-is.md)
</dt> <dt>

[**наборов**](union.md)
</dt> </dl>

 

 




