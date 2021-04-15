---
description: Вспомогательный модуль IP может помочь в управлении IP-адресами, связанными с интерфейсами на локальном компьютере. Используйте функции, описанные в следующих параграфах, для управления IP-адресами.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Управление IP-адресами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682616"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="50777-104">Управление IP-адресами</span><span class="sxs-lookup"><span data-stu-id="50777-104">Managing IP Addresses</span></span>

<span data-ttu-id="50777-105">Вспомогательный модуль IP может помочь в управлении IP-адресами, связанными с интерфейсами на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="50777-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="50777-106">Используйте функции, описанные в следующих параграфах, для управления IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="50777-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="50777-107">Функция [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) извлекает таблицу, содержащую сопоставление IP-адресов с интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="50777-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="50777-108">С одним интерфейсом может быть связано более одного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="50777-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="50777-109">Используйте функцию [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) для добавления IP-адреса к определенному интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="50777-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="50777-110">Чтобы удалить IP-адреса, которые были ранее добавлены с помощью **аддипаддресс**, используйте функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="50777-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="50777-111">Для функций [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) требуется, чтобы локальный компьютер использовал протокол DHCP.</span><span class="sxs-lookup"><span data-stu-id="50777-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="50777-112">Функция **ипрелеасеаддресс** освобождает IP-адрес, который ранее был ПОЛУЧЕН от DHCP.</span><span class="sxs-lookup"><span data-stu-id="50777-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="50777-113">Функция **ипреневаддресс** ОБНОВЛЯЕТ аренду DHCP по ОПРЕДЕЛЕННОМУ IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="50777-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="50777-114">Аренда DHCP позволяет компьютеру использовать IP-адрес в течение указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="50777-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="50777-115">Примеры кода, включающие [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , см. [в разделе Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="50777-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="50777-116">Примеры кода, включающие [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) и [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), см. в разделе [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="50777-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="50777-117">Примеры кода, включающие [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , см. [в разделе Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="50777-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



