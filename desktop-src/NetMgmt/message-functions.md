---
title: Функции сообщений (Управление сетью)
description: Функция сообщений управления сетью отправляет сообщения и поддерживает псевдонимы сообщений. Ниже перечислены функции сообщений.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414581"
---
# <a name="message-functions-network-management"></a><span data-ttu-id="3e0b3-104">Функции сообщений (Управление сетью)</span><span class="sxs-lookup"><span data-stu-id="3e0b3-104">Message Functions (Network Management)</span></span>

<span data-ttu-id="3e0b3-105">\[Функции сообщений не поддерживаются в Windows Vista, так как службы оповещений и сообщений не поддерживаются.\]</span><span class="sxs-lookup"><span data-stu-id="3e0b3-105">\[The message functions are not supported as of Windows Vista because the alerter and messenger services are not supported.\]</span></span>

<span data-ttu-id="3e0b3-106">Функция сообщений управления сетью отправляет сообщения и поддерживает псевдонимы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-106">The network management message functions send messages and maintain message aliases.</span></span> <span data-ttu-id="3e0b3-107">Ниже перечислены функции сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-107">The message functions are listed following.</span></span>

<span data-ttu-id="3e0b3-108">**Windows Server 2003:** Службы оповещений и сообщений по умолчанию отключены.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-108">**Windows Server 2003:** The alerter and messenger services are disabled by default.</span></span> <span data-ttu-id="3e0b3-109">Необходимо повторно включить службы перед вызовом [функций предупреждений](alert-functions.md) управления сетью или функций сообщений управления сетью.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-109">You must re-enable the services before calling the network management [Alert functions](alert-functions.md) or the network management Message functions.</span></span>



