---
title: атрибут ncacn_dnet_nsp
description: '\_ \_ Ключевое слово нкакн днет NSP идентифицирует DECnet в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133838"
---
# <a name="ncacn_dnet_nsp-attribute"></a>нкакн \_ днет \_ NSP, атрибут

Ключевое слово **нкакн \_ днет \_ NSP** идентифицирует DECnet в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя сервера* 
</dt> <dd>

Указывает имя или адрес в Интернете для сервера или узла, компьютер. Имя является символьной строкой.

</dd> <dt>

*имя порта* 
</dt> <dd>

Указывает имя объекта или номер объекта DECnet. Имя объекта может содержать до 16 символов. Номера объектов могут начинаться с символа решетки ( \# ).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Синтаксис строки транспортного порта DECnet, как и все строки портов, определяется независимо от спецификации IDL. Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.

> [!Note]  
> Это семейство протоколов не поддерживается в Windows XP.

 

## <a name="examples"></a>Примеры

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[**Строковая привязка**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 