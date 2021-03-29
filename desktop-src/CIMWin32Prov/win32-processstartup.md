---
description: '\_Абстрактный класс WMI Процессстартуп Win32 представляет конфигурацию запуска процесса Windows.'
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Класс Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8def1e7ff8e3011d5ca6c2df303818bea36eca65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141046"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="b01eb-103">\_Класс Win32 процессстартуп</span><span class="sxs-lookup"><span data-stu-id="b01eb-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="b01eb-104">Абстрактный [класс WMI](../wmisdk/retrieving-a-class.md) **\_ процессстартуп Win32** представляет конфигурацию запуска процесса Windows.</span><span class="sxs-lookup"><span data-stu-id="b01eb-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="b01eb-105">Класс определяется как определение типа метода, что означает, что он используется только для передачи информации в метод [**CREATE**](create-method-in-class-win32-process.md) класса [**\_ процесса Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="b01eb-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="b01eb-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b01eb-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b01eb-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="b01eb-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b01eb-108">Members</span></span>

<span data-ttu-id="b01eb-109">Класс **Win32 \_ процессстартуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b01eb-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="b01eb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b01eb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b01eb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b01eb-111">Properties</span></span>

<span data-ttu-id="b01eb-112">Класс **Win32 \_ процессстартуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b01eb-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b01eb-113">**креатефлагс**</span><span class="sxs-lookup"><span data-stu-id="b01eb-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и функции потока \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| двкреатионфлагс")</span><span class="sxs-lookup"><span data-stu-id="b01eb-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-117">Дополнительные значения, управляющие классом приоритета и созданием процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="b01eb-118">Следующие значения создания могут быть указаны в любом сочетании, за исключением указанных.</span><span class="sxs-lookup"><span data-stu-id="b01eb-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="b01eb-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Отладка \_ Процесс** (1)</span><span class="sxs-lookup"><span data-stu-id="b01eb-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-120">Если этот флаг установлен, вызывающий процесс обрабатывается как отладчик, а новый процесс отлаживается.</span><span class="sxs-lookup"><span data-stu-id="b01eb-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="b01eb-121">Система уведомляет отладчик обо всех событиях отладки, происходящих в отлаживаемом процессе.</span><span class="sxs-lookup"><span data-stu-id="b01eb-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="b01eb-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Отладка \_ Только \_ этот \_ процесс** (2)</span><span class="sxs-lookup"><span data-stu-id="b01eb-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-123">Если этот флаг не установлен и выполняется отладка вызывающего процесса, новый процесс становится еще одним отлаживаемым процессом.</span><span class="sxs-lookup"><span data-stu-id="b01eb-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="b01eb-124">Если вызывающий процесс не является отлаживаемым процессом, действия, связанные с отладкой, не выполняются.</span><span class="sxs-lookup"><span data-stu-id="b01eb-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="b01eb-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Создание \_ Приостановлено** (4)</span><span class="sxs-lookup"><span data-stu-id="b01eb-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-126">Основной поток нового процесса создается в приостановленном состоянии и не выполняется до тех пор, пока не будет вызван метод [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="b01eb-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="b01eb-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>Отсоединено **\_ Процесс** (8)</span><span class="sxs-lookup"><span data-stu-id="b01eb-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-128">Для процессов консоли новый процесс не имеет доступа к консоли родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="b01eb-129">Этот флаг нельзя использовать, если установлен флаг **создания \_ новой \_ консоли** .</span><span class="sxs-lookup"><span data-stu-id="b01eb-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="b01eb-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Создание \_ Новая \_ консоль** (16)</span><span class="sxs-lookup"><span data-stu-id="b01eb-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-131">Этот новый процесс имеет новую консоль, а не наследует родительскую консоль.</span><span class="sxs-lookup"><span data-stu-id="b01eb-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="b01eb-132">Этот флаг нельзя использовать с флагом **отсоединенного \_ процесса** .</span><span class="sxs-lookup"><span data-stu-id="b01eb-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="b01eb-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Создание \_ Новая \_ \_ Группа процессов** (512)</span><span class="sxs-lookup"><span data-stu-id="b01eb-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-134">Этот новый процесс является корневым процессом новой группы процессов.</span><span class="sxs-lookup"><span data-stu-id="b01eb-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="b01eb-135">Группа процессов включает все процессы, которые являются потомками этого корневого процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="b01eb-136">Идентификатор процесса новой группы процессов совпадает с идентификатором процесса, возвращаемым в свойстве **ProcessID** класса [**\_ процесса Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="b01eb-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="b01eb-137">Группы процессов используются методом [**женератеконсолектрлевент**](/windows/console/generateconsolectrlevent) для включения отправки сигналов CTRL + C или Ctrl + Break в группу процессов консоли.</span><span class="sxs-lookup"><span data-stu-id="b01eb-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="b01eb-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Создание \_ \_Среда Юникода** (1024)</span><span class="sxs-lookup"><span data-stu-id="b01eb-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-139">Параметры среды, перечисленные в свойстве **EnvironmentVariables** , используют символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="b01eb-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="b01eb-140">Если этот флаг не установлен, блок среды использует символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="b01eb-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="b01eb-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Создание \_ \_ \_ Режим ошибок по умолчанию** (67108864)</span><span class="sxs-lookup"><span data-stu-id="b01eb-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-142">Только что созданные процессы получают по умолчанию системный режим ошибок вызывающего процесса, а не наследуют режим ошибок родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="b01eb-143">Этот флаг полезен для многопоточных приложений оболочки, которые выполняются с отключенными жесткими ошибками.</span><span class="sxs-lookup"><span data-stu-id="b01eb-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="b01eb-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Создание \_ БРЕАКАВАЙ \_ из \_ задания** (16777216)</span><span class="sxs-lookup"><span data-stu-id="b01eb-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-145">Используется, чтобы созданный процесс не был ограничен объектом задания.</span><span class="sxs-lookup"><span data-stu-id="b01eb-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b01eb-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="b01eb-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-147">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b01eb-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-149">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hKey \_ Текущая \_ Пользовательская \\ \\ Среда")</span><span class="sxs-lookup"><span data-stu-id="b01eb-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-150">Список параметров конфигурации компьютера.</span><span class="sxs-lookup"><span data-stu-id="b01eb-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="b01eb-151">Переменные среды указывают пути поиска для файлов, каталоги для временных файлов, параметры конкретного приложения и другие аналогичные сведения.</span><span class="sxs-lookup"><span data-stu-id="b01eb-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="b01eb-152">Система поддерживает блок параметров среды для каждого пользователя и один для компьютера.</span><span class="sxs-lookup"><span data-stu-id="b01eb-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="b01eb-153">Блок системной среды представляет переменные среды для всех пользователей определенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="b01eb-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="b01eb-154">Блок среды пользователя представляет переменные среды, которые система поддерживает для конкретного пользователя, и включает набор системных переменных среды.</span><span class="sxs-lookup"><span data-stu-id="b01eb-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="b01eb-155">По умолчанию каждый процесс получает копию блока среды для своего родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="b01eb-156">Как правило, это блок среды для пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="b01eb-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="b01eb-157">Процесс может указывать различные блоки среды для своих дочерних процессов.</span><span class="sxs-lookup"><span data-stu-id="b01eb-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-158">**ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="b01eb-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b01eb-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-161">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error functions \| функцию SetErrorMode")</span><span class="sxs-lookup"><span data-stu-id="b01eb-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-162">На некоторых процессорах, отличных от x86, неправильно выровненные ссылки памяти приводят к возникновению ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="b01eb-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="b01eb-163">Флаг « **без \_ выравнивания \_ \_** » позволяет управлять тем, будет ли операционная система автоматически исправлять такие ошибки выравнивания или сделать их видимыми для приложения.</span><span class="sxs-lookup"><span data-stu-id="b01eb-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="b01eb-164">В миллионах инструкций в секунду для платформы MIPS приложение должно явным образом вызвать [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) с параметром **без \_ выравнивания, \_ \_ Кроме** флага, чтобы операционная система автоматически исправит ошибки выравнивания.</span><span class="sxs-lookup"><span data-stu-id="b01eb-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="b01eb-165">Как операционная система обрабатывает несколько типов серьезных ошибок.</span><span class="sxs-lookup"><span data-stu-id="b01eb-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="b01eb-166">Можно указать, что ошибки процесса операционной системы или приложение может принимать и обрабатывать ошибки.</span><span class="sxs-lookup"><span data-stu-id="b01eb-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="b01eb-167">Значение по умолчанию — для операционной системы, чтобы сделать ошибки выравнивания видимыми для приложения.</span><span class="sxs-lookup"><span data-stu-id="b01eb-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="b01eb-168">Так как платформа x86 не делает ошибки выравнивания видимыми для приложения, неисправность **без \_ выравнивания, \_ \_ Кроме** флага, не позволяет операционной системе выдать ошибку выравнивания, даже если флаг не установлен.</span><span class="sxs-lookup"><span data-stu-id="b01eb-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="b01eb-169">Состояние по умолчанию для [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) — установка всех флагов равным 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="b01eb-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="b01eb-170">(1)</span><span class="sxs-lookup"><span data-stu-id="b01eb-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-171">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b01eb-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="b01eb-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Не пройден \_ Критические \_ ошибки** (2)</span><span class="sxs-lookup"><span data-stu-id="b01eb-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-173">Если этот флаг установлен, операционная система не отображает окно сообщения о критическом обработчике ошибок при возникновении такой ошибки.</span><span class="sxs-lookup"><span data-stu-id="b01eb-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="b01eb-174">Вместо этого операционная система отправляет сообщение об ошибке вызывающему процессу.</span><span class="sxs-lookup"><span data-stu-id="b01eb-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="b01eb-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Нет \_ Ошибка выравнивания, \_ \_ Кроме** (4)</span><span class="sxs-lookup"><span data-stu-id="b01eb-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-176">Если этот флаг установлен, операционная система автоматически исправляет ошибки выравнивания памяти и делает их невидимыми для приложения.</span><span class="sxs-lookup"><span data-stu-id="b01eb-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="b01eb-177">Это делается для вызывающих и подчиненных процессов.</span><span class="sxs-lookup"><span data-stu-id="b01eb-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="b01eb-178">Этот флаг применяется только к ограниченной инструкции SET Computing (RISC) и не влияет на процессоры x86.</span><span class="sxs-lookup"><span data-stu-id="b01eb-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="b01eb-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Нет \_ \_ \_ \_ Поле "ошибка сбоя GP"** (8)</span><span class="sxs-lookup"><span data-stu-id="b01eb-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-180">Если этот флаг установлен, операционная система не отображает окно сообщения об ошибке общей защиты (GP) при возникновении ошибки GP.</span><span class="sxs-lookup"><span data-stu-id="b01eb-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="b01eb-181">Этот флаг следует устанавливать только при отладке приложений, которые обрабатывали ошибки GP.</span><span class="sxs-lookup"><span data-stu-id="b01eb-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="b01eb-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Нет \_ \_ \_ \_ Поле "Ошибка открытия файла"** (16)</span><span class="sxs-lookup"><span data-stu-id="b01eb-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-183">Если этот флаг установлен, операционная система не отображает окно сообщения, если не удается найти файл.</span><span class="sxs-lookup"><span data-stu-id="b01eb-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="b01eb-184">Вместо этого в вызывающий процесс возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="b01eb-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="b01eb-185">Этот флаг в данный момент игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b01eb-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b01eb-186">**филлаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="b01eb-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-189">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двфиллаттрибуте")</span><span class="sxs-lookup"><span data-stu-id="b01eb-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-190">Цвета текста и фона, если в консольном приложении создано новое окно консоли.</span><span class="sxs-lookup"><span data-stu-id="b01eb-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="b01eb-191">Эти значения игнорируются в приложениях графического интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="b01eb-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="b01eb-192">Чтобы указать как цвет переднего плана, так и цвет фона, добавьте значения вместе.</span><span class="sxs-lookup"><span data-stu-id="b01eb-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="b01eb-193">Например, чтобы красный тип (4) был на синем фоне (16), задайте для параметра Филлаттрибуте значение 20.</span><span class="sxs-lookup"><span data-stu-id="b01eb-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="b01eb-194">1</span><span class="sxs-lookup"><span data-stu-id="b01eb-194">1</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-195">Синий цвет переднего плана \_</span><span class="sxs-lookup"><span data-stu-id="b01eb-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-196">2</span><span class="sxs-lookup"><span data-stu-id="b01eb-196">2</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-197">Зеленый передний план \_</span><span class="sxs-lookup"><span data-stu-id="b01eb-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-198">4</span><span class="sxs-lookup"><span data-stu-id="b01eb-198">4</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-199">Красный передний план \_</span><span class="sxs-lookup"><span data-stu-id="b01eb-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-200">8</span><span class="sxs-lookup"><span data-stu-id="b01eb-200">8</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-201">Интенсивность переднего плана \_</span><span class="sxs-lookup"><span data-stu-id="b01eb-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-202">16</span><span class="sxs-lookup"><span data-stu-id="b01eb-202">16</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-203">\_Синий фон</span><span class="sxs-lookup"><span data-stu-id="b01eb-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-204">32</span><span class="sxs-lookup"><span data-stu-id="b01eb-204">32</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-205">\_Зеленый фон</span><span class="sxs-lookup"><span data-stu-id="b01eb-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-206">64</span><span class="sxs-lookup"><span data-stu-id="b01eb-206">64</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-207">\_Красный фон</span><span class="sxs-lookup"><span data-stu-id="b01eb-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-208">128</span><span class="sxs-lookup"><span data-stu-id="b01eb-208">128</span></span>
</dt> <dd>

