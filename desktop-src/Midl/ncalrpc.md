---
title: атрибут нкалрпк
description: Ключевое слово нкалрпк определяет локальное межпроцессное взаимодействие как семейство протоколов для конечной точки. Это ключевое слово является одним из допустимых имен семейств протоколов, которые должны использоваться с атрибутом \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- атрибут нкалрпк MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481f005a741c6a815572f5861755f52d5921bae89e8bb2d8a3ef757a0fc42d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067004"
---
# <a name="ncalrpc-attribute"></a>атрибут нкалрпк

Ключевое слово **нкалрпк** определяет локальное межпроцессное взаимодействие как семейство протоколов для конечной точки. Это ключевое слово является одним из допустимых имен семейств протоколов, которые должны использоваться с **\[** [](endpoint.md) **\]** атрибутом Endpoint.

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя порта* 
</dt> <dd>

Строка символов, указывающая коммуникационный порт (приложение, служба или экземпляр службы), который клиент использует для выполнения межпроцессных вызовов к серверу. Строка может содержать до 53 символов и не должна содержать символы обратной косой черты ( \\ ). Имя компьютера не должно использоваться с ключевым словом **нкалрпк** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Синтаксис локальной строки порта межпроцессного взаимодействия, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL. Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки. Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
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

[**нкадг \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**нкадг \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Строковая привязка](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 