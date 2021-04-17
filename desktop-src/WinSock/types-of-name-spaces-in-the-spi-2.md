---
description: Три типа пространств имен в списке безопасности сокетов Windows (Winsock) включают динамические, статические и постоянные пространства имен.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Типы пространств имен в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693387"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="cd8ed-103">Типы пространств имен в SPI</span><span class="sxs-lookup"><span data-stu-id="cd8ed-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="cd8ed-104">Существует три разных типа пространств имен, в которых может быть зарегистрирована служба:</span><span class="sxs-lookup"><span data-stu-id="cd8ed-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="cd8ed-105">Динамический</span><span class="sxs-lookup"><span data-stu-id="cd8ed-105">Dynamic</span></span>
-   <span data-ttu-id="cd8ed-106">Статические</span><span class="sxs-lookup"><span data-stu-id="cd8ed-106">Static</span></span>
-   <span data-ttu-id="cd8ed-107">Постоянный</span><span class="sxs-lookup"><span data-stu-id="cd8ed-107">Persistent</span></span>

<span data-ttu-id="cd8ed-108">Динамические пространства имен позволяют службам регистрироваться в пространстве имен на лету, а клиенты могут обнаруживать доступные службы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="cd8ed-109">Динамические пространства имен часто полагаются на широковещательные рассылки, чтобы указать на непрерывную доступность сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="cd8ed-110">Примеры динамических пространств имен включают пространство имен SAP, используемое в среде NetWare, и пространство имен NBP, используемое протоколом AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="cd8ed-111">Для статических пространств имен все службы должны быть зарегистрированы заранее, то есть при создании пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="cd8ed-112">DNS является примером статического пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="cd8ed-113">Хотя существует программный способ разрешения имен, не существует программного способа регистрации имен.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="cd8ed-114">Постоянные пространства имен позволяют службам регистрироваться в пространстве имен в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="cd8ed-115">В отличие от динамических пространств имен, постоянные пространства имен сохранит сведения о регистрации в энергонезависимом хранилище, где они остаются до тех пор, пока не будут удалены запросы службы.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="cd8ed-116">Постоянные пространства имен типифиед такими службами каталогов, как X. 500 и NDS (Служба каталогов NetWare).</span><span class="sxs-lookup"><span data-stu-id="cd8ed-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="cd8ed-117">Эти среды позволяют добавлять, удалять и изменять свойства службы.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="cd8ed-118">Кроме того, объект службы, представляющий службу в службе каталогов, может иметь разнообразные атрибуты, связанные со службой.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="cd8ed-119">Наиболее важным атрибутом для клиентских приложений являются сведения об адресации службы.</span><span class="sxs-lookup"><span data-stu-id="cd8ed-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