| <span data-ttu-id="3e0b3-110">Функция</span><span class="sxs-lookup"><span data-stu-id="3e0b3-110">Function</span></span>                                               | <span data-ttu-id="3e0b3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3e0b3-111">Description</span></span>                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="3e0b3-112">**нетмессажебуфферсенд**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-112">**NetMessageBufferSend**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | <span data-ttu-id="3e0b3-113">Отправляет сообщение в псевдоним зарегистрированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-113">Sends a message to a registered message alias.</span></span>                                  |
| [<span data-ttu-id="3e0b3-114">**нетмессаженамеадд**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-114">**NetMessageNameAdd**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | <span data-ttu-id="3e0b3-115">Регистрирует псевдоним сообщения в таблице имен сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-115">Registers a message alias in the message name table.</span></span>                            |
| [<span data-ttu-id="3e0b3-116">**нетмессаженамедел**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-116">**NetMessageNameDel**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | <span data-ttu-id="3e0b3-117">Удаляет псевдоним сообщения из таблицы имен сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-117">Deletes a message alias from the message name table.</span></span>                            |
| [<span data-ttu-id="3e0b3-118">**нетмессаженаминум**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-118">**NetMessageNameEnum**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | <span data-ttu-id="3e0b3-119">Список всех псевдонимов сообщений, хранящихся в таблице имен сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-119">Lists all the message aliases stored in the message name table.</span></span>                 |
| [<span data-ttu-id="3e0b3-120">**нетмессаженамежетинфо**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-120">**NetMessageNameGetInfo**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | <span data-ttu-id="3e0b3-121">Возвращает сведения о конкретном псевдониме сообщения в таблице имен сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-121">Returns information about a particular message alias in the message name table.</span></span> |



 

<span data-ttu-id="3e0b3-122">*Сообщение* — это буфер текстовых данных, отправляемых пользователю или приложению в сети.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-122">A *message* is a buffer of text data sent to a user or application on the network.</span></span> <span data-ttu-id="3e0b3-123">Чтобы получить сообщение, пользователь или приложение должны зарегистрировать псевдоним сообщения в таблице компьютеров с именами сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-123">To receive a message, a user or application must register a message alias in a computer's table of message names.</span></span> <span data-ttu-id="3e0b3-124">По умолчанию регистрируются следующие псевдонимы: "пользователь", "компьютер", "домен" или " \* " (текущий домен компьютера).</span><span class="sxs-lookup"><span data-stu-id="3e0b3-124">The following aliases are registered by default: "user", "machine", "domain", or "\*" (the current domain of the computer).</span></span> <span data-ttu-id="3e0b3-125">Псевдоним "домен" определяет набор компьютеров, имеющих одно и то же доменное имя, определенное в качестве домена или в качестве рабочей группы, и прослушивать широковещательные передачи в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-125">The "domain" alias specifies the set of computers that have the same domain name defined as their domain or as their workgroup and listen to broadcasts on the same subnet.</span></span> <span data-ttu-id="3e0b3-126">Для NetBIOS через TCP/IP указание псевдонима домена также может быть выполнено в подсетях, если доменное имя разрешается сервером имен или если широковещательные рассылки датаграмм NetBIOS пересылаются между маршрутизаторами.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-126">For NetBIOS over TCP/IP, specifying the "domain" alias can also succeed across subnets if the domain name is resolved by a name server, or if NetBIOS datagram broadcasts are forwarded across routers.</span></span> <span data-ttu-id="3e0b3-127">Таким образом, сообщения, отправляемые в домен, не гарантированно доставляться всем членам домена.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-127">Therefore, messages sent to a domain do not have guaranteed delivery to all members of the domain.</span></span> <span data-ttu-id="3e0b3-128">Некоторые члены домена также могут получить сообщение несколько раз, если на них установлен несколько транспортов, поддерживающих протокол NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-128">It is also possible for some domain members to receive the message multiple times if they have multiple transports installed that support NetBIOS.</span></span>

<span data-ttu-id="3e0b3-129">Можно также зарегистрировать псевдоним сообщения, вызвав функцию [**нетмессаженамеадд**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) .</span><span class="sxs-lookup"><span data-stu-id="3e0b3-129">You can also register a message alias by calling the [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) function.</span></span> <span data-ttu-id="3e0b3-130">*Таблица имен сообщений* содержит список зарегистрированных псевдонимов сообщений (пользователей и приложений), которым разрешено принимать сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-130">A *message name table* contains a list of registered message aliases (users and applications) permitted to receive messages.</span></span> <span data-ttu-id="3e0b3-131">Псевдонимы, зарегистрированные в таблице имен сообщений, не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-131">The aliases registered in the message name table are case insensitive.</span></span>

<span data-ttu-id="3e0b3-132">Служба сообщений должна быть запущена на принимающем компьютере для отображения всплывающего сообщения при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-132">The messenger service must be running on the receiving computer to display a pop-up message when the message is received.</span></span> <span data-ttu-id="3e0b3-133">Кроме того, на локальном компьютере должна быть запущена служба рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-133">In addition, the Workstation service must be running on the local computer.</span></span> <span data-ttu-id="3e0b3-134">NetBIOS — это транспортный механизм, используемый между отправителем и получателем.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-134">NetBIOS is the transport mechanism used between the sender and receiver.</span></span>

<span data-ttu-id="3e0b3-135">Функции сообщений доступны на двух уровнях информации:</span><span class="sxs-lookup"><span data-stu-id="3e0b3-135">Message functions are available at two information levels:</span></span>

-   [<span data-ttu-id="3e0b3-136">**\_Сведения о сообщениях \_ 0**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-136">**MSG\_INFO\_0**</span></span>](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [<span data-ttu-id="3e0b3-137">**\_Сведения о сообщениях \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3e0b3-137">**MSG\_INFO\_1**</span></span>](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

<span data-ttu-id="3e0b3-138">Информационный **уровень \_ сообщения \_ 1** существует только для обеспечения совместимости.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-138">The **MSG\_INFO\_1** information level exists only for compatibility.</span></span> <span data-ttu-id="3e0b3-139">Служба сообщений не пересылает имена или не разрешает пересылать имена.</span><span class="sxs-lookup"><span data-stu-id="3e0b3-139">The messenger service does not forward names or allow names to be forwarded to it.</span></span>

 

 




