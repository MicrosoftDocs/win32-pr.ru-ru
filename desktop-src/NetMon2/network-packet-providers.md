---
description: Поставщики сетевых пакетов (НППС) — это сетевой монитор компоненты системы, собирающие сетевой трафик (кадры) из сети и передающие их в пользовательский интерфейс сетевой монитор и приложения НПП.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Поставщики сетевых пакетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913443"
---
# <a name="network-packet-providers"></a><span data-ttu-id="0b17e-103">Поставщики сетевых пакетов</span><span class="sxs-lookup"><span data-stu-id="0b17e-103">Network Packet Providers</span></span>

<span data-ttu-id="0b17e-104">Поставщики сетевых пакетов (НППС) — это сетевой монитор компоненты системы, собирающие сетевой трафик (кадры) из сети и передающие их в пользовательский интерфейс сетевой монитор и [*приложения НПП*](n.md).</span><span class="sxs-lookup"><span data-stu-id="0b17e-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="0b17e-105">На следующем рисунке показаны два НППС: NDIS НПП, предоставляемый сетевой монитор, и настраиваемый НПП.</span><span class="sxs-lookup"><span data-stu-id="0b17e-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NDIS НПП, предоставляемый сетевым монитором и пользовательским НПП](images/npp.png)

<span data-ttu-id="0b17e-107">НПП NDIS, предоставляемый сетевой монитор, Ndisnpp.dll.</span><span class="sxs-lookup"><span data-stu-id="0b17e-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="0b17e-108">В этом НПП используется драйвер сетевой монитор системы (Nmnt.sys) для получения кадров, собранных из сети, и нескольких COM-интерфейсов (называемых интерфейсами НПП) для передачи кадров в пользовательский интерфейс сетевой монитор, а также приложений НПП, где их можно просматривать и анализировать.</span><span class="sxs-lookup"><span data-stu-id="0b17e-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="0b17e-109">Ndisnpp.dll подключается к слою [*NDIS*](n.md) для получения сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="0b17e-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="0b17e-110">(Пользовательское НППС может обойти уровень NDIS и напрямую взаимодействовать с сетевым оборудованием). Имейте в виду, что независимо от того, использует ли НПП интерфейс NDIS, НППС может подключаться к любому числу сетевых карт и что все НППС должны поддерживать одни и те же интерфейсы НПП.</span><span class="sxs-lookup"><span data-stu-id="0b17e-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="0b17e-111">Прежде чем приложение сможет начать сбор данных, оно должно:</span><span class="sxs-lookup"><span data-stu-id="0b17e-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="0b17e-112">Выберите сетевой адаптер, который будет подключать НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="0b17e-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="0b17e-113">Выберите интерфейс НПП, который будет использоваться для записи кадров сети.</span><span class="sxs-lookup"><span data-stu-id="0b17e-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="0b17e-114">Используйте выбранный интерфейс для подключения к сетевой карте.</span><span class="sxs-lookup"><span data-stu-id="0b17e-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="0b17e-115">Дополнительные сведения о том, как перечислить и выбрать сетевой адаптер, см. [в разделе Выбор сетевой](selecting-a-network-interface-card.md)карты.</span><span class="sxs-lookup"><span data-stu-id="0b17e-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="0b17e-116">Дополнительные сведения о COM-интерфейсах, предоставляемых НППС, см. [в разделе Выбор интерфейса НПП](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0b17e-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b17e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0b17e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b17e-118">**иделайдк**</span><span class="sxs-lookup"><span data-stu-id="0b17e-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0b17e-119">**иесп**</span><span class="sxs-lookup"><span data-stu-id="0b17e-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="0b17e-120">**иртк**</span><span class="sxs-lookup"><span data-stu-id="0b17e-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="0b17e-121">**истатс**</span><span class="sxs-lookup"><span data-stu-id="0b17e-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



