---
title: Использование RPC с прокси-сервером Winsock
description: Использование RPC с прокси-сервером Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070577"
---
# <a name="using-rpc-with-winsock-proxy"></a><span data-ttu-id="934b4-103">Использование RPC с прокси-сервером Winsock</span><span class="sxs-lookup"><span data-stu-id="934b4-103">Using RPC with Winsock Proxy</span></span>

<span data-ttu-id="934b4-104">В выпуске сервера Microsoft Internet Access Server входит Winsock Proxy, улучшенная версия API Windows Sockets версии 1,1.</span><span class="sxs-lookup"><span data-stu-id="934b4-104">The release of Microsoft Internet Access Server included Winsock Proxy, an enhanced version of Windows Sockets API version 1.1.</span></span> <span data-ttu-id="934b4-105">Прокси-сервер Winsock позволяет приложению Windows Sockets, работающему на клиенте частной сети, работать так же, как если бы оно было напрямую подключено к удаленному Интернет-серверу.</span><span class="sxs-lookup"><span data-stu-id="934b4-105">Winsock Proxy lets a Windows Sockets application, running on a private network client, behave as if it were directly connected to a remote Internet server application.</span></span> <span data-ttu-id="934b4-106">Прокси-сервер Microsoft выступает в качестве узла для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="934b4-106">The Microsoft Proxy Server acts as the host for this connection.</span></span> <span data-ttu-id="934b4-107">Это означает, что все подключения на уровне приложения проходят через один защищенный компьютер — компьютер шлюза, на котором работает прокси-сервер Microsoft.</span><span class="sxs-lookup"><span data-stu-id="934b4-107">This means that all application-level communications are channeled through a single secured computer—the gateway computer running Microsoft Proxy Server.</span></span>

<span data-ttu-id="934b4-108">Обычно для передачи датаграмм-пакетов библиотека DLL транспорта RPC обходит функции [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) и [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) , предоставленные в Wsock32.dll, и напрямую взаимодействует с драйвером соответствующего устройства.</span><span class="sxs-lookup"><span data-stu-id="934b4-108">Ordinarily, for datagram-packet transfers, the RPC transport DLL bypasses the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) functions provided in Wsock32.dll, and communicates directly with the underlying device driver.</span></span> <span data-ttu-id="934b4-109">Это повышает скорость передачи пакетов, но делает функции прокси-сервера Winsock недоступными для приложения.</span><span class="sxs-lookup"><span data-stu-id="934b4-109">This improves the speed of packet transfers but makes Winsock Proxy features unavailable to the application.</span></span>

<span data-ttu-id="934b4-110">Каждый поставщик сетевых протоколов имеет связанный GUID.</span><span class="sxs-lookup"><span data-stu-id="934b4-110">Each network protocol provider to have an associated GUID.</span></span> <span data-ttu-id="934b4-111">Библиотека времени выполнения RPC сравнивает идентификаторы GUID и IPX с известными идентификаторами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="934b4-111">The RPC run-time library compares the UDP and IPX GUIDs to the well known Microsoft identifiers.</span></span> <span data-ttu-id="934b4-112">Если они не совпадают, RPC автоматически использует Winsock.</span><span class="sxs-lookup"><span data-stu-id="934b4-112">If they don't match, RPC automatically uses Winsock.</span></span>

<span data-ttu-id="934b4-113">Другой возможностью прокси-сервера Winsock является возможность имитировать транспортный протокол TCP через транспорт Novell SPX, если на клиентском компьютере SPX не установлен протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="934b4-113">Another feature of Winsock Proxy is its ability to emulate the TCP transport protocol over the Novell SPX transport when the SPX client computer does not have TCP installed.</span></span> <span data-ttu-id="934b4-114">Чтобы использовать эту функцию с приложениями RPC, измените системный реестр на каждом клиентском компьютере, чтобы добавить эту запись:</span><span class="sxs-lookup"><span data-stu-id="934b4-114">To use this feature with RPC applications, edit the system registry on each client computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="934b4-115">Измените реестр на каждом сервере, чтобы добавить эту запись:</span><span class="sxs-lookup"><span data-stu-id="934b4-115">Edit the registry on each server computer to add this entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

<span data-ttu-id="934b4-116">Дополнительные сведения о протоколах транспорта RPC см. в разделе [Указание последовательностей протоколов](specifying-protocol-sequences.md).</span><span class="sxs-lookup"><span data-stu-id="934b4-116">For more information about RPC transport protocols see [Specifying Protocol Sequences](specifying-protocol-sequences.md).</span></span> <span data-ttu-id="934b4-117">Дополнительные сведения о прокси-сервере Winsock см. в документации по продукту для сервера Microsoft Internet Access Server.</span><span class="sxs-lookup"><span data-stu-id="934b4-117">For more information about Winsock Proxy, see the product documentation for Microsoft Internet Access Server.</span></span>

<span data-ttu-id="934b4-118">В Windows 2000 не реализованы записи реестра **ClientProtocols** и **серверпротоколс** .</span><span class="sxs-lookup"><span data-stu-id="934b4-118">Windows 2000 does not implement the **ClientProtocols** and **ServerProtocols** registry entries.</span></span> <span data-ttu-id="934b4-119">Корпорация Майкрософт предоставляет все хорошо известные транспорты в составе библиотеки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="934b4-119">Microsoft provides all well known transports as part of the run-time library.</span></span> <span data-ttu-id="934b4-120">Поэтому эти записи не требуются.</span><span class="sxs-lookup"><span data-stu-id="934b4-120">Therefore, these entries are not necessary.</span></span>

 

 