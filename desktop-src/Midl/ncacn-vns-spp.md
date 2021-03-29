---
title: атрибут ncacn_vns_spp
description: '\_ \_ Ключевое слово нкакн ВНС SPP идентифицирует Banyan VINEs SPP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790710"
---
# <a name="ncacn_vns_spp-attribute"></a>\_атрибут нкакн ВНС \_ SPP

Ключевое слово **нкакн \_ ВНС \_ SPP** ИДЕНТИФИЦИРУЕТ Banyan Vines SPP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя сервера* 
</dt> <dd>

Указывает Стритталк имя сервера. Имя имеет вид item@group @organization . Элемент может иметь длину до 31 символа, а группа и организация могут содержать до 15 символов.

</dd> <dt>

*имя порта* 
</dt> <dd>

Указывает порт Banyan Vines SPP. Допустимый диапазон для статических конечных точек — 250 – 511.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы использовать транспортный протокол **нкакн \_ ВНС \_ SPP** в распределенных приложениях под управлением Windows 2000, необходимо установить соответствующее клиентское программное обеспечение Banyan Enterprise. После установки откройте **Панель управления**, выберите **Конфигурация и добавить**, а затем выберите **Service \| Banyan \| RPC Services for Banyan**. Для поддержки 16-разрядных клиентов требуется соответствующее программное обеспечение Vines. Дополнительные сведения о корпоративном клиенте Banyan и 16-разрядном программном обеспечении vines см. по адресу Banyan.

Синтаксис строки транспортного порта Banyan Vines SPP, как и все строки портов, определяется независимо от спецификации IDL. Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.

> [!Note]  
> Это семейство протоколов не поддерживается в Windows XP.

 

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
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

[**нкалрпк**](ncalrpc.md)
</dt> <dt>

[**нкадг \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**нкадг \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[Строковая привязка](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 