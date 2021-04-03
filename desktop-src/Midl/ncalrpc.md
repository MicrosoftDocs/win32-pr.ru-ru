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
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987476"
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

Строка символов, указывающая коммуникационный порт (приложение, служба или экземпляр службы), который клиент использует для выполнения межпроцессных вызовов к серверу. Строка может содержать до 53 символов и не должна содержать обратную косую черту ( \) символы). Имя компьютера не должно использоваться с ключевым словом **нкалрпк** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

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

[**нкакн \_ ВНС \_ SPP**](ncacn-vns-spp.md)
</dt> <dt>

[**нкадг \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**нкадг \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Строковая привязка](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 