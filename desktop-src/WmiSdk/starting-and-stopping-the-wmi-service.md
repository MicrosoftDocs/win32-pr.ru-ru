---
description: Инструментарий WMI запускается как служба с отображаемым именем &\# 0034; Инструментарий управления Windows (WMI)&\# 0034; и имя службы &\# 0034; winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Запуск и остановка службы WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263804"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="ed9a9-103">Запуск и остановка службы WMI</span><span class="sxs-lookup"><span data-stu-id="ed9a9-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="ed9a9-104">Инструментарий WMI запускается как служба с отображаемым именем "инструментарий управления Windows (WMI)" и именем службы "Winmgmt".</span><span class="sxs-lookup"><span data-stu-id="ed9a9-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="ed9a9-105">Инструментарий WMI запускается автоматически при запуске системы под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="ed9a9-106">Если инструментарий WMI не запущен, он автоматически запускается, когда первое приложение или сценарий управления запрашивают соединение с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="ed9a9-107">Некоторые другие службы зависят от службы WMI в зависимости от версии операционной системы, в которой работает система.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="ed9a9-108">Запуск службы WinMgmt</span><span class="sxs-lookup"><span data-stu-id="ed9a9-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="ed9a9-109">В следующей процедуре описывается запуск службы WMI.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="ed9a9-110">**Запуск службы WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="ed9a9-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="ed9a9-111">В командной строке введите **net** **Start** **Winmgmt** \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="ed9a9-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="ed9a9-112">Дополнительные сведения о доступных параметрах см. в разделе [Winmgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="ed9a9-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="ed9a9-113">Для запуска службы WMI используется встроенная учетная запись администратора или учетная запись в группе "Администраторы", которая работает с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="ed9a9-114">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ed9a9-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="ed9a9-115">Другие службы, зависящие от службы WMI, такие как узел агента SMS или брандмауэр Windows, не будут перезапущены автоматически.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="ed9a9-116">Остановка службы WinMgmt</span><span class="sxs-lookup"><span data-stu-id="ed9a9-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="ed9a9-117">В следующей процедуре описывается, как прерывать работу службы WMI.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="ed9a9-118">**Завершение службы WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="ed9a9-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="ed9a9-119">В командной строке введите команду **net останавливаться Winmgmt**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="ed9a9-120">Также останавливается работа других служб, зависящих от службы WMI, таких как узел агента SMS или брандмауэр Windows.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="ed9a9-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed9a9-121">Examples</span></span>

<span data-ttu-id="ed9a9-122">Коллекция TechNet содержит [сценарий наблюдения службы WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), в котором описывается программное завершение работы и перезапуск службы Winmgmt с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed9a9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ed9a9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed9a9-124">Использование средств Command-Line инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="ed9a9-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



