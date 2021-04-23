---
description: Использование служебной программы Checkv4.exe для изменения приложения IPv4 для поддержки IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Использование служебной программы Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570806"
---
# <a name="using-the-checkv4exe-utility"></a><span data-ttu-id="865d5-103">Использование служебной программы Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="865d5-103">Using the Checkv4.exe utility</span></span>

> [!IMPORTANT]
> <span data-ttu-id="865d5-104">Служебная программа *Checkv4.exe* не поставляется в комплекте средств разработки программного обеспечения (SDK) для Windows 8, а также в более поздних версиях Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="865d5-104">The *Checkv4.exe* utility doesn't ship in the Windows Software Development Kit (SDK) for Windows 8, nor in later versions of the Windows SDK.</span></span>

<span data-ttu-id="865d5-105">Служебная программа *Checkv4.exe* предназначена для предоставления партнеру по переносу кода; Программа, которая посвящена вашей базе кода, выявляет потенциальные проблемы или выделяет код, который может выиграть от функций и структур, поддерживающих IPv6, и дает рекомендации.</span><span class="sxs-lookup"><span data-stu-id="865d5-105">The *Checkv4.exe* utility is designed to provide you with a code porting partner; a utility that steps through your code base with you, identifies potential problems or highlights code that could benefit from IPv6-capable functions or structures, and makes recommendations.</span></span> <span data-ttu-id="865d5-106">С помощью служебной программы Checkv4.exe задача изменения существующего приложения IPv4 для поддержки IPv6 становится намного проще.</span><span class="sxs-lookup"><span data-stu-id="865d5-106">With the Checkv4.exe utility, the task of modifying an existing IPv4 application to support IPv6 becomes much easier.</span></span>

<span data-ttu-id="865d5-107">Программа *Checkv4.exe* устанавливается как часть пакета средств разработки программного обеспечения Microsoft Windows (SDK), выпущенного для Windows Vista и более поздних пакетов SDK (до, но не включая пакет средств разработки программного обеспечения Windows (SDK) для Windows 8).</span><span class="sxs-lookup"><span data-stu-id="865d5-107">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later SDKs (up to, but not including, the Windows Software Development Kit (SDK) for Windows 8).</span></span>

<span data-ttu-id="865d5-108">Более ранняя версия служебной программы *Checkv4.exe* с более ограниченными функциями была также выпущена в рамках предыдущей предварительной версии технологии IPv6 Microsoft для Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="865d5-108">An earlier version of the *Checkv4.exe* utility with more limited features was also made available as part of the earlier Microsoft IPv6 Technology Preview for Windows 2000.</span></span>

<span data-ttu-id="865d5-109">В следующих разделах описывается использование служебной программы *Checkv4.exe* , а затем объясняется рекомендуемый подход к изменению существующего приложения IPv4 для поддержки IPv6.</span><span class="sxs-lookup"><span data-stu-id="865d5-109">The following sections describe how to use the *Checkv4.exe* utility, then explain the recommended approach for modifying an existing IPv4 application to support IPv6.</span></span>

## <a name="recommendations-for-running-checkv4exe"></a><span data-ttu-id="865d5-110">Рекомендации по выполнению Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="865d5-110">Recommendations for Running Checkv4.exe</span></span>

-   <span data-ttu-id="865d5-111">Программа *Checkv4.exe* проста.</span><span class="sxs-lookup"><span data-stu-id="865d5-111">The *Checkv4.exe* utility is straightforward.</span></span> <span data-ttu-id="865d5-112">Просто выполните *Checkv4.exe* в командной строке с именем файла, который требуется проверить в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="865d5-112">Simply execute *Checkv4.exe* at the command line with the name of the file you want to check as the parameter.</span></span> <span data-ttu-id="865d5-113">*Checkv4.exe* анализирует файл и предоставляет отзыв о том, где в этом файле существуют проблемы с IPv6-портами.</span><span class="sxs-lookup"><span data-stu-id="865d5-113">*Checkv4.exe* parses the file and provides feedback as to where IPv6 porting issues exist in that file.</span></span> <span data-ttu-id="865d5-114">Размещение *Checkv4.exe* в пути компьютера значительно упрощает запуск служебной программы *Checkv4.exe* из любого места в структуре каталога с исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="865d5-114">Placing the *Checkv4.exe* into your computer's path makes running the *Checkv4.exe* utility from anywhere in your source code directory structure much easier.</span></span> <span data-ttu-id="865d5-115">Например, размещение *Checkv4.exe* в% WINDIR% позволяет запускать *Checkv4.exe* из любого каталога на компьютере без включения пути.</span><span class="sxs-lookup"><span data-stu-id="865d5-115">For example, placing *Checkv4.exe* into %windir% enables you to launch *Checkv4.exe* from any directory on your computer without including its path.</span></span>

