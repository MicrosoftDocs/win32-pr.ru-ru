---
description: Internet Explorer 8 — Защита выполнения данных/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8 — Защита выполнения данных/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088252"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="9da50-103">Internet Explorer 8 — Защита выполнения данных/NX</span><span class="sxs-lookup"><span data-stu-id="9da50-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="9da50-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="9da50-104">Affected Platforms</span></span>

 <span data-ttu-id="9da50-105">**Клиенты** — Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="9da50-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="9da50-106">**Серверы** — windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9da50-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="9da50-107">Internet Explorer 8 включит защиту DEP/NX при запуске в операционной системе с последним пакетом обновления.</span><span class="sxs-lookup"><span data-stu-id="9da50-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="9da50-108">В Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 и Windows Server 2008 по умолчанию DEP/NX включено в Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="9da50-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="9da50-109">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="9da50-109">Feature Impact</span></span>

<span data-ttu-id="9da50-110">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="9da50-110">**Severity** - Medium</span></span>  
<span data-ttu-id="9da50-111">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="9da50-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="9da50-112">Как правило, любое приложение, работающее в Internet Explorer и несовместимое с DEP/NX, приведет к сбою при запуске и не будет работать.</span><span class="sxs-lookup"><span data-stu-id="9da50-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="9da50-113">Internet Explorer может аварийно завершить работу при запуске, если установлены надстройки, несовместимые с DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="9da50-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="9da50-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9da50-114">Description</span></span>

<span data-ttu-id="9da50-115">DEP/NX — это функция безопасности, которая помогает устранить уязвимости, связанные с памятью.</span><span class="sxs-lookup"><span data-stu-id="9da50-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="9da50-116">Начиная с Internet Explorer 8, все процессы Internet Explorer по умолчанию включают функцию DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="9da50-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="9da50-117">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="9da50-117">Manifestation of Impact</span></span>

<span data-ttu-id="9da50-118">Ядро Windows отслеживает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="9da50-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="9da50-119">Если ядро обнаруживает попытку выполнить код на странице памяти, которая не помечена как исполняемый объект, ядро прерывает выполнение программы, что приводит к сбою.</span><span class="sxs-lookup"><span data-stu-id="9da50-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="9da50-120">Это мера безопасности, позволяющая гарантировать, что уязвимости, связанные с памятью (например, переполнения буфера) в приложении, нельзя использовать для выполнения произвольного кода.</span><span class="sxs-lookup"><span data-stu-id="9da50-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="9da50-121">Устранение End-User</span><span class="sxs-lookup"><span data-stu-id="9da50-121">End-User Mitigation</span></span>

-   <span data-ttu-id="9da50-122">Установите более позднюю версию надстройки или платформы, совместимую с DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="9da50-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="9da50-123">Запустите Internet Explorer с правами администратора, а затем отключите DEP/NX с помощью флажка **включить защиту памяти для предотвращения атак** из Интернета на вкладке **Свойства обозревателя**  /  **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="9da50-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="9da50-124">Решение для разработчиков</span><span class="sxs-lookup"><span data-stu-id="9da50-124">Developer Solution</span></span>

<span data-ttu-id="9da50-125">Скомпилируйте приложения с помощью последних версий платформ, совместимых с DEP.</span><span class="sxs-lookup"><span data-stu-id="9da50-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="9da50-126">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="9da50-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="9da50-127">Использование параметра компоновщика/NXCOMPAT для указания совместимости DEP/NX</span><span class="sxs-lookup"><span data-stu-id="9da50-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="9da50-128">Применяйте свой код к другим доступным средствам защиты, таким как защита стека (/GS), защищенная обработка исключений (/SafeSEH) и ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="9da50-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="9da50-129">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="9da50-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="9da50-130">Протестируйте код с включенной функцией DEP/NX с помощью последней выпущенной версии Internet Explorer в Windows Vista SP1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9da50-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="9da50-131">Протестируйте Internet Explorer 7 в Windows Vista после включения параметра DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="9da50-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="9da50-132">Чтобы включить DEP/NX для Internet Explorer 7, запустите Internet Explorer от имени администратора, а затем установите соответствующий флажок в меню Сервис > свойства обозревателя > вкладка Дополнительно.</span><span class="sxs-lookup"><span data-stu-id="9da50-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="9da50-133">Запустите средство тестирования совместимости Internet Explorer (ИЕКТТ), входящее в состав набора средств для обеспечения совместимости приложений (ACT), для выявления потенциальных проблем, связанных с изменениями DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="9da50-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="9da50-134">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="9da50-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="9da50-135">Internet Explorer 8 Security, часть I: защита памяти DEP/NX</span><span class="sxs-lookup"><span data-stu-id="9da50-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="9da50-136">Предотвращение выполнения данных</span><span class="sxs-lookup"><span data-stu-id="9da50-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="9da50-137">Новые API-интерфейсы NX, добавленные в Windows Vista SP1, Windows XP SP3 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9da50-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="9da50-138">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="9da50-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="9da50-139">[Известные проблемы с функциями безопасности в Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9da50-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
