---
description: В этом руководством содержатся сведения, необходимые для того, чтобы приложение Microsoft Windows использовало новое поколение протокола IP версии 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Рекомендации по IPv6 для приложений Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145031"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="75f07-103">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="75f07-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="75f07-104">В этом руководством содержатся сведения, необходимые для того, чтобы приложение Microsoft Windows использовало новое поколение протокола IP версии 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="75f07-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="75f07-105">Добавление возможности IPv6 в приложение не обязательно является процессом переноса.</span><span class="sxs-lookup"><span data-stu-id="75f07-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="75f07-106">Чтобы перенести приложение, мы предлагаем изменить код для работы на другой платформе, что подразумевает использование предыдущей платформы.</span><span class="sxs-lookup"><span data-stu-id="75f07-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="75f07-107">Это краткое справочное по предназначено для упрощения добавления возможностей протокола IPv6 в приложение с сохранением функциональных возможностей IPv4.</span><span class="sxs-lookup"><span data-stu-id="75f07-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="75f07-108">В этом руководством обсуждаются проблемы, связанные с добавлением функций IPv6, а затем нацелены на области разработки, которые наиболее подвержены переходу.</span><span class="sxs-lookup"><span data-stu-id="75f07-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="75f07-109">Каждая область получает подробное объяснение ошибок, которые следует отслеживать, стратегии, предлагаемые для их устранения, и советы по обеспечению оптимального использования новых программных элементов [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (функций и структур).</span><span class="sxs-lookup"><span data-stu-id="75f07-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="75f07-110">Дополнительные сведения об IPv6 см. в разделе [Поддержка IPv6](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="75f07-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="75f07-111">В этом руководство также приводятся примеры кода, позволяющие получить практические навыки и визуальные представления о проблемах, которые могут возникнуть при изменении приложений.</span><span class="sxs-lookup"><span data-stu-id="75f07-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="75f07-112">Примеры взяты из полного набора рабочих примеров простого приложения Windows Sockets, которое было изменено для поддержки IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="75f07-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="75f07-113">Исходный код для этих рабочих примеров целиком включен в два приложения в конце этого документа: [приложение а. исходный код](appendix-a-ipv4-only-source-code-2.md) , предназначенный только для IPv4, содержит исходный код приложения до его изменения для поддержки IPv6; [Приложение б. Независимый от IP-версии исходный код](appendix-b-ip-version-agnostic-source-code-2.md) предоставляет исходный код после включения приложения с поддержкой IPv6.</span><span class="sxs-lookup"><span data-stu-id="75f07-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="75f07-114">Корпорация Майкрософт предоставляет служебную программу с именем Checkv4.exe, которая помогает найти в коде приложения потенциально переносимый код, а также рекомендации по исправлениям.</span><span class="sxs-lookup"><span data-stu-id="75f07-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="75f07-115">В этом документе показана служебная программа Checkv4.exe, использующая пример приложения в приложениях, а также снимки экрана, отображающие выходные данные, которые создает служебная программа Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="75f07-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="75f07-116">Дополнительные сведения см. [в разделе Использование служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="75f07-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="75f07-117">В этом руководство рассматриваются следующие вопросы программирования:</span><span class="sxs-lookup"><span data-stu-id="75f07-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="75f07-118">Изменение структур данных для IPv6 Winsock Аппикатионс</span><span class="sxs-lookup"><span data-stu-id="75f07-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="75f07-119">Вызовы функций для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="75f07-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="75f07-120">Использование жестко закодированных IPv4-адресов</span><span class="sxs-lookup"><span data-stu-id="75f07-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="75f07-121">Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="75f07-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="75f07-122">Базовые протоколы для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="75f07-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="75f07-123">Сокеты с двумя стеками для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="75f07-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="75f07-124">Поскольку не существует унифицированной последовательности событий, разделы, которые устраняют проблемы, связанные с IPv6, не упорядочиваются последовательно, поэтому вы можете ссылаться на любой раздел в любое время.</span><span class="sxs-lookup"><span data-stu-id="75f07-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="75f07-125">Настоятельно рекомендуется проанализировать каждый раздел при добавлении возможности IPv6 в приложение.</span><span class="sxs-lookup"><span data-stu-id="75f07-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="75f07-126">Также рекомендуется ознакомиться со служебной программой Checkv4.exe, так как она включает советы по порядку устранения неполадок, связанных с IPv6.</span><span class="sxs-lookup"><span data-stu-id="75f07-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="75f07-127">Чтобы ознакомиться с программой Checkv4.exe и просмотреть порядок, в котором следует подходить процесс переноса в приложениях, см. раздел [Использование служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="75f07-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="75f07-128">В этом разделе содержатся сведения о флаге времени компиляции, который строго проверяет элементы программирования, несовместимые с IPv6.</span><span class="sxs-lookup"><span data-stu-id="75f07-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="75f07-129">Чтобы перейти непосредственно к примеру приложения, см. [приложение а. исходный код только для IPv4](appendix-a-ipv4-only-source-code-2.md) и [приложение б: независимый от IP-версии исходный код](appendix-b-ip-version-agnostic-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="75f07-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75f07-130">См. также</span><span class="sxs-lookup"><span data-stu-id="75f07-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f07-131">Протокол IP версии 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="75f07-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="75f07-132">Поддержка IPv6</span><span class="sxs-lookup"><span data-stu-id="75f07-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="75f07-133">Предварительный просмотр технологии IPv6 для Windows 2000</span><span class="sxs-lookup"><span data-stu-id="75f07-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="75f07-134">Использование служебной программы Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="75f07-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="75f07-135">Приложение а. исходный код только для IPv4</span><span class="sxs-lookup"><span data-stu-id="75f07-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="75f07-136">Приложение б. Независимый от IP-версии исходный код</span><span class="sxs-lookup"><span data-stu-id="75f07-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



