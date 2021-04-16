---
title: атрибут ncacn_ip_tcp
description: '\_ \_ Ключевое слово нкакн IP TCP определяет TCP/IP как семейство протоколов для конечной точки.'
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650349"
---
# <a name="ncacn_ip_tcp-attribute"></a>нкакн \_ IP- \_ атрибут TCP

Ключевое слово **нкакн \_ IP \_ TCP** определяет TCP/IP как семейство протоколов для конечной точки.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя сервера* 
</dt> <dd>

Указывает имя или адрес в Интернете для сервера или узла, компьютер. Имя является символьной строкой. Интернет-адрес представляет собой стандартную нотацию Интернета.

</dd> <dt>

*имя порта* 
</dt> <dd>

Указывает необязательное 16-разрядное число. Значения менее 1024 обычно зарезервированы. Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Синтаксис строки порта транспорта TCP/IP, как и все строки портов, определяется независимо от спецификации IDL. Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.

## <a name="examples"></a>Примеры

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**нкакн \_ NetBIOS, \_ протокол TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**нкакн \_ NP**](ncacn-np.md)
</dt> <dt>

[**нкакн \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**нкалрпк**](ncalrpc.md)
</dt> <dt>

[**Строковая привязка**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 