-   <span data-ttu-id="865d5-116">Выполните следующую команду в командной строке, чтобы проанализировать файл Симплек. c:</span><span class="sxs-lookup"><span data-stu-id="865d5-116">Issue the following command at the command prompt to parse the file Simplec.c:</span></span>

    <span data-ttu-id="865d5-117">**Checkv4 симплек. c**</span><span class="sxs-lookup"><span data-stu-id="865d5-117">**Checkv4 simplec.c**</span></span>

    <span data-ttu-id="865d5-118">Обратите внимание, что некоторые рекомендации, выполняемые служебной программой *Checkv4.exe* , должны иметь структуры, доступные только в последних версиях файла заголовков *Ws2tcpip. h* , например в структуре **SOCKADDR \_ IN6** .</span><span class="sxs-lookup"><span data-stu-id="865d5-118">Note that some of the recommendations made by the *Checkv4.exe* utility require structures available only in recent versions of the *Ws2tcpip.h* header file, such as the **SOCKADDR\_IN6** structure.</span></span> <span data-ttu-id="865d5-119">Эти файлы заголовков включены в Windows SDK, выпущенные для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="865d5-119">These header files are included in the Windows SDK released for Windows Vista and later.</span></span> <span data-ttu-id="865d5-120">Эти файлы заголовков также включены в пакет SDK для платформы более ранних версий, выпущенный для Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="865d5-120">These header files are also included in the earlier Platform Software Development Kit (SDK) released for Windows Server 2003.</span></span> <span data-ttu-id="865d5-121">Эти файлы заголовков также входят в состав подписки MSDN или по загрузке.</span><span class="sxs-lookup"><span data-stu-id="865d5-121">These header files are also included as part of an MSDN subscription or by download.</span></span>

    <span data-ttu-id="865d5-122">На следующем снимке экрана показаны результаты использования служебной программы *Checkv4.exe* в файле симплек. c, включенном в приложение а.</span><span class="sxs-lookup"><span data-stu-id="865d5-122">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simplec.c file included in Appendix A:</span></span>

    ![checkv4.exe сообщает о несовместимости IPv6 в файле симплек. c](images/portingguide002.jpg)

    <span data-ttu-id="865d5-124">На следующем снимке экрана показаны результаты использования служебной программы *Checkv4.exe* в файле Simple. c, который также включен в приложение а.</span><span class="sxs-lookup"><span data-stu-id="865d5-124">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simples.c file, which is also included in Appendix A:</span></span>

    ![checkv4.exe сообщает о несовместимости IPv6 в файле Simple. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a><span data-ttu-id="865d5-126">Процесс изменения приложения: с чего начать</span><span class="sxs-lookup"><span data-stu-id="865d5-126">The Application Modification Process: Where to Start</span></span>

<span data-ttu-id="865d5-127">Существует рекомендуемая процедура, связанная с добавлением возможностей IPv6 в приложения.</span><span class="sxs-lookup"><span data-stu-id="865d5-127">There is a recommended procedure associated with adding IPv6 capability to applications.</span></span> <span data-ttu-id="865d5-128">Эта последовательность является полезной, поскольку она позволяет разработчикам убедиться, что все шаги, необходимые для изменения существующего приложения IPv4 для поддержки IPv6, выполнены.</span><span class="sxs-lookup"><span data-stu-id="865d5-128">Following this sequence is beneficial, because it enables developers to ensure that all steps necessary to modify an existing IPv4 application to support IPv6 are taken.</span></span> <span data-ttu-id="865d5-129">Некоторые приложения могут потребовать более тщательного внимания к одной из этих последовательностей; Например, системная служба, скорее всего, будет иметь меньше проблем с интерфейсом пользователя, чем графическая программа для обмена файлами (FTP).</span><span class="sxs-lookup"><span data-stu-id="865d5-129">Certain applications may require more extensive attention to one of these sequences; for example, a system service would likely have less user interface issues than a graphical file transfer program (FTP).</span></span>

<span data-ttu-id="865d5-130">**Изменение приложений IPv4 для поддержки IPv6**</span><span class="sxs-lookup"><span data-stu-id="865d5-130">**To modify IPv4 applications to support IPv6**</span></span>

1.  <span data-ttu-id="865d5-131">Исправьте структуры и объявления, чтобы включить совместимость IPv6 и IPv4.</span><span class="sxs-lookup"><span data-stu-id="865d5-131">Fix structures and declarations to enable IPv6 and IPv4 compatibility.</span></span>
2.  <span data-ttu-id="865d5-132">Измените вызовы функций, чтобы воспользоваться преимуществами функций, поддерживающих протокол IPv6, таких как функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="865d5-132">Modify function calls to take advantage of IPv6-enabled functions, such as the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>
3.  <span data-ttu-id="865d5-133">Проверьте исходный код на использование жестко запрограммированных IPv4-адресов, таких как петлевой адрес, или использование других строковых литералов.</span><span class="sxs-lookup"><span data-stu-id="865d5-133">Review source code for the use of hard-coded IPv4 addresses such as the loopback address, or the use of other literal strings.</span></span>
4.  <span data-ttu-id="865d5-134">Тщательное изучение пользовательского интерфейса, включая информационные диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="865d5-134">Perform a thorough review of the user interface, including informational dialog boxes.</span></span> <span data-ttu-id="865d5-135">Подумали, подходит ли он для приложений с поддержкой IPv6 для указания или предоставления информации на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="865d5-135">Give thought to whether it is appropriate for IPv6-enabled applications to specify or provide IP-address based information.</span></span>
5.  <span data-ttu-id="865d5-136">Определите, полагается ли ваше приложение на базовые протоколы, такие как RPC, и внесите соответствующие программные изменения в обработку IPv6-адресов.</span><span class="sxs-lookup"><span data-stu-id="865d5-136">Determine whether your application relies on underlying protocols, such as RPC, and make appropriate programmatic changes to handle IPv6 addresses.</span></span>
6.  <span data-ttu-id="865d5-137">Используйте флаг времени компиляции IPV6STRICT при компиляции приложений в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="865d5-137">Use the compile-time flag IPV6STRICT when compiling applications on Windows XP and later.</span></span> <span data-ttu-id="865d5-138">Этот флаг приводит к невозможности компиляции несовместимого кода следующим образом:</span><span class="sxs-lookup"><span data-stu-id="865d5-138">This flag results in incompatible code failing to compile, as follows:</span></span>

    <span data-ttu-id="865d5-139">Приложения Windows Sockets 1. x с несовместимым кодом не компилируются и возвращают сообщение об ошибке «требуется WINSOCK2».</span><span class="sxs-lookup"><span data-stu-id="865d5-139">Windows Sockets 1.x applications with incompatible code fail to compile and return the error message "WINSOCK2 Required."</span></span>

    <span data-ttu-id="865d5-140">Приложения Windows Sockets 2. x с несовместимым кодом вызывают ошибку времени компиляции для каждого экземпляра несовместимого кода.</span><span class="sxs-lookup"><span data-stu-id="865d5-140">Windows Sockets 2.x applications with incompatible code cause a compile time error for each instance of incompatible code.</span></span> <span data-ttu-id="865d5-141">Сообщение об ошибке создается в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="865d5-141">An error message is generated in the following format:</span></span>

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    <span data-ttu-id="865d5-142">Пример:</span><span class="sxs-lookup"><span data-stu-id="865d5-142">For example:</span></span>

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



