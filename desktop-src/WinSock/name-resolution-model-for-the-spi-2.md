---
description: Модель разрешения имен и регистрации для сокетов Windows (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Модель разрешения имен для SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145001"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="4eef7-103">Модель разрешения имен для SPI</span><span class="sxs-lookup"><span data-stu-id="4eef7-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="4eef7-104">При разработке независимого от протокола клиентского или серверного приложения существует два основных требования, которые связаны с разрешением имен и регистрацией:</span><span class="sxs-lookup"><span data-stu-id="4eef7-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="4eef7-105">Возможность серверной части приложения (затем называемой службой) регистрировать свое существование в одном или нескольких пространствах имен (или стать доступным).</span><span class="sxs-lookup"><span data-stu-id="4eef7-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="4eef7-106">Способность клиентского приложения находить службу в пространстве имен и получать требуемый транспортный протокол и сведения об адресации.</span><span class="sxs-lookup"><span data-stu-id="4eef7-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="4eef7-107">Для тех, которые привыкли разрабатывать приложения на основе TCP/IP, это может потребовать немного больше, чем поиск адреса узла, а затем использовать согласованный по номеру порта.</span><span class="sxs-lookup"><span data-stu-id="4eef7-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="4eef7-108">Другие схемы сети, тем не менее, разрешают расположение службы, протокол, используемый для службы, и другие атрибуты, которые обнаруживаются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4eef7-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="4eef7-109">Для поддержки диапазона возможностей в существующих службах имен интерфейс Windows Sockets 2 использует модель, описанную ниже.</span><span class="sxs-lookup"><span data-stu-id="4eef7-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="4eef7-110">*Пространство имен* относится к некоторой возможности для сопоставления (как минимум) протокола и адресации атрибутов сетевой службы с одним или несколькими понятными именами.</span><span class="sxs-lookup"><span data-stu-id="4eef7-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="4eef7-111">В настоящее время многие пространства имен используются в широком спектре, включая систему доменных имен (DNS), службы каталогов NetWare, X. 500 и т. д. Эти пространства имен могут сильно различаться в том, как они организованы и реализованы.</span><span class="sxs-lookup"><span data-stu-id="4eef7-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="4eef7-112">Некоторые из их свойств особенно важны для понимания с точки зрения разрешения имен Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="4eef7-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



