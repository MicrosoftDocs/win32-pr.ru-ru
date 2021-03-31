---
description: Неотъемлемой частью тестирования и отладки реализаций обработчика протоколов является понимание того, как запускаются обработчики протоколов.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Обработчики протокола отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144050"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="df94b-103">Обработчики протокола отладки</span><span class="sxs-lookup"><span data-stu-id="df94b-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="df94b-104">Неотъемлемой частью тестирования и отладки реализаций обработчика протоколов является понимание того, как запускаются обработчики протоколов.</span><span class="sxs-lookup"><span data-stu-id="df94b-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="df94b-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="df94b-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="df94b-106">Сведения о обработчиках протокола отладки</span><span class="sxs-lookup"><span data-stu-id="df94b-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="df94b-107">Настройка отладки</span><span class="sxs-lookup"><span data-stu-id="df94b-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="df94b-108">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df94b-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="df94b-109">См. также</span><span class="sxs-lookup"><span data-stu-id="df94b-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="df94b-110">Сведения о обработчиках протокола отладки</span><span class="sxs-lookup"><span data-stu-id="df94b-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="df94b-111">Процесс Сеарчиндексер (searchindexer.exe) запускает одну копию процесса Сеарчпротоколхост (SearchProtocolHost.exe) в контексте системы и другую копию в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="df94b-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="df94b-112">Затем обработчики протокола загружаются в процесс Сеарчпротоколхост по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="df94b-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="df94b-113">Они не выгружаются до тех пор, пока служба поиска не будет остановлена.</span><span class="sxs-lookup"><span data-stu-id="df94b-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="df94b-114">Один и тот же экземпляр обработчика протокола используется повторно в любое количество раз во время работы службы.</span><span class="sxs-lookup"><span data-stu-id="df94b-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="df94b-115">Процессы Сеарчиндексер и Сеарчпротоколхост часто взаимодействуют во время индексирования.</span><span class="sxs-lookup"><span data-stu-id="df94b-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="df94b-116">Если вы приостанавливаете или останавливаете процесс Сеарчпротоколхост для отладки, Сеарчиндексер запустит новый процесс Сеарчпротоколхост и сделает сеанс отладки недействительным.</span><span class="sxs-lookup"><span data-stu-id="df94b-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="df94b-117">Кроме того, при присоединении отладчика непосредственно к процессу Сеарчпротоколхост можно приостановить наследование маркеров от searchindexer.exe до searchprotocolhost.exe, и два процесса не смогут взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="df94b-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="df94b-118">Чтобы избежать этих проблем, необходимо уведомить службу поиска, которая отлаживается, и необходимо присоединить отладчик к процессу Сеарчиндексер с инструкциями по отладке дочерних процессов, как описано далее.</span><span class="sxs-lookup"><span data-stu-id="df94b-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="df94b-119">Настройка отладки</span><span class="sxs-lookup"><span data-stu-id="df94b-119">Setting Up Debugging</span></span>

<span data-ttu-id="df94b-120">Выполните следующие действия, чтобы настроить отладку для обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="df94b-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="df94b-121">Уведомите службу поиска об отладке, задав для параметра Дебугфилтерс значение 1 в реестре:</span><span class="sxs-lookup"><span data-stu-id="df94b-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="df94b-122">Подключите отладчик с помощью раздела реестра параметры выполнения файла образа:</span><span class="sxs-lookup"><span data-stu-id="df94b-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="df94b-123">Параметры для примера отладчика описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="df94b-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="df94b-124">**Пример с использованием отладчика NTSD**   *= C: \\ Отладчики \\ntsd.exe-одгкс-c: "sxe ld mydll.dll; g"*</span><span class="sxs-lookup"><span data-stu-id="df94b-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="df94b-125">Перезапустите searchindexer.exe в отладчике с помощью compmgmt. msc, Services. msc или командного окна с командами, аналогичными следующим:</span><span class="sxs-lookup"><span data-stu-id="df94b-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="df94b-126">Чтобы отличить процесс Сеарчпротоколхост, выполняемый в контексте системы, и запустить его в контексте пользователя, можно проверить строки среды.</span><span class="sxs-lookup"><span data-stu-id="df94b-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="df94b-127">Например, с помощью ntsd.exe можно использовать команду Extension **! пеб** для отображения форматированного представления информации в блоке среды Process (пеб).</span><span class="sxs-lookup"><span data-stu-id="df94b-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df94b-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df94b-128">Additional Resources</span></span>

-   <span data-ttu-id="df94b-129">Сведения о создании обработчиков см. в разделе [Регистрация расширений оболочки](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="df94b-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df94b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="df94b-130">Related topics</span></span>

<dl> <span data-ttu-id="df94b-131"><dt>**Основные**</dt> <dt><a href="-search-3x-wds-phaddins.md">обработчики протокола разработки</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Основные сведения об обработчиках протоколов</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">уведомление об изменении индекса изменений</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Добавление значков и контекстных меню</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">пример кода: расширения оболочки для обработчиков протоколов</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Создание соединителя поиска для обработчика протокола</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Установка и регистрация обработчиков протоколов</a></dt> </span><span class="sxs-lookup"><span data-stu-id="df94b-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
