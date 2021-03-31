---
title: атрибут ncacn_nb_tcp
description: '\_ \_ Ключевое слово TCP нкакн NetBIOS используется для обнаружения TCP через NetBIOS в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337292"
---
# <a name="ncacn_nb_tcp-attribute"></a>\_ \_ атрибут TCP нкакн NetBIOS

Ключевое слово **\_ \_ TCP нкакн NetBIOS** используется для обнаружения TCP через NetBIOS в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя порта* 
</dt> <dd>

Задает необязательное 8-разрядное значение в диапазоне от 1 до 254. Значения меньше 0x20 зарезервированы. Если значение *имени порта* не указано, служба сопоставления конечных точек выбирает значение порта.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Синтаксис строки порта NetBIOS, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL. Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.

> [!Note]  
> Это семейство протоколов не поддерживается в Windows XP.

 

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
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

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**нкакн \_ IP \_ TCP**](ncacn-ip-tcp.md)
</dt> <dt>

[**нкакн \_ имена \_ NetBIOS**](ncacn-nb-nb.md)
</dt> <dt>

[**нкакн \_ NP**](ncacn-np.md)
</dt> <dt>

[**нкакн \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**нкалрпк**](ncalrpc.md)
</dt> <dt>

[**Строковая привязка**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 