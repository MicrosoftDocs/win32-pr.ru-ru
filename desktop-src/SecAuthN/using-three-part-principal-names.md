---
description: При создании пакета безопасности поставщика поддержки безопасности (SSP) не следует разрешать проверку подлинности клиента, присоединенного к домену, на контроллере домена с помощью имени поставщика услуг (SPN) из двух частей в следующей форме.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Использование трех имен субъектов-частей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662367"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="492b0-103">Использование трех имен субъектов-частей</span><span class="sxs-lookup"><span data-stu-id="492b0-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="492b0-104">При создании пакета безопасности поставщика поддержки безопасности (SSP) не следует разрешать проверку подлинности клиента, присоединенного к домену, на контроллере домена с помощью имени поставщика услуг (SPN) из двух частей в следующей форме.</span><span class="sxs-lookup"><span data-stu-id="492b0-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="492b0-105"><*протокол* >/< *имя узла*></span><span class="sxs-lookup"><span data-stu-id="492b0-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="492b0-106">Клиент должен всегда проходить проверку подлинности, указывая домен.</span><span class="sxs-lookup"><span data-stu-id="492b0-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="492b0-107"><*протокол* >/< *имя узла* >/< *доменное имя*></span><span class="sxs-lookup"><span data-stu-id="492b0-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="492b0-108">Клиент, присоединенный к домену, который входит в систему с именем субъекта-службы с двумя частями, может иметь возможность олицетворять контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="492b0-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="492b0-109">При разрешении двух частей имен участников-служб следует создать запись в журнале, содержащую достаточно сведений, чтобы администратор определял вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="492b0-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



