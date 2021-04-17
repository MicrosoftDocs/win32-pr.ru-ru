---
description: Любой язык сценариев, например VBScript, который работает с объектами ActiveX, может получать доступ к данным WMI. Приложения могут получать доступ к WMI в C++, используя API COM для WMI или в Visual Basic, используя библиотеку типов Wbemdisp. tlb и API скриптов для WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Создание приложения или скрипта WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703003"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="c84c9-105">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="c84c9-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="c84c9-106">Любой язык сценариев, например VBScript, который работает с объектами ActiveX, может получать доступ к данным WMI.</span><span class="sxs-lookup"><span data-stu-id="c84c9-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="c84c9-107">Приложения могут получать доступ к WMI в C++, используя [API COM для WMI](com-api-for-wmi.md) или в Visual Basic, используя [библиотеку типов](using-the-wmi-scripting-type-library.md) WBEMDISP. tlb и [API скриптов для WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c84c9-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="c84c9-108">.</span><span class="sxs-lookup"><span data-stu-id="c84c9-108">.</span></span> <span data-ttu-id="c84c9-109">Получить данные можно с помощью инструментария WMI, написав сценарий, Active Serverную страницу (ASP) или HTML-приложение (HTA).</span><span class="sxs-lookup"><span data-stu-id="c84c9-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="c84c9-110">Можно также использовать Windows PowerShell для получения данных или написания скриптов.</span><span class="sxs-lookup"><span data-stu-id="c84c9-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="c84c9-111">Дополнительные сведения см. в статьях [Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) и [Начало работы с помощью Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="c84c9-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="c84c9-112">TechNet Скриптцентер at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) содержит сотни примеров сценариев.</span><span class="sxs-lookup"><span data-stu-id="c84c9-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="c84c9-113">Дополнительные сведения о печати и сетевых ресурсах см. в разделе [Дополнительные сведения](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="c84c9-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="c84c9-114">Следующая процедура описывает подключение к службе WMI и хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="c84c9-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="c84c9-115">**Подключение к службе WMI и хранилищу данных**</span><span class="sxs-lookup"><span data-stu-id="c84c9-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="c84c9-116">Нахождение службы WMI на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c84c9-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="c84c9-117">Подключитесь к одному или нескольким пространствам имен WMI.</span><span class="sxs-lookup"><span data-stu-id="c84c9-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="c84c9-118">Эти операции отличаются в C++, Visual Basic, платформа .NET Framework языках или при использовании скрипта.</span><span class="sxs-lookup"><span data-stu-id="c84c9-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="c84c9-119">Скрипты и Visual Basic приложения должны обращаться к классам, экземпляры которых предоставляются данными существующих поставщиков.</span><span class="sxs-lookup"><span data-stu-id="c84c9-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="c84c9-120">Но приложения, написанные на C++, могут сделать больше.</span><span class="sxs-lookup"><span data-stu-id="c84c9-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="c84c9-121">Например, приложение, написанное на языке C++, может отправлять события, но сценарий WMI может подписываться только на получение событий.</span><span class="sxs-lookup"><span data-stu-id="c84c9-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="c84c9-122">Поставщик WMI может быть написан только на C++ или с помощью платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c84c9-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="c84c9-123">Дополнительные сведения о создании приложений на C# или Visual Basic .NET см. в разделе [Общие сведения об инструментарии WMI .NET](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="c84c9-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="c84c9-124">Дополнительные сведения о создании приложений и скриптов для WMI см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c84c9-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="c84c9-125">Создание приложения WMI с помощью C++</span><span class="sxs-lookup"><span data-stu-id="c84c9-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="c84c9-126">Создание скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="c84c9-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="c84c9-127">Создание управляемого клиента WMI</span><span class="sxs-lookup"><span data-stu-id="c84c9-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="c84c9-128">Для выполнения большинства задач используйте предустановленные [классы WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c84c9-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c84c9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c84c9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c84c9-130">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="c84c9-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