<span data-ttu-id="b01eb-209">\_Интенсивность фона</span><span class="sxs-lookup"><span data-stu-id="b01eb-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b01eb-210">**PriorityClass значение**</span><span class="sxs-lookup"><span data-stu-id="b01eb-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-211">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-212">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-213">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**жобобжект \_ Basic \_ Limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass значение")</span><span class="sxs-lookup"><span data-stu-id="b01eb-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-214">Класс приоритета нового процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-214">Priority class of the new process.</span></span> <span data-ttu-id="b01eb-215">Это свойство используется для определения приоритетов потоков в процессе.</span><span class="sxs-lookup"><span data-stu-id="b01eb-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="b01eb-216">Если свойство оставлено равным null, класс приоритета по умолчанию имеет значение "Стандартный", если класс приоритета процесса создания не простаивает или не ниже \_ обычного.</span><span class="sxs-lookup"><span data-stu-id="b01eb-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="b01eb-217">В таких случаях дочерний процесс получает класс приоритета по умолчанию для вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="b01eb-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (32)</span><span class="sxs-lookup"><span data-stu-id="b01eb-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-219">Обозначает нормальный процесс без специальных требований к расписанию.</span><span class="sxs-lookup"><span data-stu-id="b01eb-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="b01eb-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Бездействие** (64)</span><span class="sxs-lookup"><span data-stu-id="b01eb-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-221">Обозначает процесс с потоками, которые выполняются только в том случае, когда система бездействует и заменяется потоками любого процесса, запущенного в классе с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b01eb-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="b01eb-222">Примером является экранная заставка.</span><span class="sxs-lookup"><span data-stu-id="b01eb-222">An example is a screen saver.</span></span> <span data-ttu-id="b01eb-223">Класс приоритета простоя наследуется дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="b01eb-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="b01eb-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (128)</span><span class="sxs-lookup"><span data-stu-id="b01eb-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-225">Обозначает процесс, выполняющий критические по времени задачи, которые должны быть выполнены немедленно для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="b01eb-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="b01eb-226">Потоки процесса класса с высоким приоритетом выгружают потоки процессов класса с обычным приоритетом или с приоритетом простоя.</span><span class="sxs-lookup"><span data-stu-id="b01eb-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="b01eb-227">Примером может быть Windows список задач, который должен быстро реагировать при вызове пользователем, независимо от нагрузки на операционную систему.</span><span class="sxs-lookup"><span data-stu-id="b01eb-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="b01eb-228">При использовании класса с высоким приоритетом необходимо соблюдать осторожность, так как приложение класса с высоким приоритетом может использовать почти все доступные циклы.</span><span class="sxs-lookup"><span data-stu-id="b01eb-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="b01eb-229">Для этого уровня задаются только потоки приоритетного прерывания в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="b01eb-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="b01eb-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Реальное** (256)</span><span class="sxs-lookup"><span data-stu-id="b01eb-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-231">Указывает процесс с наибольшим возможным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b01eb-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="b01eb-232">Потоки процесса класса приоритета в реальном времени выгружают потоки всех других процессов, включая потоки с высоким приоритетом и процессы операционной системы, выполняющие важные задачи.</span><span class="sxs-lookup"><span data-stu-id="b01eb-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="b01eb-233">Например, процесс в режиме реального времени, который выполняется в течение более короткого интервала, может привести к тому, что дисковые кэши не будут сбрасываться или заставить мышь не отвечать.</span><span class="sxs-lookup"><span data-stu-id="b01eb-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="b01eb-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ниже \_ Обычная** (16384)</span><span class="sxs-lookup"><span data-stu-id="b01eb-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-235">Указывает процесс с приоритетом выше, чем в режиме простоя, но ниже обычного.</span><span class="sxs-lookup"><span data-stu-id="b01eb-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="b01eb-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Выше \_ Обычная** (32768)</span><span class="sxs-lookup"><span data-stu-id="b01eb-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-237">Указывает процесс с приоритетом выше обычного, но меньше высокого.</span><span class="sxs-lookup"><span data-stu-id="b01eb-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b01eb-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="b01eb-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b01eb-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-240">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-241">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| вшоввиндов")</span><span class="sxs-lookup"><span data-stu-id="b01eb-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-242">Способ отображения окна для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b01eb-242">How the window is displayed to the user.</span></span>

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span data-ttu-id="b01eb-243"><span id="SW_HIDE"></span><span id="sw_hide"></span>**SW \_ СКРЫТЬ** (0)</span><span class="sxs-lookup"><span data-stu-id="b01eb-243"><span id="SW_HIDE"></span><span id="sw_hide"></span>**SW\_HIDE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-244">Скрывает окно и активирует другое окно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-244">Hides the window and activates another window.</span></span>

