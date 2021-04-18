---
description: Инструментарий WMI запускается как часть общего узла службы с портами, назначенными по протоколу DCOM по умолчанию. Однако службу WMI можно настроить для запуска в качестве единственного процесса на отдельном узле и указать фиксированный порт.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Настройка фиксированного порта для WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712941"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="94406-104">Настройка фиксированного порта для WMI</span><span class="sxs-lookup"><span data-stu-id="94406-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="94406-105">Инструментарий WMI запускается как часть общего узла службы с портами, назначенными по протоколу DCOM по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94406-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="94406-106">Однако службу WMI можно настроить для запуска в качестве единственного процесса на отдельном узле и указать фиксированный порт.</span><span class="sxs-lookup"><span data-stu-id="94406-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="94406-107">Следующая процедура представляет собой автоматическую установку, позволяющую инструментарию WMI иметь фиксированный порт.</span><span class="sxs-lookup"><span data-stu-id="94406-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="94406-108">Процедура использует программу командной строки [**Winmgmt**](winmgmt.md) .</span><span class="sxs-lookup"><span data-stu-id="94406-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="94406-109">**Настройка фиксированного порта для WMI**</span><span class="sxs-lookup"><span data-stu-id="94406-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="94406-110">В командной строке введите команду **Winmgmt-стандалонехост** .</span><span class="sxs-lookup"><span data-stu-id="94406-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="94406-111">Чтобы отключить службу WMI, введите команду **net останавливают "Инструментарий управления Windows (WMI)"** или используйте короткое имя команды **net останавливаться Winmgmt** .</span><span class="sxs-lookup"><span data-stu-id="94406-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="94406-112">Снова запустите службу WMI на новом узле службы, введя **net start "Инструментарий управления Windows (WMI)"** или **net start Winmgmt** .</span><span class="sxs-lookup"><span data-stu-id="94406-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="94406-113">Установите новый номер порта для службы WMI, введя **команду netsh firewall Add открытие портов TCP 24158 вмификседпорт**</span><span class="sxs-lookup"><span data-stu-id="94406-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="94406-114">Чтобы отменить любые изменения, внесенные в WMI, введите команду **Winmgmt/шаредхост**, а затем закройте и снова запустите службу Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="94406-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="94406-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="94406-115">Examples</span></span>

<span data-ttu-id="94406-116">Сценарий, который настраивает фиксированный порт для WMI, см. в следующем [примере кода](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )коллекции скриптов.</span><span class="sxs-lookup"><span data-stu-id="94406-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="94406-117">или пример кода PowerShell, который включает или отключает параметры порта WMI, см. пример [Set-вмисинглепорт](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) в коллекции TechNet.</span><span class="sxs-lookup"><span data-stu-id="94406-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94406-118">См. также</span><span class="sxs-lookup"><span data-stu-id="94406-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94406-119">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="94406-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="94406-120">Устранение неполадок удаленных подключений WMI</span><span class="sxs-lookup"><span data-stu-id="94406-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="94406-121">Размещение и безопасность поставщика</span><span class="sxs-lookup"><span data-stu-id="94406-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



