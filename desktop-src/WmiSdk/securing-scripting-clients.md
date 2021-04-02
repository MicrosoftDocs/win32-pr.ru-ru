---
description: Сценарии и Visual Basic приложения должны устанавливать безопасность DCOM, особенно для удаленного доступа, а также могут включать права доступа.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Защита клиентов скриптов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263807"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="db54a-103">Защита клиентов скриптов</span><span class="sxs-lookup"><span data-stu-id="db54a-103">Securing Scripting Clients</span></span>

<span data-ttu-id="db54a-104">Сценарии и Visual Basic приложения должны устанавливать безопасность DCOM, особенно для удаленного доступа, а также могут включать права доступа.</span><span class="sxs-lookup"><span data-stu-id="db54a-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="db54a-105">Разрешения на доступ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="db54a-105">Default Access Permissions</span></span>

<span data-ttu-id="db54a-106">Доступ к инструментарию WMI на локальном и удаленном компьютерах отличается.</span><span class="sxs-lookup"><span data-stu-id="db54a-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="db54a-107">Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="db54a-108">Ниже перечислены разрешения на доступ по умолчанию для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="db54a-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="db54a-109">Все, LocalService, NetworkService</span><span class="sxs-lookup"><span data-stu-id="db54a-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="db54a-110">Разрешение на чтение или запись данных и выполнение [*методов поставщика*](gloss-p.md) на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="db54a-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="db54a-111">Эти учетные записи не могут создавать новые классы или устанавливать новые поставщики.</span><span class="sxs-lookup"><span data-stu-id="db54a-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="db54a-112">Учетные записи администратора</span><span class="sxs-lookup"><span data-stu-id="db54a-112">Administrator accounts</span></span>

    <span data-ttu-id="db54a-113">Полный контроль на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="db54a-113">Full control on local computer.</span></span> <span data-ttu-id="db54a-114">При подключении к удаленному компьютеру учетная запись должна также иметь права локального администратора на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="db54a-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="db54a-115">Защита клиента скриптов</span><span class="sxs-lookup"><span data-stu-id="db54a-115">Securing a Scripting Client</span></span>

<span data-ttu-id="db54a-116">Приложения для работы со скриптами и Visual Basicом WMI должны правильно задавать уровни безопасности DCOM для операционных систем, на которых они нацелены.</span><span class="sxs-lookup"><span data-stu-id="db54a-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="db54a-117">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="db54a-118">При подключении к удаленному компьютеру может потребоваться изменить службу (NTLM или Kerberos), которая обрабатывает проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="db54a-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="db54a-119">Дополнительные сведения см. [в разделе Настройка службы проверки подлинности с помощью VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="db54a-120">Для доступа к некоторым классам или данным WMI может потребоваться привилегия, которая не включена.</span><span class="sxs-lookup"><span data-stu-id="db54a-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="db54a-121">Например, необходимо включить привилегию безопасности при подключении к классу [**Win32 \_ нтевентлогфиле**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="db54a-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="db54a-122">Дополнительные сведения см. в статье [выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="db54a-123">При доступе к WMI из Active Server страницы (ASP) требуется настройка некоторых служб IIS.</span><span class="sxs-lookup"><span data-stu-id="db54a-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="db54a-124">Дополнительные сведения см. в разделе [Настройка IIS 5,0 и более поздних версий для сценариев ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="db54a-125">Возможно, вы пытаетесь подключиться к пространству имен, для которого требуется зашифрованное соединение, иными словами, для которого требуется уровень проверки подлинности Пктприваци.</span><span class="sxs-lookup"><span data-stu-id="db54a-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="db54a-126">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="db54a-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
