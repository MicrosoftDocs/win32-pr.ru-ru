---
description: Одной из важнейших задач поставщика услуг транспорта данных является то, что предоставляет указание клиенту при возникновении определенных сетевых событий.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Уведомление о событиях сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897317"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="597ad-103">Уведомление о событиях сети</span><span class="sxs-lookup"><span data-stu-id="597ad-103">Notification of Network Events</span></span>

<span data-ttu-id="597ad-104">Одной из важнейших задач поставщика услуг транспорта данных является то, что предоставляет указание клиенту при возникновении определенных сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="597ad-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="597ad-105">Список определенных сетевых событий состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="597ad-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="597ad-106">Процесс **демона \_ CONNECT**— подключение к удаленному узлу или сеансу многоадресной рассылки завершено.</span><span class="sxs-lookup"><span data-stu-id="597ad-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="597ad-107">Процесс **демона \_ ACCEPT**— удаленный узел делает запрос на подключение.</span><span class="sxs-lookup"><span data-stu-id="597ad-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="597ad-108">Процесс **демона \_ READ**— данные сети уже получены, доступные для чтения.</span><span class="sxs-lookup"><span data-stu-id="597ad-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="597ad-109">Процесс **демона \_ WRITE**— место в буферах поставщика услуг становится доступным, поэтому теперь можно отправлять дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="597ad-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="597ad-110">Процесс **демона \_ OOB**— данные по внешнему каналу доступны для чтения.</span><span class="sxs-lookup"><span data-stu-id="597ad-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="597ad-111">Процесс **демона \_ ЗАКРЫТЬ**— удаленный узел закрыл подключение.</span><span class="sxs-lookup"><span data-stu-id="597ad-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="597ad-112">Процесс **демона \_ QOS**— изменение было выполнено на согласованных уровнях качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="597ad-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="597ad-113">Процесс **демона \_ \_QoS группы**— зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="597ad-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="597ad-114">Процесс **демона \_ \_ \_ Изменение интерфейса маршрутизации**— локальный интерфейс, который должен использоваться для достижения назначения, указанного в **\_ \_ интерфейсе маршрутизации SIO \_ изменение ioctl** .</span><span class="sxs-lookup"><span data-stu-id="597ad-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="597ad-115">Процесс **демона \_ \_ \_ Изменение списка адресов**— список локальных адресов, к которым может быть привязано приложение.</span><span class="sxs-lookup"><span data-stu-id="597ad-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="597ad-116">Набор сетевых событий, перечисленных выше, иногда называют событиями **демо-фильтра \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="597ad-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="597ad-117">Указание на вхождение одного или нескольких таких сетевых событий может быть предоставлено несколькими способами в зависимости от того, как клиент запрашивает уведомления.</span><span class="sxs-lookup"><span data-stu-id="597ad-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



