---
title: Протокол Teredo
description: Протокол Teredo
ms.assetid: fc213675-dbdb-42a1-a09f-dda598b95b94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e1a2717f3732c32f2c1fe4104c8edd2f802ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105652"
---
# <a name="teredo"></a><span data-ttu-id="9d878-103">Протокол Teredo</span><span class="sxs-lookup"><span data-stu-id="9d878-103">Teredo</span></span>

## <a name="purpose"></a><span data-ttu-id="9d878-104">Цель</span><span class="sxs-lookup"><span data-stu-id="9d878-104">Purpose</span></span>

<span data-ttu-id="9d878-105">Teredo — это технология туннелирования IPv6, которая обеспечивает назначение адресов и автоматическое туннелирование между узлами для одноадресного трафика IPv6, когда узлы IPv6 и IPv4 находятся за одним или несколькими трансляторами сетевых адресов (NAT) IPv4.</span><span class="sxs-lookup"><span data-stu-id="9d878-105">Teredo is an IPv6 transition technology that provides address assignment and host-to-host automatic tunneling for unicast IPv6 traffic when IPv6/IPv4 hosts are located behind one or multiple IPv4 network address translators (NATs).</span></span> <span data-ttu-id="9d878-106">Для обхода NAT протоколов IPv4 пакеты IPv6 отправляются в виде сообщений UDP.</span><span class="sxs-lookup"><span data-stu-id="9d878-106">To traverse IPv4 NATs, IPv6 packets are sent as IPv4 User Datagram Protocol (UDP) messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9d878-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="9d878-107">Developer audience</span></span>

<span data-ttu-id="9d878-108">Teredo предназначен для использования разработчиками C/C++ с возможностями сетевого программирования IPv6.</span><span class="sxs-lookup"><span data-stu-id="9d878-108">Teredo is designed for use by C/C++ developers with IPv6 network programming experience.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9d878-109">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="9d878-109">Run-time requirements</span></span>

<span data-ttu-id="9d878-110">Интерфейс Teredo в основном поддерживается Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9d878-110">The Teredo interface is primarily supported by Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9d878-111">Ограниченная функциональность интерфейса Teredo, поддерживаемого Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003, подробно описана в разделе [Получение запрошенного трафика через Teredo](receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="9d878-111">The limited functionality of the Teredo Interface supported by Windows XP with Service Pack 2 (SP2) and Windows Server 2003 is detailed in [Receiving Solicited Traffic Over Teredo](receiving-solicited-traffic-over-teredo.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d878-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9d878-112">In this section</span></span>



| <span data-ttu-id="9d878-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="9d878-113">Topic</span></span>                                       | <span data-ttu-id="9d878-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9d878-114">Description</span></span>                                                                                |
|---------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d878-115">О Teredo</span><span class="sxs-lookup"><span data-stu-id="9d878-115">About Teredo</span></span>](about-teredo.md)<br/> | <span data-ttu-id="9d878-116">Сведения об интерфейсе Teredo.</span><span class="sxs-lookup"><span data-stu-id="9d878-116">Information about the Teredo interface.</span></span><br/>                                         |
| [<span data-ttu-id="9d878-117">Использование Teredo</span><span class="sxs-lookup"><span data-stu-id="9d878-117">Using Teredo</span></span>](using-teredo.md)<br/> | <span data-ttu-id="9d878-118">Сведения о реализации и общем использовании интерфейса Teredo.</span><span class="sxs-lookup"><span data-stu-id="9d878-118">Information about the implementation and general usage of the Teredo Interface.</span></span><br/> |



 

 

 





