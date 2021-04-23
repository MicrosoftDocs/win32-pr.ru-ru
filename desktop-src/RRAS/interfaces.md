---
title: Интерфейсы RAS
description: Интерфейс представляет сеть, к которой можно подключиться через адаптер ЛВС или WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103890068"
---
# <a name="ras-interfaces"></a><span data-ttu-id="95ada-103">Интерфейсы RAS</span><span class="sxs-lookup"><span data-stu-id="95ada-103">RAS interfaces</span></span>

<span data-ttu-id="95ada-104">Интерфейс представляет сеть, к которой можно подключиться через адаптер ЛВС или WAN.</span><span class="sxs-lookup"><span data-stu-id="95ada-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="95ada-105">Каждый интерфейс имеет уникальный идентификатор маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="95ada-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="95ada-106">Активные интерфейсы имеют адаптер, обеспечивающий подключение к сети, которую они представляют.</span><span class="sxs-lookup"><span data-stu-id="95ada-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="95ada-107">Неактивные интерфейсы не имеют адаптера, предоставляющего возможность подключения, если только администратор не отключил интерфейс после того, как он уже имел адаптер.</span><span class="sxs-lookup"><span data-stu-id="95ada-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="95ada-108">Маршрутизация пакета в сеть, представленная интерфейсом, приведет к тому, что маршрутизатор выделит адаптер для этого интерфейса и установит подключение к удаленной сети через ГЛОБАЛЬную сеть.</span><span class="sxs-lookup"><span data-stu-id="95ada-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="95ada-109">Выделение адаптера для интерфейса называется *привязкой*.</span><span class="sxs-lookup"><span data-stu-id="95ada-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="95ada-110">Интерфейсы являются управляемыми объектами.</span><span class="sxs-lookup"><span data-stu-id="95ada-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="95ada-111">Каждый интерфейс отображается в виде строки в таблице Interface соответствующей SNMP MIB.</span><span class="sxs-lookup"><span data-stu-id="95ada-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>