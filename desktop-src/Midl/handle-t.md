---
title: атрибут handle_t
description: '\_Ключевое слово Handle t объявляет объект для типа маркера-примитива с типом \_ t. Простой маркер привязки — это объект данных, который может использоваться приложением для представления привязки.'
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t атрибута MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337057"
---
# <a name="handle_t-attribute"></a>Handle \_ t, атрибут

Ключевое слово **Handle \_ t** объявляет объект для типа маркера-примитива с **типом \_ t**. Простой маркер привязки — это объект данных, который может использоваться приложением для представления привязки.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Параметры

Этот атрибут не имеет параметров.

## <a name="remarks"></a>Комментарии

Тип **« \_ Handle** » является одним из предопределенных типов языка определения интерфейса (IDL). Он может использоваться в качестве спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в качестве спецификатора возвращаемого типа функции и описателя типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

В Microsoft RPC параметры типа **Handle \_ t** могут происходить только в качестве параметров **\[** [**in**](in.md) **\]** . У примитивных дескрипторов не может быть **\[** атрибута [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** .

Параметры типа **Handle \_ t** (Параметры обработчика примитива) не передаются в сети.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[Привязка и дескрипторы](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**окне**](in.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**однозначно**](unique.md)
</dt> </dl>

 

 