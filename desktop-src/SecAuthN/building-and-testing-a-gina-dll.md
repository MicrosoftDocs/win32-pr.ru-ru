---
description: Все функции, прототипы, структуры и константы определены в файле заголовка Винвлкс. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Создание и тестирование библиотеки DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352045"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="627be-103">Создание и тестирование библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="627be-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="627be-104">Все функции, прототипы, структуры и константы определены в файле заголовка Винвлкс. h.</span><span class="sxs-lookup"><span data-stu-id="627be-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="627be-105">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="627be-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="627be-106">Для тестирования библиотеки DLL [*GINA*](/windows/desktop/SecGloss/g-gly) используйте Winlogon.exe из проверенной версии операционной системы, которая доступна в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="627be-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="627be-107">Проверенная версия [*Winlogon*](/windows/desktop/SecGloss/w-gly) поддерживает отладку GINA следующим образом.</span><span class="sxs-lookup"><span data-stu-id="627be-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="627be-108">Для создания раздела в Win.ini можно использовать следующий синтаксис, чтобы указать параметры отладки Winlogon.</span><span class="sxs-lookup"><span data-stu-id="627be-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="627be-109">Если указано, файл **журнала** должен содержать полное имя файла, которое будет использоваться для регистрации отладочной информации.</span><span class="sxs-lookup"><span data-stu-id="627be-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="627be-110">Если файл не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="627be-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="627be-111">Параметры **дебугфлагс** указывают, какие типы отладочной информации следует записать в файл журнала или в отладчик.</span><span class="sxs-lookup"><span data-stu-id="627be-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="627be-112">**Дебугфлагс** может содержать один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="627be-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="627be-113">Флаг отладки</span><span class="sxs-lookup"><span data-stu-id="627be-113">Debugging flag</span></span> | <span data-ttu-id="627be-114">Описание</span><span class="sxs-lookup"><span data-stu-id="627be-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="627be-115">кулсвитч</span><span class="sxs-lookup"><span data-stu-id="627be-115">CoolSwitch</span></span>     | <span data-ttu-id="627be-116">Сочетание клавиш CTRL + ALT + SHIFT + TAB вызовет прерывание отладки в Winlogon.</span><span class="sxs-lookup"><span data-stu-id="627be-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="627be-117">Ошибка</span><span class="sxs-lookup"><span data-stu-id="627be-117">Error</span></span>          | <span data-ttu-id="627be-118">Печать ошибок.</span><span class="sxs-lookup"><span data-stu-id="627be-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="627be-119">Init</span><span class="sxs-lookup"><span data-stu-id="627be-119">Init</span></span>           | <span data-ttu-id="627be-120">Печать сообщений инициализации и хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="627be-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="627be-121">Уведомление</span><span class="sxs-lookup"><span data-stu-id="627be-121">Notify</span></span>         | <span data-ttu-id="627be-122">Печать сообщений пакета уведомлений.</span><span class="sxs-lookup"><span data-stu-id="627be-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="627be-123">SAS</span><span class="sxs-lookup"><span data-stu-id="627be-123">SAS</span></span>            | <span data-ttu-id="627be-124">Печать сведений о уведомлениях о [*последовательности безопасных предупреждений*](/windows/desktop/SecGloss/s-gly) (SAS).</span><span class="sxs-lookup"><span data-stu-id="627be-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="627be-125">Состояние</span><span class="sxs-lookup"><span data-stu-id="627be-125">State</span></span>          | <span data-ttu-id="627be-126">Печать сообщений при изменении состояния Winlogon.</span><span class="sxs-lookup"><span data-stu-id="627be-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="627be-127">Время ожидания</span><span class="sxs-lookup"><span data-stu-id="627be-127">Timeout</span></span>        | <span data-ttu-id="627be-128">Печать сообщений, если задано ограничение по времени или достигнуто ограничение по времени.</span><span class="sxs-lookup"><span data-stu-id="627be-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="627be-129">Трассировка</span><span class="sxs-lookup"><span data-stu-id="627be-129">Trace</span></span>          | <span data-ttu-id="627be-130">Печать подробных сведений о трассировке.</span><span class="sxs-lookup"><span data-stu-id="627be-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="627be-131">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="627be-131">Warn</span></span>           | <span data-ttu-id="627be-132">Выводить предупреждения.</span><span class="sxs-lookup"><span data-stu-id="627be-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="627be-133">Чтобы запустить проверенную версию Winlogon в отладчике, добавьте в реестр следующую запись:</span><span class="sxs-lookup"><span data-stu-id="627be-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="627be-134">Для отладки Winlogon необходимо использовать символьный отладчик Windows (NTSD).</span><span class="sxs-lookup"><span data-stu-id="627be-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="627be-135">См. также</span><span class="sxs-lookup"><span data-stu-id="627be-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="627be-136">Загрузка и запуск библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="627be-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="627be-137">Функции экспорта GINA</span><span class="sxs-lookup"><span data-stu-id="627be-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="627be-138">Структуры GINA</span><span class="sxs-lookup"><span data-stu-id="627be-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="627be-139">Функции GINA служб терминалов</span><span class="sxs-lookup"><span data-stu-id="627be-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
