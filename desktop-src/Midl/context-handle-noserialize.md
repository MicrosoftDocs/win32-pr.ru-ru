---
title: атрибут context_handle_noserialize
description: Атрибут \ context \_ дескриптора \_ NONSERIALIZED \ ACF гарантирует, что дескриптор контекста не будет сериализован, независимо от поведения приложения по умолчанию.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize атрибута MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789871"
---
# <a name="context_handle_noserialize-attribute"></a>\_атрибут несериализации контекстного обработчика \_

Атрибут ACF **\[ \_ дескриптора \_ \] несериализации** гарантирует, что дескриптор контекста не будет сериализован, независимо от поведения приложения по умолчанию.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Type-ACF-Attribute-List* 
</dt> <dd>

Любые другие атрибуты ACF, применяемые к типу.

</dd> <dt>

*Контекстный-Handle-тип* 
</dt> <dd>

Идентификатор, указывающий тип обработчика контекста, как определено в объявлении [**typedef**](typedef.md) . Это тип, который получает атрибут [**\[ \_ Handle \] для контекста**](context-handle.md) в IDL-файле.

</dd> <dt>

*Функция-ACF-Attribute-List* 
</dt> <dd>

Любые дополнительные атрибуты ACF, применяемые к функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя функции, определенное в IDL-файле.

</dd> <dt>

*параметр-ACF-Attribute-List* 
</dt> <dd>

Любые другие атрибуты ACF, применяемые к параметру.

</dd> <dt>

*Param-Name* 
</dt> <dd>

Имя параметра, определенное в IDL-файле.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут [**\[ \_ Handle \] контекста**](context-handle.md) определяет маркер привязки, который сохраняет контекст или сведения о состоянии на сервере между вызовами удаленных процедур. Атрибут может отображаться как атрибут типа IDL [**typedef**](typedef.md) , как атрибут типа возвращаемого значения функции, или как атрибут параметра.

По умолчанию вызовы дескрипторов контекста сериализуются. Приложение может вызвать [**рпкссдонтсериализеконтекст**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) , чтобы переопределить это поведение по умолчанию. Использование атрибута [**\[ \_ дескриптора \] контекста**](context-handle.md) в файле ACF гарантирует, что вызовы в данном конкретном дескрипторе контекста не будут сериализованы независимо от поведения вызывающего приложения. Предоставление подпрограммы очистки контекста является необязательным.

Этот атрибут доступен в MIDL версии 5,0.

**Windows server 2003 и Windows XP или более поздней версии:** Один интерфейс может разрешать как сериализованные, так и несериализованные дескрипторы контекста, что позволяет одному методу интерфейса получить доступ к дескриптору контекста исключительно (сериализованный), а другие методы — к этому дескриптору контекста в общем режиме (не сериализованном). Эти возможности доступа сравнимы с механизмами блокировки чтения и записи. методы, использующие сериализованный контекстный маркер, являются эксклюзивными пользователями (модулями записи), тогда как методы, использующие несериализованный контекст контекста, являются общими пользователями (читателями). Методы, которые удаляют или изменяют состояние обработчика контекста, должны быть сериализованы. Методы, которые не изменяют состояние маркера контекста, например методы, которые просто считывают из обработчика контекста, могут быть несериализуемыми. Обратите внимание, что методы создания неявно сериализуются.

## <a name="examples"></a>Примеры

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты ACF](acf-attributes.md)
</dt> <dt>

[**\_сериализация обработчика контекста \_**](context-handle-serialize.md)
</dt> <dt>

[**Контекстный \_ маркер**](context-handle.md)
</dt> <dt>

[Дескрипторы контекста](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**рпкссдонтсериализеконтекст**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Подпрограммы запуска контекста сервера](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Многопоточные клиенты и дескрипторы контекста](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 