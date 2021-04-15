---
description: Чтобы получить данные трассировки для инфраструктуры VSS, можно использовать средство Всстраце, средство logman или средство tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Использование средств трассировки с VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263099"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="abd17-103">Использование средств трассировки с VSS</span><span class="sxs-lookup"><span data-stu-id="abd17-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="abd17-104">Чтобы получить данные трассировки для инфраструктуры VSS, можно использовать средство Всстраце, средство logman или средство tracelog.</span><span class="sxs-lookup"><span data-stu-id="abd17-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="abd17-105">Всстраце доступен в пакете средств разработки программного обеспечения Microsoft Windows (SDK) и может использоваться для трассировки приложений VSS в Windows 7 и более поздних версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="abd17-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="abd17-106">Logman — это контроллер трассировки для событий трассировки и счетчиков производительности; его также можно использовать для трассировки приложений VSS в Windows 7 и более поздних версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="abd17-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="abd17-107">Tracelog входит в комплект драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="abd17-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="abd17-108">Сведения об использовании средств трассировки с помощью [автоматического восстановления системы (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md)см. в статье [использование средств трассировки с приложениями ASR](using-tracing-tools-with-vss-asr-applications.md).</span><span class="sxs-lookup"><span data-stu-id="abd17-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="abd17-109">Для всех Всстраце, Logman и tracelog требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="abd17-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="abd17-110">Сведения о каждом средстве см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="abd17-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="abd17-111">Использование Всстраце</span><span class="sxs-lookup"><span data-stu-id="abd17-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="abd17-112">Параметры Command-Line Всстраце</span><span class="sxs-lookup"><span data-stu-id="abd17-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="abd17-113">Использование программы Logman</span><span class="sxs-lookup"><span data-stu-id="abd17-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="abd17-114">Использование tracelog</span><span class="sxs-lookup"><span data-stu-id="abd17-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="abd17-115">Использование Всстраце</span><span class="sxs-lookup"><span data-stu-id="abd17-115">Using VssTrace</span></span>

<span data-ttu-id="abd17-116">Чтобы запустить средство Всстраце из командной строки, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="abd17-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="abd17-117"> *Параметры командной строки* всстраце</span><span class="sxs-lookup"><span data-stu-id="abd17-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="abd17-118">Чтобы отобразить краткую справку командной строки для средства Всстраце, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="abd17-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="abd17-119">**всстраце — Справка**</span><span class="sxs-lookup"><span data-stu-id="abd17-119">**vsstrace -help**</span></span>

<span data-ttu-id="abd17-120">Чтобы отобразить подробную справку по командной строке для средства Всстраце, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="abd17-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="abd17-121">**всстраце — Справка все**</span><span class="sxs-lookup"><span data-stu-id="abd17-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="abd17-122">Параметры Command-Line Всстраце</span><span class="sxs-lookup"><span data-stu-id="abd17-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="abd17-123">Средство Всстраце использует следующие параметры командной строки:</span><span class="sxs-lookup"><span data-stu-id="abd17-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="abd17-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>*Флаги* **-f**</span><span class="sxs-lookup"><span data-stu-id="abd17-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-125">Включите модули, флаги которых задаются битовой маской *флагов* .</span><span class="sxs-lookup"><span data-stu-id="abd17-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="abd17-126">Каждый флаг соответствует модулю VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="abd17-127">Если *Флаги* равны нулю, модули не включены.</span><span class="sxs-lookup"><span data-stu-id="abd17-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="abd17-128">Обратите внимание, что большинство модулей включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="abd17-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="abd17-129">Этот параметр можно сочетать с **+** параметром _module_ .</span><span class="sxs-lookup"><span data-stu-id="abd17-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="abd17-130">Например, **всстраце-f 0 + WRITER + курд** отключает трассировку всех модулей, включенных по умолчанию, и позволяет отслеживать модули записи VSS и службу VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="abd17-131">Кроме того, **всстраце + f 0xFFFF-курд** включает трассировку всех модулей, кроме службы VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="abd17-132">Если параметр **-f** используется вместе с **+** параметром _module_ , то **-f** должен предшествовать **+** параметру _module_ .</span><span class="sxs-lookup"><span data-stu-id="abd17-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="abd17-133">В следующей таблице перечислены имя модуля и флаг для каждого доступного модуля.</span><span class="sxs-lookup"><span data-stu-id="abd17-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="abd17-134">Модуль</span><span class="sxs-lookup"><span data-stu-id="abd17-134">Module</span></span> | <span data-ttu-id="abd17-135">Flag</span><span class="sxs-lookup"><span data-stu-id="abd17-135">Flag</span></span>       | <span data-ttu-id="abd17-136">По умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="abd17-136">Enabled by default</span></span> | <span data-ttu-id="abd17-137">Отслеживаемые элементы</span><span class="sxs-lookup"><span data-stu-id="abd17-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd17-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="abd17-138">EXCEPT</span></span> | <span data-ttu-id="abd17-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="abd17-139">0x00000001</span></span> | <span data-ttu-id="abd17-140">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-140">Yes</span></span>                | <span data-ttu-id="abd17-141">Обработка исключений C++.</span><span class="sxs-lookup"><span data-stu-id="abd17-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="abd17-142">курд</span><span class="sxs-lookup"><span data-stu-id="abd17-142">COORD</span></span>  | <span data-ttu-id="abd17-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="abd17-143">0x00000002</span></span> | <span data-ttu-id="abd17-144">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-144">Yes</span></span>                | <span data-ttu-id="abd17-145">Служба VSS, которая также называется координатором VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="abd17-146">свпрв</span><span class="sxs-lookup"><span data-stu-id="abd17-146">SWPRV</span></span>  | <span data-ttu-id="abd17-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="abd17-147">0x00000004</span></span> | <span data-ttu-id="abd17-148">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-148">Yes</span></span>                | <span data-ttu-id="abd17-149">Служба поставщика теневого копирования системы VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="abd17-150">букомп</span><span class="sxs-lookup"><span data-stu-id="abd17-150">BUCOMP</span></span> | <span data-ttu-id="abd17-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="abd17-151">0x00000008</span></span> | <span data-ttu-id="abd17-152">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-152">Yes</span></span>                | <span data-ttu-id="abd17-153">Инициатор запроса VSS и обработка метаданных резервной копии.</span><span class="sxs-lookup"><span data-stu-id="abd17-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="abd17-154">WRITER.</span><span class="sxs-lookup"><span data-stu-id="abd17-154">WRITER</span></span> | <span data-ttu-id="abd17-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="abd17-155">0x00000010</span></span> | <span data-ttu-id="abd17-156">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-156">Yes</span></span>                | <span data-ttu-id="abd17-157">Операции модуля записи VSS и реализации размещаемого модуля записи VSS, такие как модуль записи реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="abd17-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="abd17-158">вссапи</span><span class="sxs-lookup"><span data-stu-id="abd17-158">VSSAPI</span></span> | <span data-ttu-id="abd17-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="abd17-159">0x00000020</span></span> | <span data-ttu-id="abd17-160">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-160">Yes</span></span>                | <span data-ttu-id="abd17-161">Различные функции API VSS, экспортированные VSSAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="abd17-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="abd17-162">хвдиаг</span><span class="sxs-lookup"><span data-stu-id="abd17-162">HWDIAG</span></span> | <span data-ttu-id="abd17-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="abd17-163">0x00000040</span></span> | <span data-ttu-id="abd17-164">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-164">Yes</span></span>                | <span data-ttu-id="abd17-165">Инфраструктура и операции поставщика оборудования VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="abd17-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="abd17-166">ADMIN</span></span>  | <span data-ttu-id="abd17-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="abd17-167">0x00000080</span></span> | <span data-ttu-id="abd17-168">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-168">Yes</span></span>                | <span data-ttu-id="abd17-169">Служебные программы командной строки VSS, такие как VSSADMIN.EXE и DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="abd17-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="abd17-170">вссуи</span><span class="sxs-lookup"><span data-stu-id="abd17-170">VSSUI</span></span>  | <span data-ttu-id="abd17-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="abd17-171">0x00000100</span></span> | <span data-ttu-id="abd17-172">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-172">Yes</span></span>                | <span data-ttu-id="abd17-173">Пользовательский интерфейс конфигурации теневые копии общих папок.</span><span class="sxs-lookup"><span data-stu-id="abd17-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="abd17-174">Пользовательский интерфейс доступен только в операционных системах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="abd17-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="abd17-175">TEST</span><span class="sxs-lookup"><span data-stu-id="abd17-175">TEST</span></span>   | <span data-ttu-id="abd17-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="abd17-176">0x00000200</span></span> | <span data-ttu-id="abd17-177">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-177">Yes</span></span>                | <span data-ttu-id="abd17-178">Не применяется</span><span class="sxs-lookup"><span data-stu-id="abd17-178">Not applicable.</span></span> <span data-ttu-id="abd17-179">(Этот модуль трассировки зарезервирован.)</span><span class="sxs-lookup"><span data-stu-id="abd17-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="abd17-180">ЗАПРОС</span><span class="sxs-lookup"><span data-stu-id="abd17-180">IOCTL</span></span>  | <span data-ttu-id="abd17-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="abd17-181">0x00000400</span></span> | <span data-ttu-id="abd17-182">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-182">Yes</span></span>                | <span data-ttu-id="abd17-183">Сведения об операциях ФСКТЛ и IOCTL, инициированных службой VSS путем вызова функции [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="abd17-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="abd17-184">ОПЕРАЦИЙ</span><span class="sxs-lookup"><span data-stu-id="abd17-184">GEN</span></span>    | <span data-ttu-id="abd17-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="abd17-185">0x00000800</span></span> | <span data-ttu-id="abd17-186">Да</span><span class="sxs-lookup"><span data-stu-id="abd17-186">Yes</span></span>                | <span data-ttu-id="abd17-187">Общие служебные функции VSS, такие как распределительы, классы строковых классов, операции с реестром и томами.</span><span class="sxs-lookup"><span data-stu-id="abd17-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="abd17-188">врксмл</span><span class="sxs-lookup"><span data-stu-id="abd17-188">WRXML</span></span>  | <span data-ttu-id="abd17-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="abd17-189">0x00001000</span></span> | <span data-ttu-id="abd17-190">Нет</span><span class="sxs-lookup"><span data-stu-id="abd17-190">No</span></span>                 | <span data-ttu-id="abd17-191">Обработка XML для метаданных модуля записи.</span><span class="sxs-lookup"><span data-stu-id="abd17-191">XML processing for writer metadata.</span></span> <span data-ttu-id="abd17-192">Этот модуль имеет очень высокий уровень шума.</span><span class="sxs-lookup"><span data-stu-id="abd17-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="abd17-193">вссксмл</span><span class="sxs-lookup"><span data-stu-id="abd17-193">VSSXML</span></span> | <span data-ttu-id="abd17-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="abd17-194">0x00002000</span></span> | <span data-ttu-id="abd17-195">Нет</span><span class="sxs-lookup"><span data-stu-id="abd17-195">No</span></span>                 | <span data-ttu-id="abd17-196">Базовые классы обработки XML.</span><span class="sxs-lookup"><span data-stu-id="abd17-196">XML processing base classes.</span></span> <span data-ttu-id="abd17-197">Этот модуль имеет очень высокий уровень шума.</span><span class="sxs-lookup"><span data-stu-id="abd17-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="abd17-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Модуль_</span><span class="sxs-lookup"><span data-stu-id="abd17-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="abd17-199">Включите модуль, указанный *модулем*.</span><span class="sxs-lookup"><span data-stu-id="abd17-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="abd17-200">В каждый момент времени можно включить несколько модулей.</span><span class="sxs-lookup"><span data-stu-id="abd17-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="abd17-201">Чтобы получить список доступных модулей, введите в командной строке **всстраце – Help modules** .</span><span class="sxs-lookup"><span data-stu-id="abd17-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Модуль_</span><span class="sxs-lookup"><span data-stu-id="abd17-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="abd17-203">Отключите модуль, указанный *модулем*.</span><span class="sxs-lookup"><span data-stu-id="abd17-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="abd17-204">Чтобы получить список доступных модулей, введите в командной строке **всстраце – Help modules** .</span><span class="sxs-lookup"><span data-stu-id="abd17-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID идентификатор** *процесса*</span><span class="sxs-lookup"><span data-stu-id="abd17-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-206">Включите процесс, указанный в параметре *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="abd17-207">Чтобы включить все процессы, используйте " \* " для значения *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="abd17-208">В каждый момент времени можно указать несколько параметров **PID** .</span><span class="sxs-lookup"><span data-stu-id="abd17-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="abd17-209">Порядок параметров определяет, какие процессы включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="abd17-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="abd17-210">Например, чтобы включить только процесс, идентификатор процесса которого — 0xe8c, используйте **всстраце-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="abd17-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="abd17-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-212">Отключите процесс, указанный в параметре *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="abd17-213">Чтобы отключить все процессы, используйте " \* " для значения *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="abd17-214">В каждый момент времени можно указать несколько параметров **PID** .</span><span class="sxs-lookup"><span data-stu-id="abd17-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="abd17-215">Порядок параметров определяет, какие процессы включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="abd17-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="abd17-216">Например, чтобы отключить все процессы, кроме процесса, идентификатор процесса которого — 0xe8c, используйте **всстраце-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="abd17-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ tid** , *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="abd17-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-218">Включите поток, указанный в *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="abd17-219">Чтобы включить все потоки, используйте " \* " для значения *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="abd17-220">Одновременно может быть задано более одного параметра **tid** .</span><span class="sxs-lookup"><span data-stu-id="abd17-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="abd17-221">Порядок параметров определяет, какие потоки включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="abd17-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="abd17-222">Например, чтобы включить только поток, идентификатор процесса которого — 0x31a, используйте **всстраце-TID \* + tid 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="abd17-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**— tid** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="abd17-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-224">Отключите поток, указанный в *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="abd17-225">Чтобы отключить все потоки, используйте " \* " для значения *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="abd17-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="abd17-226">Одновременно может быть задано более одного параметра **tid** .</span><span class="sxs-lookup"><span data-stu-id="abd17-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="abd17-227">Порядок параметров определяет, какие потоки включены или отключены.</span><span class="sxs-lookup"><span data-stu-id="abd17-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="abd17-228">Например, чтобы отключить все потоки, за исключением потока, идентификатор процесса которого — 0x31a, используйте **всстраце-TID \* + tid 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="abd17-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span> *уровень* l</span><span class="sxs-lookup"><span data-stu-id="abd17-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-230">Используйте уровень трассировки, заданный параметром *Level*.</span><span class="sxs-lookup"><span data-stu-id="abd17-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="abd17-231">Чем выше уровень, тем более подробные выходные данные трассировки.</span><span class="sxs-lookup"><span data-stu-id="abd17-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="abd17-232">Каждый уровень включает все нижние уровни.</span><span class="sxs-lookup"><span data-stu-id="abd17-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="abd17-233">Уровень по умолчанию — 170.</span><span class="sxs-lookup"><span data-stu-id="abd17-233">The default level is 170.</span></span> <span data-ttu-id="abd17-234">Доступны следующие уровни.</span><span class="sxs-lookup"><span data-stu-id="abd17-234">The following levels are available.</span></span>



| <span data-ttu-id="abd17-235">Level</span><span class="sxs-lookup"><span data-stu-id="abd17-235">Level</span></span> | <span data-ttu-id="abd17-236">Сведения, включаемые в выходные данные трассировки</span><span class="sxs-lookup"><span data-stu-id="abd17-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="abd17-237">000</span><span class="sxs-lookup"><span data-stu-id="abd17-237">000</span></span>   | <span data-ttu-id="abd17-238">Нет</span><span class="sxs-lookup"><span data-stu-id="abd17-238">None</span></span>                                     |
| <span data-ttu-id="abd17-239">020</span><span class="sxs-lookup"><span data-stu-id="abd17-239">020</span></span>   | <span data-ttu-id="abd17-240">Неустранимые ошибки</span><span class="sxs-lookup"><span data-stu-id="abd17-240">Fatal errors</span></span>                             |
| <span data-ttu-id="abd17-241">030</span><span class="sxs-lookup"><span data-stu-id="abd17-241">030</span></span>   | <span data-ttu-id="abd17-242">необработанных исключений.</span><span class="sxs-lookup"><span data-stu-id="abd17-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="abd17-243">040</span><span class="sxs-lookup"><span data-stu-id="abd17-243">040</span></span>   | <span data-ttu-id="abd17-244">ошибки</span><span class="sxs-lookup"><span data-stu-id="abd17-244">Errors</span></span>                                   |
| <span data-ttu-id="abd17-245">050</span><span class="sxs-lookup"><span data-stu-id="abd17-245">050</span></span>   | <span data-ttu-id="abd17-246">Утверждения</span><span class="sxs-lookup"><span data-stu-id="abd17-246">Assertions</span></span>                               |
| <span data-ttu-id="abd17-247">060</span><span class="sxs-lookup"><span data-stu-id="abd17-247">060</span></span>   | <span data-ttu-id="abd17-248">Предупреждения</span><span class="sxs-lookup"><span data-stu-id="abd17-248">Warnings</span></span>                                 |
| <span data-ttu-id="abd17-249">080</span><span class="sxs-lookup"><span data-stu-id="abd17-249">080</span></span>   | <span data-ttu-id="abd17-250">Обработка исключений</span><span class="sxs-lookup"><span data-stu-id="abd17-250">Exception handling</span></span>                       |
| <span data-ttu-id="abd17-251">100</span><span class="sxs-lookup"><span data-stu-id="abd17-251">100</span></span>   | <span data-ttu-id="abd17-252">Действие "журнал событий"</span><span class="sxs-lookup"><span data-stu-id="abd17-252">Event Log activity</span></span>                       |
| <span data-ttu-id="abd17-253">120</span><span class="sxs-lookup"><span data-stu-id="abd17-253">120</span></span>   | <span data-ttu-id="abd17-254">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="abd17-254">General information</span></span>                      |
| <span data-ttu-id="abd17-255">140</span><span class="sxs-lookup"><span data-stu-id="abd17-255">140</span></span>   | <span data-ttu-id="abd17-256">поток кода.</span><span class="sxs-lookup"><span data-stu-id="abd17-256">Code flow</span></span>                                |
| <span data-ttu-id="abd17-257">160</span><span class="sxs-lookup"><span data-stu-id="abd17-257">160</span></span>   | <span data-ttu-id="abd17-258">Вход и выход из функции</span><span class="sxs-lookup"><span data-stu-id="abd17-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="abd17-259">170</span><span class="sxs-lookup"><span data-stu-id="abd17-259">170</span></span>   | <span data-ttu-id="abd17-260">Возвращаемые значения функции</span><span class="sxs-lookup"><span data-stu-id="abd17-260">Function return values</span></span>                   |
| <span data-ttu-id="abd17-261">180</span><span class="sxs-lookup"><span data-stu-id="abd17-261">180</span></span>   | <span data-ttu-id="abd17-262">Параметры функции (сжатые)</span><span class="sxs-lookup"><span data-stu-id="abd17-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="abd17-263">190</span><span class="sxs-lookup"><span data-stu-id="abd17-263">190</span></span>   | <span data-ttu-id="abd17-264">Параметры функции (verbose)</span><span class="sxs-lookup"><span data-stu-id="abd17-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="abd17-265">200</span><span class="sxs-lookup"><span data-stu-id="abd17-265">200</span></span>   | <span data-ttu-id="abd17-266">Подробный уровень информации 1</span><span class="sxs-lookup"><span data-stu-id="abd17-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="abd17-267">210</span><span class="sxs-lookup"><span data-stu-id="abd17-267">210</span></span>   | <span data-ttu-id="abd17-268">Подробный уровень информации 2</span><span class="sxs-lookup"><span data-stu-id="abd17-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="abd17-269">220</span><span class="sxs-lookup"><span data-stu-id="abd17-269">220</span></span>   | <span data-ttu-id="abd17-270">Подробный уровень информации 3</span><span class="sxs-lookup"><span data-stu-id="abd17-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="abd17-271">230</span><span class="sxs-lookup"><span data-stu-id="abd17-271">230</span></span>   | <span data-ttu-id="abd17-272">Быстрый уровень кода 1</span><span class="sxs-lookup"><span data-stu-id="abd17-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="abd17-273">240</span><span class="sxs-lookup"><span data-stu-id="abd17-273">240</span></span>   | <span data-ttu-id="abd17-274">Быстрый уровень кода 2</span><span class="sxs-lookup"><span data-stu-id="abd17-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="abd17-275">250</span><span class="sxs-lookup"><span data-stu-id="abd17-275">250</span></span>   | <span data-ttu-id="abd17-276">Быстрый уровень кода 3</span><span class="sxs-lookup"><span data-stu-id="abd17-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="abd17-277">255</span><span class="sxs-lookup"><span data-stu-id="abd17-277">255</span></span>   | <span data-ttu-id="abd17-278">Все</span><span class="sxs-lookup"><span data-stu-id="abd17-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="abd17-279"><span id="_indent"></span><span id="_INDENT"></span>**+ отступ**</span><span class="sxs-lookup"><span data-stu-id="abd17-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="abd17-280">Отступ форматированного вывода трассировки для каждой функции и границы подфункции.</span><span class="sxs-lookup"><span data-stu-id="abd17-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-281"><span id="-indent"></span><span id="-INDENT"></span>**— отступ**</span><span class="sxs-lookup"><span data-stu-id="abd17-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="abd17-282">Не изменять отступ форматированного вывода трассировки.</span><span class="sxs-lookup"><span data-stu-id="abd17-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *етлфиле*</span><span class="sxs-lookup"><span data-stu-id="abd17-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-284">Преобразование выходного файла logman, указанного параметром *етлфиле* , в текстовый формат для чтения.</span><span class="sxs-lookup"><span data-stu-id="abd17-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *выходной_файл*</span><span class="sxs-lookup"><span data-stu-id="abd17-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-286">Сохраните данные трассировки в выходной файл, указанный в файле *выходной_файл*.</span><span class="sxs-lookup"><span data-stu-id="abd17-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="abd17-287">Для лучшей производительности выходной файл должен находиться на томе, который не является частью теневой копии.</span><span class="sxs-lookup"><span data-stu-id="abd17-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="abd17-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *хелпоптион*</span><span class="sxs-lookup"><span data-stu-id="abd17-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="abd17-289">Отобразить справку командной строки, указанную параметром *хелпоптион*.</span><span class="sxs-lookup"><span data-stu-id="abd17-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="abd17-290">Допустимые значения *хелпоптион* : **modules**, **Levels** и **ALL**.</span><span class="sxs-lookup"><span data-stu-id="abd17-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="abd17-291">Указание **модулей** вызывает перечисление модулей.</span><span class="sxs-lookup"><span data-stu-id="abd17-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="abd17-292">Задание **уровней** приводит к отображению доступных уровней.</span><span class="sxs-lookup"><span data-stu-id="abd17-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="abd17-293">Указание параметра **ALL** приводит к отображению подробной справки.</span><span class="sxs-lookup"><span data-stu-id="abd17-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="abd17-294">Если параметры не используются, отображается краткая справка.</span><span class="sxs-lookup"><span data-stu-id="abd17-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="abd17-295">Использование программы Logman</span><span class="sxs-lookup"><span data-stu-id="abd17-295">Using Logman</span></span>

<span data-ttu-id="abd17-296">В следующей процедуре описывается использование программы Logman с приложением VSS.</span><span class="sxs-lookup"><span data-stu-id="abd17-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="abd17-297">**Использование программы Logman с приложением VSS**</span><span class="sxs-lookup"><span data-stu-id="abd17-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="abd17-298">Чтобы начать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="abd17-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="abd17-299">**Logman Start VSS-o** *x: \\ \* \* \* VSS. ETL-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span><span class="sxs-lookup"><span data-stu-id="abd17-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="abd17-300">Замените "x: \\ " на путь к каталогу, в котором должен храниться файл журнала трассировки.</span><span class="sxs-lookup"><span data-stu-id="abd17-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="abd17-301">Чтобы прерывать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="abd17-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="abd17-302">**Logman останавливает VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="abd17-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="abd17-303">Файл журнала трассировки — *x: \\* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="abd17-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="abd17-304">Дополнительные сведения о средстве Logman см. в разделе [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="abd17-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="abd17-305">Использование tracelog</span><span class="sxs-lookup"><span data-stu-id="abd17-305">Using Tracelog</span></span>

<span data-ttu-id="abd17-306">В следующей процедуре описывается использование tracelog.</span><span class="sxs-lookup"><span data-stu-id="abd17-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="abd17-307">**Использование tracelog**</span><span class="sxs-lookup"><span data-stu-id="abd17-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="abd17-308">Создайте текстовый файл с именем VSS. CTL, который содержит только следующий текст:</span><span class="sxs-lookup"><span data-stu-id="abd17-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="abd17-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 VSS**</span><span class="sxs-lookup"><span data-stu-id="abd17-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="abd17-310">Чтобы начать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="abd17-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="abd17-311">**tracelog-Start VSS-f** *x: \\ \* \* \* VSS. ETL-GUID VSS. CTL-флаг 0xFF-Level 0xAA*\*</span><span class="sxs-lookup"><span data-stu-id="abd17-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="abd17-312">Замените "x: \\ " на путь к каталогу, в котором должен храниться файл журнала трассировки.</span><span class="sxs-lookup"><span data-stu-id="abd17-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="abd17-313">Чтобы прерывать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="abd17-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="abd17-314">**tracelog — останавливает VSS**</span><span class="sxs-lookup"><span data-stu-id="abd17-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="abd17-315">Файл журнала трассировки — *x: \\* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="abd17-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="abd17-316">Дополнительные сведения о средстве tracelog см. в разделе [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="abd17-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
