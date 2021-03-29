---
title: атрибут ncacn_http
description: '\_Ключевое слово нкакн HTTP определяет сервер Microsoft Internet Information Server (IIS) в качестве семейства протоколов для конечной точки.'
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790903"
---
# <a name="ncacn_http-attribute"></a>нкакн \_ -атрибут HTTP

Ключевое слово **нкакн \_ http** определяет сервер Microsoft Internet Information Server (IIS) в качестве семейства протоколов для конечной точки.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*\_сервер RPC* 
</dt> <dd>

Интернет-адрес или имя компьютера, на котором выполняется процесс сервера RPC.

</dd> <dt>

*endpoint* 
</dt> <dd>

Известный (статический) порт TCP/IP, прослушиваемый процессом RPC-сервера.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Определение Microsoft Internet Information Server (IIS) в качестве семейства протоколов позволяет клиентским и серверным приложениям обмениваться данными через Интернет, используя Microsoft Internet Information Server (IIS) в качестве прокси-сервера. Так как вызовы проходят через установленный HTTP-порт, они могут пересекать брандмауэры.

Все клиентские и серверные приложения RPC могут поддерживать протокол **\_ http нкакн** , если они подключены к серверу IIS. Службы IIS обращаются к серверу RPC и устанавливают сокеты TCP/IP, которые обслуживаются для клиента. Службы IIS согласовывают подключение TCP/IP с сервером RPC, и после завершения согласования действует как прокси RPC, пересылает данные между сокетом TCP/IP на стороне клиента и сокетом TCP/IP на стороне сервера. Когда прокси-сервер RPC IIS обнаруживает закрытие сеанса на клиенте или на стороне сервера, он закрывает оставшийся сокет.

Клиентское приложение неявно использует статическую привязку к службам IIS, но сервер может использовать динамические конечные точки с RPC сервера (сопоставитель конечных точек), разрешающим порт сервера RPC. Если службы IIS находятся на разных компьютерах, чем на сервере RPC, то службы IIS получают удаленный вызов, обращаются к RPC на компьютере RPC-сервера для получения конечной точки серверного процесса, а затем перенаправляют вызов соответствующему серверу RPC.

Если Internet Explorer установлен, транспорт проверит реестр на наличие конфигурации для HTTP-прокси. Если прокси-сервер существует, он будет использоваться транспортом.

## <a name="examples"></a>Примеры

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Строковая привязка**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 