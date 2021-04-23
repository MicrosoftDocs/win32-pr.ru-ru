---
title: Функции диспетчера перезапуска
description: API диспетчера перезапуска использует функции, указанные в следующей таблице.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Диспетчер перезапуска, ссылка, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888203"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="e973c-104">Функции диспетчера перезапуска</span><span class="sxs-lookup"><span data-stu-id="e973c-104">Restart Manager Functions</span></span>

<span data-ttu-id="e973c-105">API диспетчера перезапуска использует функции, указанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e973c-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="e973c-106">Функция</span><span class="sxs-lookup"><span data-stu-id="e973c-106">Function</span></span>                                           | <span data-ttu-id="e973c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e973c-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e973c-108">**рмаддфилтер**</span><span class="sxs-lookup"><span data-stu-id="e973c-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="e973c-109">Изменяет действия завершения работы или перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e973c-110">**RmStartSession**</span><span class="sxs-lookup"><span data-stu-id="e973c-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="e973c-111">Запускает новый сеанс диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e973c-112">**рмжоинсессион**</span><span class="sxs-lookup"><span data-stu-id="e973c-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="e973c-113">Присоединяет процесс приложения к существующему сеансу диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="e973c-114">**рмендсессион**</span><span class="sxs-lookup"><span data-stu-id="e973c-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="e973c-115">Завершает сеанс диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="e973c-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="e973c-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="e973c-117">Регистрирует ресурсы, такие как имена файлов, короткие имена служб или [**уникальные структуры \_ \_ процессов RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , в сеансе диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="e973c-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="e973c-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="e973c-119">Используется установщиками для получения списка всех приложений, затронутых зарегистрированными ресурсами, и их текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="e973c-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="e973c-120">**рмжетфилтерлист**</span><span class="sxs-lookup"><span data-stu-id="e973c-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="e973c-121">Запрашивает состояние завершения работы и перезапускает уже примененные изменения.</span><span class="sxs-lookup"><span data-stu-id="e973c-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="e973c-122">**рмшутдовн**</span><span class="sxs-lookup"><span data-stu-id="e973c-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="e973c-123">Инициирует завершение работы приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="e973c-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="e973c-124">**рмремовефилтер**</span><span class="sxs-lookup"><span data-stu-id="e973c-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="e973c-125">Удаляет уже примененные изменения для завершения работы и перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e973c-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="e973c-126">**рмрестарт**</span><span class="sxs-lookup"><span data-stu-id="e973c-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="e973c-127">Перезапускает приложения и службы, работа которых была завершена функцией [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) и которые были зарегистрированы для перезапуска с помощью **регистераппликатионрестарт**.</span><span class="sxs-lookup"><span data-stu-id="e973c-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="e973c-128">**рмканцелкурренттаск**</span><span class="sxs-lookup"><span data-stu-id="e973c-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="e973c-129">Отменяет текущую функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="e973c-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




