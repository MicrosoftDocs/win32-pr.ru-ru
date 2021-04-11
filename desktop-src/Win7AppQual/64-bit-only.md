---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Только 64-разрядная версия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272760"
---
# <a name="64-bit-only"></a><span data-ttu-id="f1a67-103">Только 64-разрядная версия</span><span class="sxs-lookup"><span data-stu-id="f1a67-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f1a67-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="f1a67-104">Affected Platforms</span></span>

<span data-ttu-id="f1a67-105">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1a67-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="f1a67-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="f1a67-106">Feature Impact</span></span>

 <span data-ttu-id="f1a67-107">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="f1a67-107">**Severity** - Low</span></span>  
<span data-ttu-id="f1a67-108">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="f1a67-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="f1a67-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f1a67-109">Description</span></span>

<span data-ttu-id="f1a67-110">Windows Server 2008 R2 поставляется только с 64-разрядным SKU. для серверной версии операционной системы не доступен номер SKU 32-bit.</span><span class="sxs-lookup"><span data-stu-id="f1a67-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="f1a67-111">Однако 32-разрядный SKU остается доступным для клиента Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f1a67-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f1a67-112">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="f1a67-112">Manifestation of Impact</span></span>

<span data-ttu-id="f1a67-113">Это может повлиять на три области:</span><span class="sxs-lookup"><span data-stu-id="f1a67-113">This will impact three areas:</span></span>

-   <span data-ttu-id="f1a67-114">32-разрядные драйверы</span><span class="sxs-lookup"><span data-stu-id="f1a67-114">32-bit drivers</span></span>
-   <span data-ttu-id="f1a67-115">32-разрядные подключаемые модули</span><span class="sxs-lookup"><span data-stu-id="f1a67-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="f1a67-116">16-разрядные исполняемые файлы</span><span class="sxs-lookup"><span data-stu-id="f1a67-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="f1a67-117">Решение для 32-разрядных драйверов</span><span class="sxs-lookup"><span data-stu-id="f1a67-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="f1a67-118">Перекомпиляция 32-разрядных драйверов как подписанных 64-разрядных драйверов.</span><span class="sxs-lookup"><span data-stu-id="f1a67-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="f1a67-119">Решение для 32-разрядных подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="f1a67-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="f1a67-120">Эмулятор с архитектурой x86, предназначенный для 32-разрядных приложений Windows, позволяет без 64 проблем работать с 32-битным Windows.</span><span class="sxs-lookup"><span data-stu-id="f1a67-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="f1a67-121">WoW64 теперь является необязательным компонентом, который необходимо установить, если необходимо выполнить 32-разрядный код.</span><span class="sxs-lookup"><span data-stu-id="f1a67-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="f1a67-122">Система изолирует 32-разрядные приложения от 64-разрядных приложений, что включает в себя предотвращение конфликтов файлов и реестра.</span><span class="sxs-lookup"><span data-stu-id="f1a67-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="f1a67-123">Поддерживаются консоль, графический пользовательский интерфейс и приложения службы.</span><span class="sxs-lookup"><span data-stu-id="f1a67-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="f1a67-124">Система обеспечивает взаимодействие на границе 32/64 для таких сценариев, как вырезание и вставка и COM.</span><span class="sxs-lookup"><span data-stu-id="f1a67-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="f1a67-125">Однако 32-разрядные процессы не могут загружать 64-разрядные библиотеки DLL, а 64-разрядные процессы не могут загружать 32-разрядные библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="f1a67-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="f1a67-126">Мы обычно увидим это в подключаемых модулях оболочки, написанных для проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="f1a67-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="f1a67-127">32-разрядное приложение может определить, выполняется ли оно в эмуляторе WOW64, вызвав функцию IsWow64Process.</span><span class="sxs-lookup"><span data-stu-id="f1a67-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="f1a67-128">Приложение может получить дополнительные сведения о процессоре с помощью функции Жетнативесистеминфо</span><span class="sxs-lookup"><span data-stu-id="f1a67-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="f1a67-129">Обратите внимание, что 64-разрядная версия Windows не поддерживает выполнение 16-разрядных приложений на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="f1a67-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="f1a67-130">Основная причина заключается в том, что дескрипторы имеют 32 значащих бит на 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="f1a67-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="f1a67-131">Поэтому дескрипторы не могут быть усечены и переданы в 16-разрядные приложения без потери данных.</span><span class="sxs-lookup"><span data-stu-id="f1a67-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="f1a67-132">Попытки запуска 16-разрядных приложений завершаются следующей ошибкой: ошибка \_ неправильный \_ Формат exe \_ .</span><span class="sxs-lookup"><span data-stu-id="f1a67-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="f1a67-133">Решение для 16-разрядных исполняемых файлов</span><span class="sxs-lookup"><span data-stu-id="f1a67-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="f1a67-134">64-разрядная версия Windows распознает ограниченное число конкретных 16-разрядных программ установщика и подставляет переданный в порт 32-разрядную версию.</span><span class="sxs-lookup"><span data-stu-id="f1a67-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="f1a67-135">Список подстановок хранится в реестре в следующем разделе: HKEY \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64. Встроенная поддержка нескольких ядер установщика, включая установщики InstallShield 5. x.</span><span class="sxs-lookup"><span data-stu-id="f1a67-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="f1a67-136">Обратите внимание, что 64-разрядная установщик Windows может легко установить 32-разрядные приложения на основе MSI в 64-bit Windows.</span><span class="sxs-lookup"><span data-stu-id="f1a67-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f1a67-137">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="f1a67-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="f1a67-138">Выполнение 32-разрядных приложений</span><span class="sxs-lookup"><span data-stu-id="f1a67-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="f1a67-139">Производительность и использование памяти</span><span class="sxs-lookup"><span data-stu-id="f1a67-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="f1a67-140">Сведения о реализации WOW64</span><span class="sxs-lookup"><span data-stu-id="f1a67-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="f1a67-141">Перенаправитель реестра</span><span class="sxs-lookup"><span data-stu-id="f1a67-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="f1a67-142">Перенаправитель файловой системы</span><span class="sxs-lookup"><span data-stu-id="f1a67-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="f1a67-143">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="f1a67-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="f1a67-144">Соответствие процессоров</span><span class="sxs-lookup"><span data-stu-id="f1a67-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="f1a67-145">Межпроцессное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="f1a67-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="f1a67-146">Установка приложения в 64-разрядных системах</span><span class="sxs-lookup"><span data-stu-id="f1a67-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="f1a67-147">Отладка WOW64</span><span class="sxs-lookup"><span data-stu-id="f1a67-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="f1a67-148">**Функция IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="f1a67-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="f1a67-149">**Функция Жетнативесистеминфо**</span><span class="sxs-lookup"><span data-stu-id="f1a67-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
