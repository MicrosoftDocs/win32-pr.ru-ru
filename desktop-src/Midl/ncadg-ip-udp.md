---
title: атрибут ncadg_ip_udp
description: '\_ \_ Ключевое слово нкадг IP UDP определяет версию датаграммы TCP/IP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp атрибута MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91db32fd7636f956e64dafc0db15efb520e643b435995dd977db7a631a20c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067064"
---
# <a name="ncadg_ip_udp-attribute"></a>\_атрибут IP \_ UDP нкадг

Ключевое слово **нкадг \_ IP \_ UDP** определяет версию ДАТАГРАММы TCP/IP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя сервера* 
</dt> <dd>

Указывает имя или адрес в Интернете для сервера или узла, компьютер. Имя является символьной строкой и может быть полным доменным именем. Интернет-адрес представляет собой стандартную нотацию Интернета.

</dd> <dt>

*имя порта* 
</dt> <dd>

Указывает необязательное 16-разрядное число. Значения менее 1024 обычно зарезервированы. Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .

</dd> </dl>

## <a name="remarks"></a>Remarks

К протоколам датаграмм, [**нкадг \_ IPX**](ncadg-ipx.md) и **нкадг \_ IP \_ UDP** применяются следующие ограничения.

-   Они не поддерживают обратные вызовы. Все функции, использующие **\[** атрибут [**обратного вызова**](callback.md) , завершатся **\]** ошибкой.
-   Они не поддерживают использование конструктора типа [**канала**](pipe.md) .

Синтаксис строки порта транспорта TCP/IP, как и все строки портов, определяется независимо от спецификации IDL. Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**конечной**](endpoint.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**нкакн \_ в \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**нкакн \_ днет \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**нкакн \_ IP \_ TCP**](ncacn-ip-tcp.md)
</dt> <dt>

[**нкакн \_ NetBIOS- \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**нкакн \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**нкакн \_ имена \_ NetBIOS**](ncacn-nb-nb.md)
</dt> <dt>

[**нкакн \_ NetBIOS, \_ протокол TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**нкакн \_ NP**](ncacn-np.md)
</dt> <dt>

[**нкакн \_ ВНС \_ SPP**](ncacn-vns-spp.md)
</dt> <dt>

[**нкалрпк**](ncalrpc.md)
</dt> <dt>

[**нкадг \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Строковая привязка](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 