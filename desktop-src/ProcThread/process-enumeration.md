---
description: Все пользователи имеют доступ на чтение к списку процессов в системе, и существует ряд различных функций, выполняющих перечисление активных процессов. Функция, которую следует использовать, зависит от таких факторов, как поддержка требуемой платформы.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Перечисление процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673747"
---
# <a name="process-enumeration"></a><span data-ttu-id="906b0-104">Перечисление процессов</span><span class="sxs-lookup"><span data-stu-id="906b0-104">Process Enumeration</span></span>

<span data-ttu-id="906b0-105">Все пользователи имеют доступ на чтение к списку процессов в системе, и существует ряд различных функций, выполняющих перечисление активных процессов.</span><span class="sxs-lookup"><span data-stu-id="906b0-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="906b0-106">Функция, которую следует использовать, зависит от таких факторов, как поддержка требуемой платформы.</span><span class="sxs-lookup"><span data-stu-id="906b0-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="906b0-107">Для перечисления процессов используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="906b0-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="906b0-108">Функция</span><span class="sxs-lookup"><span data-stu-id="906b0-108">Function</span></span>                                                    | <span data-ttu-id="906b0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="906b0-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="906b0-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="906b0-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="906b0-111">Получает идентификатор процесса для каждого объекта процесса в системе.</span><span class="sxs-lookup"><span data-stu-id="906b0-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="906b0-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="906b0-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="906b0-113">Извлекает сведения о первом процессе, обнаруженном в системном снимке.</span><span class="sxs-lookup"><span data-stu-id="906b0-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="906b0-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="906b0-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="906b0-115">Извлекает сведения о следующем процессе, записанном в системном снимке.</span><span class="sxs-lookup"><span data-stu-id="906b0-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="906b0-116">**втсенумератепроцессес**</span><span class="sxs-lookup"><span data-stu-id="906b0-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="906b0-117">Извлекает сведения об активных процессах на указанном сервере терминалов.</span><span class="sxs-lookup"><span data-stu-id="906b0-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="906b0-118">Функции тулхелп и [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) перечисляют весь процесс.</span><span class="sxs-lookup"><span data-stu-id="906b0-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="906b0-119">Чтобы получить список процессов, выполняемых в определенной учетной записи пользователя, используйте [**втсенумератепроцессес**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) и выполните фильтрацию по идентификатору безопасности пользователя.</span><span class="sxs-lookup"><span data-stu-id="906b0-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="906b0-120">Можно выполнить фильтрацию по ИДЕНТИФИКАТОРу сеанса, чтобы скрыть процессы, выполняющиеся в других сеансах сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="906b0-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="906b0-121">Можно также фильтровать процессы по учетной записи пользователя независимо от функции перечисления, вызывая [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)и [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) с **токенусер**.</span><span class="sxs-lookup"><span data-stu-id="906b0-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="906b0-122">Однако нельзя открыть процесс, защищенный дескриптором безопасности, если вы не предоставили доступ.</span><span class="sxs-lookup"><span data-stu-id="906b0-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
