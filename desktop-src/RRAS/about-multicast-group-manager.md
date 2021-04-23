---
title: Сведения о диспетчере групп многоадресной рассылки
description: В этой документации описывается технология диспетчера групп многоадресной рассылки (МГМ).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS многоадресной рассылки диспетчера групп
- Диспетчер групп многоадресной рассылки — RRAS, описание
- RRAS службы маршрутизации и удаленного доступа, Диспетчер групп многоадресной рассылки
- Служба маршрутизации и удаленного доступа RRAS, Диспетчер групп многоадресной рассылки, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672078"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="e53ae-107">Сведения о диспетчере групп многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="e53ae-107">About Multicast Group Manager</span></span>

<span data-ttu-id="e53ae-108">В этой документации описывается технология диспетчера групп многоадресной рассылки (МГМ).</span><span class="sxs-lookup"><span data-stu-id="e53ae-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="e53ae-109">Многоадресная рассылка позволяет узлу отправлять данные только тем получателям, которые специально запрашивают получение данных.</span><span class="sxs-lookup"><span data-stu-id="e53ae-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="e53ae-110">Таким образом, многоадресная рассылка отличается от отправки широковещательных данных, так как данные вещания отправляются на все узлы.</span><span class="sxs-lookup"><span data-stu-id="e53ae-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="e53ae-111">Многоадресная рассылка экономит пропускную способность сети, так как они получают данные только теми узлами, которые запрашивают данные, а данные передаются по любой ссылке только один раз.</span><span class="sxs-lookup"><span data-stu-id="e53ae-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="e53ae-112">Многоадресная рассылка экономит пропускную способность сервера, так как сервер должен отправить только одно многоадресное сообщение на одну сеть, а не одно одностраничное сообщение на каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="e53ae-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="e53ae-113">Примерами популярных многоадресных приложений являются сетевые собрания и Интернет-радио.</span><span class="sxs-lookup"><span data-stu-id="e53ae-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="e53ae-114">API МГМ позволяет разработчикам создавать протоколы многоадресной маршрутизации, взаимодействующие с маршрутизаторами, на которых работает диспетчер групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="e53ae-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="e53ae-115">Если на маршрутизаторе включено более одного протокола многоадресной маршрутизации, Диспетчер групп многоадресной рассылки координирует операции между всеми протоколами маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e53ae-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="e53ae-116">Диспетчер групп многоадресной рассылки уведомляет каждый протокол маршрутизации при изменении членства в группе и получении данных многоадресной рассылки из нового источника или в новую группу.</span><span class="sxs-lookup"><span data-stu-id="e53ae-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="e53ae-117">API МГМ предоставляет следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="e53ae-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="e53ae-118">Регистрация протокола</span><span class="sxs-lookup"><span data-stu-id="e53ae-118">Protocol registration</span></span>
-   <span data-ttu-id="e53ae-119">Управление группами</span><span class="sxs-lookup"><span data-stu-id="e53ae-119">Group management</span></span>
-   <span data-ttu-id="e53ae-120">Перечисление записей многоадресной пересылки (МФЕ)</span><span class="sxs-lookup"><span data-stu-id="e53ae-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="e53ae-121">Определения обратного вызова для протоколов многоадресной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="e53ae-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="e53ae-122">В этом обзоре описываются компоненты архитектуры многоадресной рассылки, клиентские сценарии, используемые для взаимодействия с диспетчером групп многоадресной рассылки, и рекомендации по программированию для использования API МГМ.</span><span class="sxs-lookup"><span data-stu-id="e53ae-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




