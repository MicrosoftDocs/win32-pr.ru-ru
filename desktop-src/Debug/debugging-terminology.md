---
description: При описании отладки используются следующие термины.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Терминология отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990324"
---
# <a name="debugging-terminology"></a><span data-ttu-id="f7cb0-103">Терминология отладки</span><span class="sxs-lookup"><span data-stu-id="f7cb0-103">Debugging Terminology</span></span>

<span data-ttu-id="f7cb0-104">При описании отладки используются следующие термины.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="f7cb0-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Синий экран</span><span class="sxs-lookup"><span data-stu-id="f7cb0-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-106">Когда система обнаруживает неполадки оборудования, несогласованность данных или аналогичную ошибку, она может отобразить синий экран, содержащий сведения, которые можно использовать для определения причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="f7cb0-107">Эти сведения включают код завершения и создание файла аварийного дампа.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="f7cb0-108">Он также может включать список загруженных драйверов и трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Файл аварийной копии памяти</span><span class="sxs-lookup"><span data-stu-id="f7cb0-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-110">Можно настроить систему для записи данных в файл аварийного дампа на жестком диске при создании кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="f7cb0-111">Файл содержит сведения, которые отладчик может использовать для анализа ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="f7cb0-112">Этот файл может быть таким же большим, как и физическая память, содержащаяся на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Отладчик</span><span class="sxs-lookup"><span data-stu-id="f7cb0-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-114">Программа, предназначенная для обнаружения, обнаружения и исправления ошибок в другой программе.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="f7cb0-115">Он позволяет разработчику выполнять этапы выполнения процесса и его потоков, отслеживать память, переменные и другие элементы контекста процесса и потока.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Режим ядра</span><span class="sxs-lookup"><span data-stu-id="f7cb0-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-117">Режим процессора, в котором запускаются системные службы и драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="f7cb0-118">Все интерфейсы и инструкции по ЦП доступны, и вся память доступна.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Файл минидампа</span><span class="sxs-lookup"><span data-stu-id="f7cb0-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-120">Приложения могут создавать файлы минидампа пользовательского режима, которые содержат полезное подмножество данных, содержащихся в файле аварийного дампа.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="f7cb0-121">Дополнительные сведения см. в разделе [файлы минидампа](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="f7cb0-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Код завершения</span><span class="sxs-lookup"><span data-stu-id="f7cb0-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-123">Код ошибки, определяющий ошибку, которая остановила выполнение системного ядра.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Файлы символов</span><span class="sxs-lookup"><span data-stu-id="f7cb0-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-125">Все системные приложения, драйверы и библиотеки DLL строятся таким образом, что отладочная информация размещается в отдельных файлах, известных как файлы символов.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="f7cb0-126">Таким образом, система меньше и быстрее, но ее по-прежнему можно отлаживать при установке файлов символов.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="f7cb0-127">Дополнительные сведения см. в разделе [файлы символов](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="f7cb0-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7cb0-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Пользовательский режим</span><span class="sxs-lookup"><span data-stu-id="f7cb0-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="f7cb0-129">Режим процессора, в котором выполняются приложения.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-129">The processor mode in which applications run.</span></span> <span data-ttu-id="f7cb0-130">В этом режиме доступен ограниченный набор интерфейсов, и доступ к системным данным ограничен.</span><span class="sxs-lookup"><span data-stu-id="f7cb0-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f7cb0-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f7cb0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7cb0-132">Настройка автоматической отладки</span><span class="sxs-lookup"><span data-stu-id="f7cb0-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



