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
# <a name="ncacn_http-attribute"></a><span data-ttu-id="c7bf7-104">нкакн \_ -атрибут HTTP</span><span class="sxs-lookup"><span data-stu-id="c7bf7-104">ncacn\_http attribute</span></span>

<span data-ttu-id="c7bf7-105">Ключевое слово **нкакн \_ http** определяет сервер Microsoft Internet Information Server (IIS) в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="c7bf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7bf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7bf7-107">*\_сервер RPC*</span><span class="sxs-lookup"><span data-stu-id="c7bf7-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="c7bf7-108">Интернет-адрес или имя компьютера, на котором выполняется процесс сервера RPC.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="c7bf7-109">*endpoint*</span><span class="sxs-lookup"><span data-stu-id="c7bf7-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="c7bf7-110">Известный (статический) порт TCP/IP, прослушиваемый процессом RPC-сервера.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7bf7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7bf7-111">Remarks</span></span>

<span data-ttu-id="c7bf7-112">Определение Microsoft Internet Information Server (IIS) в качестве семейства протоколов позволяет клиентским и серверным приложениям обмениваться данными через Интернет, используя Microsoft Internet Information Server (IIS) в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="c7bf7-113">Так как вызовы проходят через установленный HTTP-порт, они могут пересекать брандмауэры.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="c7bf7-114">Все клиентские и серверные приложения RPC могут поддерживать протокол **\_ http нкакн** , если они подключены к серверу IIS.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="c7bf7-115">Службы IIS обращаются к серверу RPC и устанавливают сокеты TCP/IP, которые обслуживаются для клиента.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="c7bf7-116">Службы IIS согласовывают подключение TCP/IP с сервером RPC, и после завершения согласования действует как прокси RPC, пересылает данные между сокетом TCP/IP на стороне клиента и сокетом TCP/IP на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="c7bf7-117">Когда прокси-сервер RPC IIS обнаруживает закрытие сеанса на клиенте или на стороне сервера, он закрывает оставшийся сокет.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="c7bf7-118">Клиентское приложение неявно использует статическую привязку к службам IIS, но сервер может использовать динамические конечные точки с RPC сервера (сопоставитель конечных точек), разрешающим порт сервера RPC.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="c7bf7-119">Если службы IIS находятся на разных компьютерах, чем на сервере RPC, то службы IIS получают удаленный вызов, обращаются к RPC на компьютере RPC-сервера для получения конечной точки серверного процесса, а затем перенаправляют вызов соответствующему серверу RPC.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="c7bf7-120">Если Internet Explorer установлен, транспорт проверит реестр на наличие конфигурации для HTTP-прокси.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="c7bf7-121">Если прокси-сервер существует, он будет использоваться транспортом.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="c7bf7-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="c7bf7-122">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c7bf7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7bf7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7bf7-124">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c7bf7-125">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="c7bf7-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c7bf7-126">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 