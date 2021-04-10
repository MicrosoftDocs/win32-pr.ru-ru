---
description: Персональные компьютеры под управлением Microsoft Windows часто имеют множество сетевых подключений, например несколько сетевых карт (NIC), подключенных к разным сетям, или физическое сетевое подключение и коммутируемое подключение.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Поставщик службы обнаружения сетевых расположений (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144992"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="03c42-103">Поставщик службы обнаружения сетевых расположений (NLA)</span><span class="sxs-lookup"><span data-stu-id="03c42-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="03c42-104">Персональные компьютеры под управлением Microsoft Windows часто имеют множество сетевых подключений, например несколько сетевых карт (NIC), подключенных к разным сетям, или физическое сетевое подключение и коммутируемое подключение.</span><span class="sxs-lookup"><span data-stu-id="03c42-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="03c42-105">Сокеты Windows способны перечислить доступные сетевые интерфейсы в течение некоторого времени, но некоторые важные сведения о сетевых подключениях ранее были недоступны.</span><span class="sxs-lookup"><span data-stu-id="03c42-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="03c42-106">Сюда входят такие сведения, как логическая сеть, к которой подключен компьютер Windows, или несколько интерфейсов, подключенных к одной сети.</span><span class="sxs-lookup"><span data-stu-id="03c42-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="03c42-107">Поставщик службы сетевого расположения, который обычно называется NLA, позволяет приложениям Windows Sockets 2 находить логическую сеть, к которой подключен компьютер Windows.</span><span class="sxs-lookup"><span data-stu-id="03c42-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="03c42-108">Кроме того, NLA позволяет приложениям Windows Sockets обнаруживать, каким физическим сетевым интерфейсом данного приложения были сохранены определенные сведения.</span><span class="sxs-lookup"><span data-stu-id="03c42-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="03c42-109">NLA реализован в виде универсального поставщика службы разрешения имен Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="03c42-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



