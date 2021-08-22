---
title: атрибут strict_context_handle
description: Атрибут \ " \_ \_ дескриптор контекста \ ACF \" задает ограничения для дескрипторов контекста.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle атрибута MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013582"
---
# <a name="strict_context_handle-attribute"></a>атрибут с определенным \_ \_ маркером контекста

Атрибут ACF **\[ \_ \_ дескриптора \] ограниченного контекста** задает ограничения для дескрипторов контекста.

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Другие атрибуты ACF, применяемые к интерфейсу в целом. К допустимым атрибутам относятся [**Auto \_ Handle**](auto-handle.md), [**неявный \_ обработчик**](implicit-handle.md), [**явный \_ обработчик**](explicit-handle.md)и [**Оптимизация**](optimize.md), [**код**](code.md)или [**код**](nocode.md). Несколько атрибутов разделяются запятыми.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Имя интерфейса.

</dd> <dt>

*Interface-операторы определения* 
</dt> <dd>

Одна или несколько инструкций MIDL, определяющих элементы [**интерфейса**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Как правило, когда вызов метода интерфейса создает маркер контекста, этот обработчик освобождается бесплатно для любого другого интерфейса. При использовании атрибута исключительного **\[ \_ \_ дескриптора \] контекста** гарантируется, что методы в этом интерфейсе будут принимать только дескрипторы контекста, созданные методом из того же интерфейса. Интерфейсы, скомпилированные без использования **\[ \_ \_ дескриптора \]** с определенными контекстами, не могут принимать дескрипторы контекста, созданные для интерфейсов, **\[ \_ \_ \] скомпилированных с помощью**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**приведен**](code.md)
</dt> <dt>

[Дескрипторы контекста](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_сериализация обработчика контекста \_**](context-handle-serialize.md)
</dt> <dt>

[**несериализуемый контекстный \_ обработчик \_**](context-handle-noserialize.md)
</dt> <dt>

[**явный \_ маркер**](explicit-handle.md)
</dt> <dt>

[**неявный \_ обработчик**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**увеличить**](optimize.md)
</dt> <dt>

[Тип \_ строгого \_ \_ маркера контекста](type-strict-context-handle.md)
</dt> </dl>

 

 