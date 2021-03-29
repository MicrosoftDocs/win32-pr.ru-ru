---
description: Во время загрузки системы SCM запускает все службы автозапуска и службы, от которых они зависят. Например, если автоматический запуск службы зависит от службы, запускаемой по требованию, то служба запуска по требованию также запускается автоматически.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Автоматический запуск служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662255"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="98c04-104">Автоматический запуск служб</span><span class="sxs-lookup"><span data-stu-id="98c04-104">Automatically Starting Services</span></span>

<span data-ttu-id="98c04-105">Во время загрузки системы SCM запускает все службы автозапуска и службы, от которых они зависят.</span><span class="sxs-lookup"><span data-stu-id="98c04-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="98c04-106">Например, если автоматический запуск службы зависит от службы, запускаемой по требованию, то служба запуска по требованию также запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="98c04-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="98c04-107">Порядок загрузки определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="98c04-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="98c04-108">Порядок групп в списке группы упорядочения нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98c04-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="98c04-109">Эти сведения хранятся в значении **ServiceGroupOrder** в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="98c04-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="98c04-110">**\_ \_ \\ \\ Элемент управления CurrentControlSet системы hKey локального компьютера \\**</span><span class="sxs-lookup"><span data-stu-id="98c04-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="98c04-111">Чтобы указать группу порядка загрузки для службы, используйте параметр *лплоадордерграуп* функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) или [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="98c04-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="98c04-112">Порядок служб в группе, указанной в векторе порядка тегов.</span><span class="sxs-lookup"><span data-stu-id="98c04-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="98c04-113">Эти сведения хранятся в значении **граупордерлист** в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="98c04-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="98c04-114">**\_ \_ \\ \\ Элемент управления CurrentControlSet системы hKey локального компьютера \\**</span><span class="sxs-lookup"><span data-stu-id="98c04-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="98c04-115">Зависимости, перечисленные для каждой службы.</span><span class="sxs-lookup"><span data-stu-id="98c04-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="98c04-116">После завершения загрузки система выполняет программу проверки загрузки, указанную параметром **бутверификатионпрограм** в следующем разделе реестра: **hKey \_ локальный \_ компьютер \\ System \\ CurrentControlSet \\ Control**.</span><span class="sxs-lookup"><span data-stu-id="98c04-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="98c04-117">По умолчанию это значение не установлено.</span><span class="sxs-lookup"><span data-stu-id="98c04-117">By default, this value is not set.</span></span> <span data-ttu-id="98c04-118">Система просто сообщает о том, что загрузка прошла успешно после входа первого пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="98c04-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="98c04-119">Вы можете указать программу проверки загрузки, которая проверяет систему на наличие проблем и передает состояние загрузки SCM с помощью функции [**нотифибутконфигстатус**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="98c04-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="98c04-120">После успешной загрузки система сохраняет клон базы данных в последней известной конфигурации (LKG).</span><span class="sxs-lookup"><span data-stu-id="98c04-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="98c04-121">Система может восстановить эту копию базы данных, если изменения, внесенные в активную базу данных, приведут к сбою перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="98c04-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="98c04-122">Ниже приведен раздел реестра для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="98c04-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="98c04-123">**\_Службы hKey локального \_ компьютера, \\ система \\ управления версиями *xxx* \\**</span><span class="sxs-lookup"><span data-stu-id="98c04-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="98c04-124">где *xxx* — значение, сохраненное в следующем параметре реестра: **hKey \_ Local \_ Machine \\ System \\ выберите \\ ласткновнгуд**.</span><span class="sxs-lookup"><span data-stu-id="98c04-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="98c04-125">Если не удается запустить автоматический запуск службы с \_ \_ критическим уровнем контроля ошибок службы, SCM перезагружает компьютер с помощью конфигурации LKG.</span><span class="sxs-lookup"><span data-stu-id="98c04-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="98c04-126">Если конфигурация LKG уже используется, происходит сбой загрузки.</span><span class="sxs-lookup"><span data-stu-id="98c04-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="98c04-127">Службу автоматического запуска можно настроить в качестве отложенного автоматического запуска, вызвав функцию [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) с \_ \_ отложенным \_ \_ автозапуском конфигурации службы \_ .</span><span class="sxs-lookup"><span data-stu-id="98c04-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="98c04-128">Это изменение вступает в силу после следующей загрузки системы.</span><span class="sxs-lookup"><span data-stu-id="98c04-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="98c04-129">Дополнительные сведения см. в разделе [**Служба \_ отложенного \_ автоматического \_ запуска \_ службы**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="98c04-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



