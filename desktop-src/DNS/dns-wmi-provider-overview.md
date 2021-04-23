---
title: Общие сведения о поставщике WMI DNS
description: Поставщик является элементом архитектуры инструментарий управления Windows (WMI) (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Система доменных имен, поставщик WMI, архитектура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067845"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="379d8-104">Общие сведения о поставщике WMI DNS</span><span class="sxs-lookup"><span data-stu-id="379d8-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="379d8-105">Поставщик является элементом архитектуры *инструментарий управления Windows (WMI) (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="379d8-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="379d8-106">WMI определяет единую архитектуру для описания, доступа и инструментирования объектов.</span><span class="sxs-lookup"><span data-stu-id="379d8-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="379d8-107">Частью этой архитектуры является большая база данных классов WMI, используемых для выполнения задач удаленного управления на конкретных объектах.</span><span class="sxs-lookup"><span data-stu-id="379d8-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="379d8-108">Поставщики WMI действуют как посредники между WMI и одним или несколькими управляемыми объектами.</span><span class="sxs-lookup"><span data-stu-id="379d8-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="379d8-109">Когда WMI получает запрос от приложения управления для данных, недоступных из репозитория CIM, или для уведомлений о событиях, которые не поддерживаются инструментарием WMI, он перенаправляет запрос поставщику.</span><span class="sxs-lookup"><span data-stu-id="379d8-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="379d8-110">Поставщики предоставляют данные и уведомления о событиях для управляемых объектов, которые находятся в их домене.</span><span class="sxs-lookup"><span data-stu-id="379d8-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="379d8-111">Поставщик расширяет схему WMI классов, позволяя инструментарию WMI работать с новыми типами объектов.</span><span class="sxs-lookup"><span data-stu-id="379d8-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="379d8-112">Поставщик WMI для DNS определяет классы для запроса и настройки DNS-сервера, а также связанные с ним зоны DNS и записи DNS.</span><span class="sxs-lookup"><span data-stu-id="379d8-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="379d8-113">Поставщик WMI для DNS предоставляет клиентам несколько объектов DNS, включая DNS-сервер, домен DNS и объекты RR DNS.</span><span class="sxs-lookup"><span data-stu-id="379d8-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="379d8-114">С помощью этих объектов клиенты могут выполнять действия по управлению DNS.</span><span class="sxs-lookup"><span data-stu-id="379d8-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="379d8-115">С помощью поставщика WMI для DNS можно создавать собственные средства для выполнения большинства задач администрирования DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="379d8-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="379d8-116">Например, можно создавать, удалять и просматривать зоны и записи. Сброс свойств сервера и зоны; и выполняют стандартные операции администрирования, такие как обновление зоны, повторная загрузка зоны, обновление зоны, запись зоны обратно в файл или Active Directory, приостановка и возобновление работы зоны, очистка кэша, остановка и запуск службы DNS, а также просмотр статистики.</span><span class="sxs-lookup"><span data-stu-id="379d8-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="379d8-117">Поставщик WMI DNS имеет набор уникальных поведений, не найденных в других поставщиках.</span><span class="sxs-lookup"><span data-stu-id="379d8-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="379d8-118">Сведения о классах см. в [справочнике по поставщику WMI DNS](dns-wmi-provider-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="379d8-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 




