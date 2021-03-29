---
title: О диспетчере перезапуска
description: Основная причина установки и обновления программного обеспечения требует перезагрузки системы, так как некоторые обновляемые файлы в настоящее время используются запущенным приложением или службой.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Диспетчер перезапуска диспетчера перезагрузки, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793332"
---
# <a name="about-restart-manager"></a><span data-ttu-id="dac06-104">О диспетчере перезапуска</span><span class="sxs-lookup"><span data-stu-id="dac06-104">About Restart Manager</span></span>

<span data-ttu-id="dac06-105">Основная причина установки и обновления программного обеспечения требует перезагрузки системы, так как некоторые обновляемые файлы в настоящее время используются запущенным приложением или службой.</span><span class="sxs-lookup"><span data-stu-id="dac06-105">The primary reason software installation and updates require a system restart is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="dac06-106">Диспетчер перезапуска позволяет завершать работу и перезапускать все критические приложения и службы.</span><span class="sxs-lookup"><span data-stu-id="dac06-106">Restart Manager enables all but the critical applications and services to be shut down and restarted .</span></span> <span data-ttu-id="dac06-107">Это освобождает используемые файлы и позволяет выполнять операции установки.</span><span class="sxs-lookup"><span data-stu-id="dac06-107">This frees the files that are in use and allows installation operations to complete.</span></span> <span data-ttu-id="dac06-108">Он также может устранить или уменьшить количество перезапусков системы, необходимых для завершения установки или обновления.</span><span class="sxs-lookup"><span data-stu-id="dac06-108">It can also eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span>

<span data-ttu-id="dac06-109">Диспетчер перезапуска останавливает приложения в следующем порядке, а после обновления приложения перезапускает приложения, которые были зарегистрированы для перезапуска в обратную последовательность.</span><span class="sxs-lookup"><span data-stu-id="dac06-109">The Restart Manager stops applications in the following order, and after the applications have been updated, restarts applications that have been registered for restart in the reverse order.</span></span>

1.  <span data-ttu-id="dac06-110">Приложения GUI</span><span class="sxs-lookup"><span data-stu-id="dac06-110">GUI applications</span></span>
2.  <span data-ttu-id="dac06-111">Консольные приложения</span><span class="sxs-lookup"><span data-stu-id="dac06-111">Console applications</span></span>
3.  <span data-ttu-id="dac06-112">Службы Windows</span><span class="sxs-lookup"><span data-stu-id="dac06-112">Windows services</span></span>
4.  <span data-ttu-id="dac06-113">Проводник Windows</span><span class="sxs-lookup"><span data-stu-id="dac06-113">Windows explorer</span></span>

<span data-ttu-id="dac06-114">Диспетчер перезапуска закрывает приложение или службы только в том случае, если у вызывающего объекта есть разрешение на это.</span><span class="sxs-lookup"><span data-stu-id="dac06-114">Restart Manager shuts down application or services only if the caller has permission to do so.</span></span> <span data-ttu-id="dac06-115">Обратите внимание, что завершение работы между сеансами не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dac06-115">Note that shutdown across sessions is not supported.</span></span>

<span data-ttu-id="dac06-116">Приложения, использующие [установщик Windows](/windows/desktop/Msi/windows-installer-portal) версии 4,0 для установки и обслуживания, автоматически используют диспетчер перезапуска для уменьшения числа перезапусков системы.</span><span class="sxs-lookup"><span data-stu-id="dac06-116">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="dac06-117">Пользовательские установщики также могут вызывать API диспетчера перезапуска для завершения работы и перезапуска приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="dac06-117">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="dac06-118">В случаях, когда перезапуск системы недоступен, установщики могут использовать API диспетчера перезапуска, чтобы запланировать перезапуск таким образом, чтобы минимизировать перебои в работе потока пользователя.</span><span class="sxs-lookup"><span data-stu-id="dac06-118">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

<span data-ttu-id="dac06-119">Сведения об использовании API диспетчера перезапуска во время установки и обновления см. в разделе [Использование диспетчера перезапуска](using-restart-manager.md).</span><span class="sxs-lookup"><span data-stu-id="dac06-119">For information about using the Restart Manager API during installation and updates, see [Using Restart Manager](using-restart-manager.md).</span></span>

<span data-ttu-id="dac06-120">Критические системные службы не могут быть остановлены и перезапущены диспетчером перезапуска без перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="dac06-120">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="dac06-121">Дополнительные сведения об определении критических системных служб см. в разделе [критические системные службы](critical-system-services.md).</span><span class="sxs-lookup"><span data-stu-id="dac06-121">For more information about identifying critical system services, see [Critical System Services](critical-system-services.md).</span></span>

<span data-ttu-id="dac06-122">Приложения и службы должны быть готовы к завершению работы диспетчера перезапуска и сохранять данные пользователя и сведения о состоянии, необходимые для чистой перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="dac06-122">Your applications and services should be prepared to be shut down by the Restart Manager and save user data and state information that are needed for a clean restart.</span></span> <span data-ttu-id="dac06-123">Дополнительные сведения о подготовке приложений и служб для работы с диспетчером перезапуска см. в разделе [рекомендации для приложений и служб](guidelines-for-applications-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="dac06-123">For more information about how to prepare your applications and services to work with the Restart Manager, see [Guidelines for Applications and Services](guidelines-for-applications-and-services.md).</span></span>

<span data-ttu-id="dac06-124">Справочные сведения о перечислениях, структурах и функциях API диспетчера перезапуска см. в разделе [Справочник по диспетчеру перезапуска](restart-manager-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="dac06-124">For reference information about the enumerations, structures, and functions of the Restart Manager API, see the [Restart Manager Reference](restart-manager-reference.md) section</span></span>

 

 