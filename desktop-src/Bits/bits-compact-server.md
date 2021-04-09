---
title: Облегченный сервер BITS
description: Фоновая интеллектуальная служба передачи (BITS) Compact Server — это изолированный файловый сервер HTTP/HTTPS, который обеспечивает возможность асинхронной передачи ограниченного числа больших файлов между компьютерами.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890876"
---
# <a name="bits-compact-server"></a><span data-ttu-id="4b76b-103">Облегченный сервер BITS</span><span class="sxs-lookup"><span data-stu-id="4b76b-103">BITS Compact Server</span></span>

<span data-ttu-id="4b76b-104">Фоновая интеллектуальная служба передачи (BITS) Compact Server — это изолированный файловый сервер HTTP/HTTPS, который обеспечивает возможность асинхронной передачи ограниченного числа больших файлов между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="4b76b-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="4b76b-105">Сервер Compact Server создается как служба NT и использует HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="4b76b-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="4b76b-106">Облегченный сервер BITS предназначен для использования корпоративными и малыми предприятиями в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="4b76b-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="4b76b-107">Ожидаемое использование составляет не более 25 групп URL-адресов, а каждая группа URL-адресов поддерживает 3 одновременных передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="4b76b-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="4b76b-108">Передача файлов выполняется между компьютерами в одном домене или в взаимодоверенных доменах.</span><span class="sxs-lookup"><span data-stu-id="4b76b-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="4b76b-109">Передача файлов не предназначена для клиентов с выходом в Интернет.</span><span class="sxs-lookup"><span data-stu-id="4b76b-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="4b76b-110">Установка облегченного сервера BITS</span><span class="sxs-lookup"><span data-stu-id="4b76b-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="4b76b-111">Облегченный сервер BITS является необязательным компонентом сервера.</span><span class="sxs-lookup"><span data-stu-id="4b76b-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="4b76b-112">Для установки облегченного сервера BITS можно использовать один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="4b76b-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="4b76b-113">Диспетчер серверов</span><span class="sxs-lookup"><span data-stu-id="4b76b-113">Server Manager</span></span>

-   <span data-ttu-id="4b76b-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b76b-114">Windows PowerShell</span></span>

-   <span data-ttu-id="4b76b-115">Диспетчер пакетов</span><span class="sxs-lookup"><span data-stu-id="4b76b-115">Package Manager</span></span>

<span data-ttu-id="4b76b-116">**Установка облегченного сервера BITS с помощью диспетчер сервера**</span><span class="sxs-lookup"><span data-stu-id="4b76b-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="4b76b-117">В разделе **Сводка компонентов** **Диспетчер сервера** щелкните **Добавить компоненты**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="4b76b-118">В мастере добавления компонентов выберите **Фоновая интеллектуальная служба передачи (BITS)** и **Compact Server**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="4b76b-119">Следуйте инструкциям мастера, включая установку необходимого программного обеспечения, если указано.</span><span class="sxs-lookup"><span data-stu-id="4b76b-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="4b76b-120">Дополнительные сведения см. в **Диспетчер сервера** справке в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4b76b-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="4b76b-121">**Установка облегченного сервера BITS с помощью Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="4b76b-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="4b76b-122">В командной строке Windows PowerShell введите следующую команду: **Import-Module ServerManager**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="4b76b-123">Затем нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="4b76b-123">Then press Enter.</span></span>
2.  <span data-ttu-id="4b76b-124">Введите следующую команду: **Add-WINDOWSFEATURE BITS-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="4b76b-125">Затем нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="4b76b-125">Then press Enter.</span></span>

<span data-ttu-id="4b76b-126">В следующем примере на основе текста демонстрируется установка Compact Server BITS с помощью командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4b76b-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="4b76b-127">Сведения об использовании командлетов см. в документации [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b76b-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="4b76b-128">Дополнительные сведения о командлете Import-Module см. в разделе [Import-Module](/previous-versions//dd347701(v=technet.10)) в библиотеке Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="4b76b-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="4b76b-129">Для получения справки в командной строке введите **Get-Help Import-Module**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="4b76b-130">Дополнительные сведения о командлете Add-WindowsFeature см. в разделе [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) в библиотеке Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="4b76b-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="4b76b-131">Для получения справки в командной строке введите **Get-Help Add-WindowsFeature**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="4b76b-132">**Установка облегченного сервера BITS с помощью диспетчера пакетов**</span><span class="sxs-lookup"><span data-stu-id="4b76b-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="4b76b-133">Введите следующую команду: **PkgMgr.exe/IU: LightweightServer**.</span><span class="sxs-lookup"><span data-stu-id="4b76b-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="4b76b-134">Параметры теряются при перезапуске службы Compact Server или при перезагрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b76b-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="4b76b-135">Удаленное управление облегченным сервером BITS</span><span class="sxs-lookup"><span data-stu-id="4b76b-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="4b76b-136">Облегченный сервер BITS с удаленным управлением BITS обеспечивает более безопасную передачу удаленных файлов.</span><span class="sxs-lookup"><span data-stu-id="4b76b-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="4b76b-137">Удаленное управление BITS использует поставщик инструментарий управления Windows (WMI) (WMI), который позволяет системному администратору или приложению контроллера удаленно создавать задания передачи BITS на клиентах и публиковать файлы для размещения на облегченном сервере BITS.</span><span class="sxs-lookup"><span data-stu-id="4b76b-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="4b76b-138">Поставщик BITS также можно использовать, чтобы позволить приложению удаленно использовать клиент BITS в сочетании с облегченным сервером BITS для передачи файлов с одного удаленного компьютера на другой удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="4b76b-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="4b76b-139">Дополнительные сведения см. в документации [поставщика BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="4b76b-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b76b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4b76b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b76b-141">Поставщик BITS</span><span class="sxs-lookup"><span data-stu-id="4b76b-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 