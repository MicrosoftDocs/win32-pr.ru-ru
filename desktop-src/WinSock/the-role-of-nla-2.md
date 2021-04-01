---
description: Поставщик службы сетевого расположения (NLA) является жизненно важным для компьютеров или устройств, которые могут перемещаться между различными сетями, а также для выбора оптимальных конфигураций, когда доступно более одного.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Роль NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263942"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="08cc9-103">Роль NLA</span><span class="sxs-lookup"><span data-stu-id="08cc9-103">The Role of NLA</span></span>

<span data-ttu-id="08cc9-104">Поставщик службы сетевого расположения (NLA) является жизненно важным для компьютеров или устройств, которые могут перемещаться между различными сетями, а также для выбора оптимальных конфигураций, когда доступно более одного.</span><span class="sxs-lookup"><span data-stu-id="08cc9-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="08cc9-105">Например, Беспроводной компьютер, перемещаемый между физическими сетями, может использовать NLA для определения правильной конфигурации на основе сведений о доступном сетевом подключении.</span><span class="sxs-lookup"><span data-stu-id="08cc9-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="08cc9-106">NLA также подтверждает ценность, когда компьютер с несколькими сетями физически подключен к одной сети, а также подключен к другой сети через коммутируемое подключение или туннель.</span><span class="sxs-lookup"><span data-stu-id="08cc9-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="08cc9-107">В прошлом разработчикам пришлось получать сведения о логическом сетевом интерфейсе и, таким образом, принимать решения о сетевом подключении, основываясь на множестве разнородных сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="08cc9-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="08cc9-108">В таких случаях разработчикам пришлось выбирать соответствующий сетевой интерфейс на основе IP-адреса, подсети интерфейса, DNS-имени, связанного с интерфейсом, MAC-адреса сетевой карты, имени беспроводной сети или других сетевых сведений.</span><span class="sxs-lookup"><span data-stu-id="08cc9-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="08cc9-109">NLA устраняет эту проблему, предоставляя стандартный интерфейс для перечисления данных логических сетевых вложений, сопоставляя его с данными физического сетевого интерфейса, а затем предоставляя уведомление, когда ранее возвращенные сведения станут недействительными.</span><span class="sxs-lookup"><span data-stu-id="08cc9-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="08cc9-110">NLA предоставляет следующие сведения о сетевом расположении:</span><span class="sxs-lookup"><span data-stu-id="08cc9-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="08cc9-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Удостоверение логической сети</span><span class="sxs-lookup"><span data-stu-id="08cc9-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="08cc9-112">Служба NLA сначала пытается опознать логическую сеть по ее доменному имени DNS.</span><span class="sxs-lookup"><span data-stu-id="08cc9-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="08cc9-113">Если логическая сеть не имеет доменного имени, NLA определяет сеть на основе настраиваемой статической информации, хранящейся в реестре, и, наконец, из адреса его подсети.</span><span class="sxs-lookup"><span data-stu-id="08cc9-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="08cc9-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Логические сетевые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="08cc9-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="08cc9-115">Для каждой сети, к которой подключен компьютер, NLA предоставляет *адаптернаме* , который однозначно определяет физический интерфейс, например сетевую карту, или логический интерфейс, например подключение RAS.</span><span class="sxs-lookup"><span data-stu-id="08cc9-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="08cc9-116">Затем Адаптернаме можно использовать с функциями, доступными в API вспомогательной функции IP для получения дополнительных характеристик интерфейса.</span><span class="sxs-lookup"><span data-stu-id="08cc9-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="08cc9-117">NLA реализует логическую сеть как класс службы с соответствующим идентификатором GUID и свойствами класса.</span><span class="sxs-lookup"><span data-stu-id="08cc9-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="08cc9-118">Каждая логическая сеть, для которой Служба NLA возвращает сведения, является экземпляром этого класса службы.</span><span class="sxs-lookup"><span data-stu-id="08cc9-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



