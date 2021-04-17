---
description: Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера. Используйте следующие функции для получения и изменения таблицы ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Использование протокола разрешения адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674313"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="da216-104">Использование протокола разрешения адресов</span><span class="sxs-lookup"><span data-stu-id="da216-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="da216-105">Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="da216-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="da216-106">Используйте следующие функции для получения и изменения таблицы ARP.</span><span class="sxs-lookup"><span data-stu-id="da216-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="da216-107">[**Жетипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) ИЗВЛЕКАЕТ таблицу ARP.</span><span class="sxs-lookup"><span data-stu-id="da216-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="da216-108">Таблица ARP содержит сопоставление IP-адресов с физическими адресами.</span><span class="sxs-lookup"><span data-stu-id="da216-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="da216-109">Физические адреса иногда называются MAC-адресами.</span><span class="sxs-lookup"><span data-stu-id="da216-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="da216-110">Используйте функции [**креатеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) и [**делетеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) для добавления или удаления определенных записей ARP в таблице или из нее.</span><span class="sxs-lookup"><span data-stu-id="da216-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="da216-111">Функция [**флушипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) удаляет все записи из таблицы.</span><span class="sxs-lookup"><span data-stu-id="da216-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="da216-112">Чтобы создать или удалить записи прокси-сервера ARP, используйте функции [**креатепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) и [**делетепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .</span><span class="sxs-lookup"><span data-stu-id="da216-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="da216-113">Функция [**сендарп**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) ОТПРАВЛЯЕТ запрос ARP в локальную сеть.</span><span class="sxs-lookup"><span data-stu-id="da216-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



