---
description: Содержит список и описание обязанностей модели GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Обязанности модели GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080748"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="abf27-103">Обязанности модели GINA</span><span class="sxs-lookup"><span data-stu-id="abf27-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="abf27-104">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="abf27-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="abf27-105">Библиотека DLL [*GINA*](../secgloss/g-gly.md) имеет следующие обязанности:</span><span class="sxs-lookup"><span data-stu-id="abf27-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="abf27-106">Мониторинг SAS</span><span class="sxs-lookup"><span data-stu-id="abf27-106">SAS monitoring</span></span>

    <span data-ttu-id="abf27-107">GINA отвечает за распознавание [*последовательности защиты*](../secgloss/s-gly.md) (SAS), мониторинг событий SAS и уведомление Winlogon при возникновении SAS.</span><span class="sxs-lookup"><span data-stu-id="abf27-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="abf27-108">Обратите внимание, что может быть определено несколько SAS, и набор определенных для них изменений со временем может измениться.</span><span class="sxs-lookup"><span data-stu-id="abf27-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="abf27-109">Например, может существовать один набор версий Sasser, когда [*Winlogon*](../secgloss/w-gly.md) находится в состоянии "отключено", и другой набор, когда он находится в состоянии "в системе".</span><span class="sxs-lookup"><span data-stu-id="abf27-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="abf27-110">Winlogon предоставляет службы, помогающие модели GINA использовать сочетание безопасности CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="abf27-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="abf27-111">Обработка SAS</span><span class="sxs-lookup"><span data-stu-id="abf27-111">SAS processing</span></span>

    <span data-ttu-id="abf27-112">Одной из причин для замены модели GINA является предоставление альтернативных механизмов идентификации и проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="abf27-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="abf27-113">Для этого GINA должен представлять все пользовательские интерфейсы, полученные в результате распознавания SAS.</span><span class="sxs-lookup"><span data-stu-id="abf27-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="abf27-114">Если ни один пользователь не вошел в систему, GINA несет ответственность за представление параметров идентификации и проверки подлинности, а также любые другие допустимые параметры, которые не прошли проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="abf27-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="abf27-115">Когда пользователь вошел в систему, GINA несет ответственность за представление соответствующих параметров для пользователя, а также принятие всех необходимых действий.</span><span class="sxs-lookup"><span data-stu-id="abf27-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="abf27-116">Например, в системе, содержащей [*смарт-карту*](../secgloss/s-gly.md), может быть предусмотрена автоматическая блокировка рабочей станции, если пользователь удаляет смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="abf27-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="abf27-117">Активация оболочки</span><span class="sxs-lookup"><span data-stu-id="abf27-117">Shell activation</span></span>

    <span data-ttu-id="abf27-118">При входе пользователя в систему GINA отвечает за создание одного или нескольких начальных процессов для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="abf27-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="abf27-119">(В этой документации предполагается, что эти начальные процессы предоставляют пользователю интерфейс.</span><span class="sxs-lookup"><span data-stu-id="abf27-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="abf27-120">Однако эти процессы фактически могут быть любыми процессами и не обязательно должны взаимодействовать с пользователем.) Эти процессы называются *пользовательской оболочкой* или просто *оболочкой*.</span><span class="sxs-lookup"><span data-stu-id="abf27-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="abf27-121">В рамках активации оболочки GINA должен назначить процессам маркер пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="abf27-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="abf27-122">Winlogon предоставляет службу, помогающую GINA в назначении маркера.</span><span class="sxs-lookup"><span data-stu-id="abf27-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
