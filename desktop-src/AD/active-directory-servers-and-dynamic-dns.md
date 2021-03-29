---
title: Серверы Active Directory и динамические DNS
description: Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- динамическое DNS-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772758"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="db3a0-104">Серверы Active Directory и динамические DNS</span><span class="sxs-lookup"><span data-stu-id="db3a0-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="db3a0-105">Active Directory серверы публикуют свои адреса, чтобы клиенты могли найти их, зная только имя домена.</span><span class="sxs-lookup"><span data-stu-id="db3a0-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="db3a0-106">Active Directory серверы публикуются с помощью записей ресурсов службы (RR SRV) в DNS.</span><span class="sxs-lookup"><span data-stu-id="db3a0-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="db3a0-107">SRV RR — это запись DNS, используемая для соответствия имени службы адресу сервера, который предлагает службу.</span><span class="sxs-lookup"><span data-stu-id="db3a0-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="db3a0-108">Имя RR SRV имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="db3a0-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="db3a0-109">Active Directory серверы предлагают службу LDAP по протоколу TCP, чтобы опубликованные имена были "LDAP. TCP <domain> ".</span><span class="sxs-lookup"><span data-stu-id="db3a0-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="db3a0-110">Таким же параметром SRV RR для fabrikam.com является «ldap.tcp.fabrikam.com».</span><span class="sxs-lookup"><span data-stu-id="db3a0-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="db3a0-111">Дополнительные данные о записи ресурса SRV указывают приоритет и вес для сервера, позволяя клиентам выбирать оптимальный сервер в соответствии с потребностями.</span><span class="sxs-lookup"><span data-stu-id="db3a0-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="db3a0-112">При установке сервера Active Directory он использует динамическое DNS для публикации.</span><span class="sxs-lookup"><span data-stu-id="db3a0-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="db3a0-113">Так как TCP/IP-адреса могут быть изменены, серверы периодически проверяют свои регистрации, чтобы убедиться в их правильности, и при необходимости обновляйте их.</span><span class="sxs-lookup"><span data-stu-id="db3a0-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="db3a0-114">Динамическое DNS — это последнее дополнение к стандарту DNS.</span><span class="sxs-lookup"><span data-stu-id="db3a0-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="db3a0-115">Динамическая DNS определяет протокол для динамического обновления DNS-сервера новыми данными.</span><span class="sxs-lookup"><span data-stu-id="db3a0-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="db3a0-116">До динамического DNS администраторам требовалось вручную настраивать записи, хранящиеся в DNS-серверах.</span><span class="sxs-lookup"><span data-stu-id="db3a0-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