</dd> <dt>

<span id="SW_NORMAL"></span><span id="sw_normal"></span>

<span data-ttu-id="b01eb-245"><span id="SW_NORMAL"></span><span id="sw_normal"></span>**SW \_ Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="b01eb-245"><span id="SW_NORMAL"></span><span id="sw_normal"></span>**SW\_NORMAL** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-246">Активирует и отображает окно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-246">Activates and displays a window.</span></span> <span data-ttu-id="b01eb-247">Если окно свернется или разворачивается, система восстанавливает исходный размер и расположение.</span><span class="sxs-lookup"><span data-stu-id="b01eb-247">If the window is minimized or maximized, the system restores it to the original size and position.</span></span> <span data-ttu-id="b01eb-248">Приложение задает этот флаг при первом отображении окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-248">An application specifies this flag when displaying the window for the first time.</span></span>

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span data-ttu-id="b01eb-249"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW \_ ШОВМИНИМИЗЕД** (2)</span><span class="sxs-lookup"><span data-stu-id="b01eb-249"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW\_SHOWMINIMIZED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-250">Активирует окно и отображает его в виде уменьшенного окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-250">Activates the window, and displays it as a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span data-ttu-id="b01eb-251"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW \_ ШОВМАКСИМИЗЕД** (3)</span><span class="sxs-lookup"><span data-stu-id="b01eb-251"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW\_SHOWMAXIMIZED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-252">Активирует окно и отображает его как развернутое окно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-252">Activates the window, and displays it as a maximized window.</span></span>

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span data-ttu-id="b01eb-253"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW \_ ШОВНОАКТИВАТЕ** (4)</span><span class="sxs-lookup"><span data-stu-id="b01eb-253"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW\_SHOWNOACTIVATE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-254">Отображает окно в самом последнем размере и положении.</span><span class="sxs-lookup"><span data-stu-id="b01eb-254">Displays a window in its most recent size and position.</span></span> <span data-ttu-id="b01eb-255">Это значение аналогично **\_ стандарту SW**, за исключением того, что окно не активировано.</span><span class="sxs-lookup"><span data-stu-id="b01eb-255">This value is similar to **SW\_NORMAL**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span data-ttu-id="b01eb-256"><span id="SW_SHOW"></span><span id="sw_show"></span>**SW \_ ПОКАЗЫВАТЬ** (5)</span><span class="sxs-lookup"><span data-stu-id="b01eb-256"><span id="SW_SHOW"></span><span id="sw_show"></span>**SW\_SHOW** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-257">Активирует окно и отображает его в текущем размере и позиции.</span><span class="sxs-lookup"><span data-stu-id="b01eb-257">Activates the window, and displays it at the current size and position.</span></span>

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span data-ttu-id="b01eb-258"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW \_ MINIMIZE** (6)</span><span class="sxs-lookup"><span data-stu-id="b01eb-258"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW\_MINIMIZE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-259">Свертывает указанное окно и активирует следующее окно верхнего уровня в Z-порядке.</span><span class="sxs-lookup"><span data-stu-id="b01eb-259">Minimizes the specified window, and activates the next top-level window in the Z order.</span></span>

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span data-ttu-id="b01eb-260"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW \_ ШОВМИННОАКТИВЕ** (7)</span><span class="sxs-lookup"><span data-stu-id="b01eb-260"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW\_SHOWMINNOACTIVE** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-261">Отображает окно в виде уменьшенного окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-261">Displays the window as a minimized window.</span></span> <span data-ttu-id="b01eb-262">Это значение аналогично **SW \_ шовминимзед**, за исключением того, что окно не активировано.</span><span class="sxs-lookup"><span data-stu-id="b01eb-262">This value is similar to **SW\_SHOWMINIMZED**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span data-ttu-id="b01eb-263"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ Показано** (8)</span><span class="sxs-lookup"><span data-stu-id="b01eb-263"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW\_SHOWNA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-264">Отображает окно по текущему размеру и положению.</span><span class="sxs-lookup"><span data-stu-id="b01eb-264">Displays the window at the current size and position.</span></span> <span data-ttu-id="b01eb-265">Это значение аналогично **\_ показу SW**, за исключением того, что окно не активировано.</span><span class="sxs-lookup"><span data-stu-id="b01eb-265">This value is similar to **SW\_SHOW**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span data-ttu-id="b01eb-266"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW \_ Восстановление** (9)</span><span class="sxs-lookup"><span data-stu-id="b01eb-266"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW\_RESTORE** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-267">Активирует и отображает окно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-267">Activates and displays the window.</span></span> <span data-ttu-id="b01eb-268">Если окно свернется или разворачивается, система восстанавливает исходный размер и расположение.</span><span class="sxs-lookup"><span data-stu-id="b01eb-268">If the window is minimized or maximized, the system restores it to the original size and position.</span></span> <span data-ttu-id="b01eb-269">Приложение задает этот флаг при восстановлении окна, которое было уменьшено.</span><span class="sxs-lookup"><span data-stu-id="b01eb-269">An application specifies this flag when restoring a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span data-ttu-id="b01eb-270"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW \_ ШОВДЕФАУЛТ** (10)</span><span class="sxs-lookup"><span data-stu-id="b01eb-270"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW\_SHOWDEFAULT** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-271">Устанавливает состояние отображения на основе значения \**SW \_ \** _, указанного в структуре [_ *стартупинфо* \*](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , передаваемой в функцию [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) программой, запускающей приложение.</span><span class="sxs-lookup"><span data-stu-id="b01eb-271">Sets the show state based on the \**SW\_\** _ value that is specified in the [_ *STARTUPINFO*\*](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure passed to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function by the program that starts the application.</span></span>

</dd> <dt>

<span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>

<span data-ttu-id="b01eb-272"><span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>**SW \_ ФОРЦЕМИНИМИЗЕ** (11)</span><span class="sxs-lookup"><span data-stu-id="b01eb-272"><span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>**SW\_FORCEMINIMIZE** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b01eb-273">Свертывает окно, даже если поток, владеющий окном, перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="b01eb-273">Minimizes a window, even when the thread that owns the window stops responding.</span></span> <span data-ttu-id="b01eb-274">Этот флаг следует использовать только при минимизации Windows из другого потока.</span><span class="sxs-lookup"><span data-stu-id="b01eb-274">Only use this flag when minimizing windows from a different thread.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b01eb-275">**Title**</span><span class="sxs-lookup"><span data-stu-id="b01eb-275">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b01eb-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-277">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-278">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| лптитле")</span><span class="sxs-lookup"><span data-stu-id="b01eb-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-279">Текст, отображаемый в строке заголовка при создании нового окна консоли; используется для процессов консоли.</span><span class="sxs-lookup"><span data-stu-id="b01eb-279">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="b01eb-280">Если **значение равно NULL**, в качестве заголовка окна используется имя исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b01eb-280">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="b01eb-281">Это свойство должно иметь **значение NULL** для графических интерфейсов или консольных процессов, которые не создают новое окно консоли.</span><span class="sxs-lookup"><span data-stu-id="b01eb-281">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-282">**винстатиондесктоп**</span><span class="sxs-lookup"><span data-stu-id="b01eb-282">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b01eb-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-284">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-285">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| лпдесктоп")</span><span class="sxs-lookup"><span data-stu-id="b01eb-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-286">Имя рабочего стола или имя рабочего стола и станции окна для процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-286">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="b01eb-287">Обратная косая черта в строке указывает, что строка включает как настольные, так и оконные станции.</span><span class="sxs-lookup"><span data-stu-id="b01eb-287">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="b01eb-288">Если **винстатиондесктоп** имеет **значение NULL**, новый процесс наследует настольную и оконную станцию своего родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-288">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="b01eb-289">Если **винстатиондесктоп** является пустой строкой, процесс не наследует настольную и оконную станции родительского процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-289">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="b01eb-290">Система определяет, нужно ли создавать новую станцию рабочего стола и Windows.</span><span class="sxs-lookup"><span data-stu-id="b01eb-290">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="b01eb-291">Оконная станция — это защищенный объект, содержащий буфер обмена, набор глобальных атомов и группу объектов настольных систем.</span><span class="sxs-lookup"><span data-stu-id="b01eb-291">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="b01eb-292">Интерактивная экранная станция, назначенная сеансу входа интерактивного пользователя, также содержит клавиатуру, мышь и устройство вывода.</span><span class="sxs-lookup"><span data-stu-id="b01eb-292">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="b01eb-293">Рабочий стол — это защищенный объект, содержащийся на станции Windows.</span><span class="sxs-lookup"><span data-stu-id="b01eb-293">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="b01eb-294">Рабочий стол имеет логическую поверхность отображения и содержит окна, меню и обработчики.</span><span class="sxs-lookup"><span data-stu-id="b01eb-294">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="b01eb-295">Станция окна может иметь несколько настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b01eb-295">A window station can have multiple desktops.</span></span> <span data-ttu-id="b01eb-296">Только рабочие столы интерактивной экранной станции могут быть видимыми и получать вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="b01eb-296">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="b01eb-297">**X**</span><span class="sxs-lookup"><span data-stu-id="b01eb-297">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-298">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-299">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-299">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-300">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двкс")</span><span class="sxs-lookup"><span data-stu-id="b01eb-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-301">Смещение по оси X верхнего левого угла окна при создании нового окна — в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b01eb-301">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="b01eb-302">Смещение находится в левом верхнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="b01eb-302">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="b01eb-303">Для процессов графического пользовательского интерфейса указанная единица используется в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *X* объекта **CreateWindow** имеет значение **\_ уседефаулт во Вт**.</span><span class="sxs-lookup"><span data-stu-id="b01eb-303">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="b01eb-304">\[! Примечание X\]</span><span class="sxs-lookup"><span data-stu-id="b01eb-304">\[!Note  X\]</span></span>  
> <span data-ttu-id="b01eb-305">и **Y** не могут быть указаны независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="b01eb-305">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="b01eb-306">**кскаунтчарс**</span><span class="sxs-lookup"><span data-stu-id="b01eb-306">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-307">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-308">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-308">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-309">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| кскаунтчарс")</span><span class="sxs-lookup"><span data-stu-id="b01eb-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-310">Ширина буфера экрана в символьных столбцах.</span><span class="sxs-lookup"><span data-stu-id="b01eb-310">Screen buffer width in character columns.</span></span> <span data-ttu-id="b01eb-311">Это свойство используется для процессов, которые создают окно консоли и не учитывается в процессах графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-311">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="b01eb-312">**Кскаунтчарс** и **икаунтчарс** нельзя указывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-312">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="b01eb-313">**кссизе**</span><span class="sxs-lookup"><span data-stu-id="b01eb-313">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-314">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-315">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-315">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-316">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двкссизе")</span><span class="sxs-lookup"><span data-stu-id="b01eb-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-317">Ширина окна в пикселях при создании нового окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-317">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="b01eb-318">Для процессов графического пользовательского интерфейса этот метод используется только в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр нвидс **CreateWindow** — **Вт \_ уседефаулт**.</span><span class="sxs-lookup"><span data-stu-id="b01eb-318">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="b01eb-319">**Кссизе** и **исизе** нельзя указывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-319">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="b01eb-320">**да**</span><span class="sxs-lookup"><span data-stu-id="b01eb-320">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-322">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-322">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-323">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| дви")</span><span class="sxs-lookup"><span data-stu-id="b01eb-323">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-324">Смещение в пикселях верхнего левого угла окна при создании нового окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-324">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="b01eb-325">Смещение находится в левом верхнем углу экрана.</span><span class="sxs-lookup"><span data-stu-id="b01eb-325">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="b01eb-326">Для процессов графического пользовательского интерфейса указанная единица используется в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *y* объекта **CreateWindow** имеет значение **\_ уседефаулт во Вт**.</span><span class="sxs-lookup"><span data-stu-id="b01eb-326">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="b01eb-327">\[! Примечание X\]</span><span class="sxs-lookup"><span data-stu-id="b01eb-327">\[!Note  X\]</span></span>  
> <span data-ttu-id="b01eb-328">и **Y** не могут быть указаны независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="b01eb-328">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="b01eb-329">**икаунтчарс**</span><span class="sxs-lookup"><span data-stu-id="b01eb-329">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-330">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-331">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-331">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-332">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| икаунтчарс")</span><span class="sxs-lookup"><span data-stu-id="b01eb-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-333">Высота буфера экрана в строках символов.</span><span class="sxs-lookup"><span data-stu-id="b01eb-333">Screen buffer height in character rows.</span></span> <span data-ttu-id="b01eb-334">Это свойство используется для процессов, которые создают окно консоли, но игнорируется в процессах графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-334">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="b01eb-335">**Кскаунтчарс** и **икаунтчарс** нельзя указывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-335">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="b01eb-336">**исизе**</span><span class="sxs-lookup"><span data-stu-id="b01eb-336">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b01eb-337">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-338">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b01eb-338">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b01eb-339">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двисизе")</span><span class="sxs-lookup"><span data-stu-id="b01eb-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="b01eb-340">Высота окна в пикселях при создании нового окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-340">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="b01eb-341">Для процессов графического пользовательского интерфейса этот метод используется только в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *Нвидс* **CreateWindow** — **Вт \_ уседефаулт**.</span><span class="sxs-lookup"><span data-stu-id="b01eb-341">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="b01eb-342">**Кссизе** и **исизе** нельзя указывать отдельно.</span><span class="sxs-lookup"><span data-stu-id="b01eb-342">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b01eb-343">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b01eb-343">Remarks</span></span>

