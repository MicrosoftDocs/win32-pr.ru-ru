---
title: Настройка RPC для SPX/IPX
description: При использовании \_ транспортов нкакн SPX и нкадг \_ IPX имя сервера точно совпадает с именем сервера в Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486916"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="6b394-103">Настройка RPC для SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="6b394-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="6b394-104">При использовании транспортов **нкакн \_ SPX** и **нкадг \_ IPX** имя сервера точно совпадает с именем сервера в Windows.</span><span class="sxs-lookup"><span data-stu-id="6b394-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="6b394-105">Однако поскольку имена распределяются по протоколам Novell, они должны соответствовать соглашениям об именовании Novell.</span><span class="sxs-lookup"><span data-stu-id="6b394-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="6b394-106">Если имя сервера не является допустимым именем Novell, серверы не смогут создавать конечные точки с помощью транспортов **\_ IPX** **нкакн \_ SPX** или нкадг.</span><span class="sxs-lookup"><span data-stu-id="6b394-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="6b394-107">Допустимое имя сервера Novell содержит только символы между 0x20 и 0x7F.</span><span class="sxs-lookup"><span data-stu-id="6b394-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="6b394-108">Символы нижнего регистра заменяются на прописные.</span><span class="sxs-lookup"><span data-stu-id="6b394-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="6b394-109">Нельзя использовать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="6b394-109">The following characters cannot be used:</span></span>

<span data-ttu-id="6b394-110">" \* ,./:; <=>?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="6b394-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="6b394-111">Чтобы обеспечить совместимость с первой версией Windows NT, **нкакн \_ SPX** и **нкадг \_ IPX** также позволяют использовать специальный формат имени сервера, известного как имя тильды.</span><span class="sxs-lookup"><span data-stu-id="6b394-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="6b394-112">Имя тильды состоит из символа тильды (~), за которым следует номер сети из восьми цифр, а затем за ним следует 12-значный адрес Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6b394-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="6b394-113">Тильды имеют преимущество в том, что они не нуждаются в возможностях службы имен.</span><span class="sxs-lookup"><span data-stu-id="6b394-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="6b394-114">Поэтому при подключении к серверу имя тильды будет работать.</span><span class="sxs-lookup"><span data-stu-id="6b394-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="6b394-115">В следующих таблицах содержатся два образца конфигураций, иллюстрирующих описанные выше точки.</span><span class="sxs-lookup"><span data-stu-id="6b394-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="6b394-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="6b394-116">Component</span></span>                            | <span data-ttu-id="6b394-117">Настроено как</span><span class="sxs-lookup"><span data-stu-id="6b394-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="6b394-118">Windows Server</span><span class="sxs-lookup"><span data-stu-id="6b394-118">Windows server</span></span>                       | <span data-ttu-id="6b394-119">нвкс</span><span class="sxs-lookup"><span data-stu-id="6b394-119">NWCS</span></span>               |
| <span data-ttu-id="6b394-120">Клиент Windows</span><span class="sxs-lookup"><span data-stu-id="6b394-120">Windows client</span></span>                       | <span data-ttu-id="6b394-121">нвкс</span><span class="sxs-lookup"><span data-stu-id="6b394-121">NWCS</span></span>               |
| <span data-ttu-id="6b394-122">16-разрядный клиент Windows, клиент MS-DOS</span><span class="sxs-lookup"><span data-stu-id="6b394-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="6b394-123">Перенаправитель NetWare</span><span class="sxs-lookup"><span data-stu-id="6b394-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="6b394-124">Конфигурация в предыдущей таблице требует наличия файловых серверов NetWare или маршрутизаторов в сети.</span><span class="sxs-lookup"><span data-stu-id="6b394-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="6b394-125">Это обеспечит лучшую производительность, поскольку имена серверов хранятся в привязке NetWare.</span><span class="sxs-lookup"><span data-stu-id="6b394-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="6b394-126">Компонент</span><span class="sxs-lookup"><span data-stu-id="6b394-126">Component</span></span>                            | <span data-ttu-id="6b394-127">Настроено как</span><span class="sxs-lookup"><span data-stu-id="6b394-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="6b394-128">Windows Server</span><span class="sxs-lookup"><span data-stu-id="6b394-128">Windows server</span></span>                       | <span data-ttu-id="6b394-129">Агент SAP</span><span class="sxs-lookup"><span data-stu-id="6b394-129">SAP Agent</span></span>     |
| <span data-ttu-id="6b394-130">Клиент Windows</span><span class="sxs-lookup"><span data-stu-id="6b394-130">Windows client</span></span>                       | <span data-ttu-id="6b394-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="6b394-131">IPX/SPX</span></span>       |
| <span data-ttu-id="6b394-132">16-разрядный клиент Windows, клиент MS-DOS</span><span class="sxs-lookup"><span data-stu-id="6b394-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="6b394-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="6b394-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="6b394-134">Вторая конфигурация работает в среде, которая не содержит файловые серверы NetWare или маршрутизаторы (например, сеть из двух компьютеров: Windows Server и клиент MS-DOS).</span><span class="sxs-lookup"><span data-stu-id="6b394-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="6b394-135">Разрешение имен, которое выполняется во время первого вызова через маркер привязки, будет немного медленнее, чем в первой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6b394-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="6b394-136">Кроме того, Вторая конфигурация приводит к большему объему трафика, создаваемого по сети.</span><span class="sxs-lookup"><span data-stu-id="6b394-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="6b394-137">Чтобы реализовать разрешение имен, когда RPC-сервер использует конечную точку SPX или IPX, имя сервера и конечная точка регистрируются как сервер SAP типа 640 (шестнадцатеричный).</span><span class="sxs-lookup"><span data-stu-id="6b394-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="6b394-138">Чтобы разрешить имя сервера, клиент RPC отправляет запрос SAP для всех служб того же типа, а затем проверяет список ответов на имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6b394-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="6b394-139">Этот процесс происходит во время первого вызова RPC для каждого маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="6b394-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="6b394-140">Дополнительные сведения о протоколе SAP для Novell см. в документации по NetWare.</span><span class="sxs-lookup"><span data-stu-id="6b394-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="6b394-141">В 16-разрядных клиентских приложениях Windows, использующих транспорты **нкакн \_ SPX** или **нкадг \_ IPX** , требуется, чтобы файл Nwipxspx.dll был установлен для запуска в подсистеме WOW.</span><span class="sxs-lookup"><span data-stu-id="6b394-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="6b394-142">Чтобы получить этот файл, обратитесь в Novell.</span><span class="sxs-lookup"><span data-stu-id="6b394-142">Contact Novell to obtain this file.</span></span>

 

 

 




