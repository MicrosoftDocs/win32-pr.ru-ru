---
description: В этом разделе описываются функции протокола управления передачей/протокола Интернета (TCP/IP), структуры данных и элементы управления.
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Приложение Winsock TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263464"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="d51c2-103">Приложение Winsock TCP/IP</span><span class="sxs-lookup"><span data-stu-id="d51c2-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="d51c2-104">В этом разделе описываются функции протокола управления передачей/протокола Интернета (TCP/IP), структуры данных и элементы управления.</span><span class="sxs-lookup"><span data-stu-id="d51c2-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="d51c2-105">Элемент</span><span class="sxs-lookup"><span data-stu-id="d51c2-105">Element</span></span>          | <span data-ttu-id="d51c2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d51c2-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51c2-107">Имена протоколов</span><span class="sxs-lookup"><span data-stu-id="d51c2-107">Protocol name(s)</span></span> | <span data-ttu-id="d51c2-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="d51c2-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="d51c2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d51c2-109">Description</span></span>      | <span data-ttu-id="d51c2-110">Предоставляет транспортные службы на уровне IP-сети: UDP для ненадежных датаграмм, TCP для надежных потоков байтов, ориентированных на подключение.</span><span class="sxs-lookup"><span data-stu-id="d51c2-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="d51c2-111">Семейство адресов</span><span class="sxs-lookup"><span data-stu-id="d51c2-111">Address family</span></span>   | <span data-ttu-id="d51c2-112">**AF \_ INET**, **AF \_ INET6**</span><span class="sxs-lookup"><span data-stu-id="d51c2-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="d51c2-113">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="d51c2-113">Header file</span></span>      | <span data-ttu-id="d51c2-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="d51c2-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="d51c2-115">Предлагаются два основных типа транспортных служб: ненадежные датаграммы (UDP) и надежные ориентированные на подключение потоки (TCP).</span><span class="sxs-lookup"><span data-stu-id="d51c2-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="d51c2-116">Кроме того, необработанный сокет необязательно поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d51c2-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="d51c2-117">Необработанные сокеты позволяют приложению взаимодействовать через протоколы, отличные от TCP и UDP, такие как ICMP.</span><span class="sxs-lookup"><span data-stu-id="d51c2-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="d51c2-118">Необработанные сокеты поддерживаются в семействах адресов **AF \_ inet** и **AF \_ INET6** с некоторыми ограничениями.</span><span class="sxs-lookup"><span data-stu-id="d51c2-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="d51c2-119">В этом разделе описываются расширения для Winsock, характерные для протоколов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d51c2-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="d51c2-120">Здесь также описываются аспекты базовых функций Winsock, требующих особого внимания или которые могут привести к уникальному поведению при использовании TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d51c2-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