<span data-ttu-id="b01eb-344">Этот класс является производным от [**Win32 \_ месодпараметеркласс**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="b01eb-344">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="b01eb-345">Обзор</span><span class="sxs-lookup"><span data-stu-id="b01eb-345">Overview</span></span>

<span data-ttu-id="b01eb-346">Метод [**Win32 \_ Process**](win32-process.md) [**CREATE**](create-method-in-class-win32-process.md) позволяет настроить параметры запуска для любого нового процесса, выполняемого на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b01eb-346">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="b01eb-347">Например, можно настроить процесс, чтобы он начинался в скрытом окне, что не позволит пользователю видеть и, возможно, прерывать его.</span><span class="sxs-lookup"><span data-stu-id="b01eb-347">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="b01eb-348">Если процесс выполняется в окне командной строки, можно настроить размер, заголовок и цвет переднего плана и фона окна.</span><span class="sxs-lookup"><span data-stu-id="b01eb-348">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="b01eb-349">Параметры запуска настраиваются с помощью класса **Win32 \_ процессстартуп** .</span><span class="sxs-lookup"><span data-stu-id="b01eb-349">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="b01eb-350">**Win32 \_ Процессстартуп** является классом типа метода; класс типа метода существует только для передачи информации в метод.</span><span class="sxs-lookup"><span data-stu-id="b01eb-350">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="b01eb-351">В этом случае все свойства экземпляра **Win32 \_ процессстартуп** передаются в экземпляр [**\_ процесса Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="b01eb-351">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="b01eb-352">**Использование Win32 \_ процессстартуп**</span><span class="sxs-lookup"><span data-stu-id="b01eb-352">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="b01eb-353">Создайте экземпляр **Win32 \_ процессстартуп**.</span><span class="sxs-lookup"><span data-stu-id="b01eb-353">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="b01eb-354">Настройте свойства нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b01eb-354">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="b01eb-355">Включите экземпляр как часть метода [**\_ процесса Win32**](win32-process.md) Create.</span><span class="sxs-lookup"><span data-stu-id="b01eb-355">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="b01eb-356">Например, если вы создали экземпляр **Win32 \_ процессстартуп** с именем обжконфиг, имя объекта необходимо передать в метод Create следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b01eb-356">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="b01eb-357">Примеры</span><span class="sxs-lookup"><span data-stu-id="b01eb-357">Examples</span></span>

<span data-ttu-id="b01eb-358">Для настройки различных параметров запуска процесса можно использовать класс **Win32 \_ процессстартуп** .</span><span class="sxs-lookup"><span data-stu-id="b01eb-358">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="b01eb-359">Эти параметры включают, но не ограничиваются, такие вещи, как создание процесса в скрытом окне и создание процесса с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b01eb-359">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="b01eb-360">Следующий сценарий VBScript создает процесс в скрытом окне.</span><span class="sxs-lookup"><span data-stu-id="b01eb-360">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="b01eb-361">Следующий сценарий VBScript создает процесс с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b01eb-361">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="b01eb-362">В следующем примере кода VBScript создается процесс «блокнот» на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b01eb-362">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="b01eb-363">**Win32 \_ Процессстартуп** используется для настройки параметров процесса.</span><span class="sxs-lookup"><span data-stu-id="b01eb-363">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="b01eb-364">Требования</span><span class="sxs-lookup"><span data-stu-id="b01eb-364">Requirements</span></span>



| <span data-ttu-id="b01eb-365">Требование</span><span class="sxs-lookup"><span data-stu-id="b01eb-365">Requirement</span></span> | <span data-ttu-id="b01eb-366">Значение</span><span class="sxs-lookup"><span data-stu-id="b01eb-366">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01eb-367">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b01eb-367">Minimum supported client</span></span><br/> | <span data-ttu-id="b01eb-368">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b01eb-368">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b01eb-369">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b01eb-369">Minimum supported server</span></span><br/> | <span data-ttu-id="b01eb-370">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b01eb-370">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b01eb-371">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b01eb-371">Namespace</span></span><br/>                | <span data-ttu-id="b01eb-372">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b01eb-372">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b01eb-373">MOF</span><span class="sxs-lookup"><span data-stu-id="b01eb-373">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b01eb-374"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b01eb-374"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b01eb-375">DLL</span><span class="sxs-lookup"><span data-stu-id="b01eb-375">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b01eb-376"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01eb-376"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b01eb-377">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b01eb-377">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01eb-378">**\_Месодпараметеркласс Win32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-378">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="b01eb-379">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="b01eb-379">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b01eb-380">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="b01eb-380">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="b01eb-381">**\_\_провидерхосткуотаконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="b01eb-381">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b01eb-382">Задачи WMI: процессы</span><span class="sxs-lookup"><span data-stu-id="b01eb-382">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
