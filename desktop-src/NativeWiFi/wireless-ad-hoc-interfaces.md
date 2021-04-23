---
description: Интерфейс беспроводного программирования нерегламентированный компьютер состоит из следующих интерфейсов.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Беспроводные нерегламентированные интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673489"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="b1095-103">Беспроводные нерегламентированные интерфейсы</span><span class="sxs-lookup"><span data-stu-id="b1095-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="b1095-104">Интерфейс беспроводного программирования нерегламентированный компьютер состоит из следующих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b1095-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="b1095-105">Имя_интерфейса</span><span class="sxs-lookup"><span data-stu-id="b1095-105">Interface Name</span></span>                                                                       | <span data-ttu-id="b1095-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b1095-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1095-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="b1095-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="b1095-108">Представляет адаптер беспроводной сети (NIC).</span><span class="sxs-lookup"><span data-stu-id="b1095-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="b1095-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="b1095-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="b1095-110">Определяет уведомления, поддерживаемые [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span><span class="sxs-lookup"><span data-stu-id="b1095-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="b1095-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="b1095-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="b1095-112">Создает и управляет 802,11 нерегламентированных сетей.</span><span class="sxs-lookup"><span data-stu-id="b1095-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="b1095-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="b1095-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="b1095-114">Определяет уведомления, поддерживаемые интерфейсом [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) .</span><span class="sxs-lookup"><span data-stu-id="b1095-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="b1095-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="b1095-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="b1095-116">Представляет доступное нерегламентированное назначение сети в пределах диапазона подключений.</span><span class="sxs-lookup"><span data-stu-id="b1095-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="b1095-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="b1095-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="b1095-118">Определяет уведомления, поддерживаемые интерфейсом [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) .</span><span class="sxs-lookup"><span data-stu-id="b1095-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="b1095-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="b1095-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="b1095-120">Задает параметры безопасности для беспроводной сети "нерегламентированный компьютер".</span><span class="sxs-lookup"><span data-stu-id="b1095-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="b1095-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b1095-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="b1095-122">Представляет коллекцию видимых в настоящее время нерегламентированных сетевых интерфейсов 802,11.</span><span class="sxs-lookup"><span data-stu-id="b1095-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="b1095-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="b1095-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="b1095-124">Представляет коллекцию видимых в настоящее время 802,11 нерегламентированных сетей.</span><span class="sxs-lookup"><span data-stu-id="b1095-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="b1095-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="b1095-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="b1095-126">Представляет коллекцию параметров безопасности, связанных с каждой видимой беспроводной сетью нерегламентированных сетей.</span><span class="sxs-lookup"><span data-stu-id="b1095-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="b1095-127">Нерегламентированный режим может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="b1095-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="b1095-128">Начиная с Windows 8.1 и Windows Server 2012 R2, следует использовать [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="b1095-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



