---
description: WinMgmt — это служба WMI в процессе SVCHOST, выполняемая в &\# 0034; \#Учетная запись LocalSystem&0034;.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: инициирует
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703111"
---
# <a name="winmgmt"></a><span data-ttu-id="87d80-103">инициирует</span><span class="sxs-lookup"><span data-stu-id="87d80-103">winmgmt</span></span>

<span data-ttu-id="87d80-104">WinMgmt — это служба WMI в рамках процесса SVCHOST, работающего под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="87d80-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="87d80-105">Во всех случаях служба WMI автоматически запускается, когда первое приложение или сценарий управления запрашивают соединение с пространством имен WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="87d80-106">Дополнительные сведения см. в статье [Запуск и остановка службы WMI](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="87d80-107">WMI — это основной компонент операционной системы Windows, позволяющий разработчикам и ИТ-администраторам создавать сценарии и приложения для автоматизации определенных задач.</span><span class="sxs-lookup"><span data-stu-id="87d80-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="87d80-108">Winmgmt.exe — это служба, которая позволяет инструментарию WMI запускаться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87d80-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="87d80-109">Дополнительные сведения об использовании инструментария WMI см. в разделе [Использование WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="87d80-110">Если вы получили сообщение об ошибке, касающееся winmgmt.exe, см. раздел [Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="87d80-111">Дополнительные сведения о Winmgmt.exe см. в разделе [использование средств управления WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="87d80-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="87d80-112">При запуске из командной строки служба WMI имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="87d80-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="87d80-113">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="87d80-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="87d80-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/баккуп\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="87d80-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="87d80-115">Заставляет Инструментарий WMI создать резервную копию репозитория по указанному имени файла.</span><span class="sxs-lookup"><span data-stu-id="87d80-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="87d80-116">Аргумент *filename* должен содержать полный путь к расположению файла.</span><span class="sxs-lookup"><span data-stu-id="87d80-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="87d80-117">Для этого процесса требуется блокировка записи в репозитории, чтобы операции записи в репозиторий приостанавливаются до завершения процесса резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="87d80-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="87d80-118">Если путь к файлу не указан, он помещается в каталог% WINDIR% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="87d80-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/RESTORE** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="87d80-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="87d80-120">Вручную восстанавливает репозиторий WMI из указанного файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="87d80-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="87d80-121">Аргумент *filename* должен содержать полный путь к расположению файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="87d80-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="87d80-122">Для выполнения операции восстановления Инструментарий WMI сохраняет существующий репозиторий для обратной записи в случае сбоя операции.</span><span class="sxs-lookup"><span data-stu-id="87d80-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="87d80-123">Затем репозиторий восстанавливается из файла резервной копии, указанного в аргументе *filename* .</span><span class="sxs-lookup"><span data-stu-id="87d80-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="87d80-124">Если не удается достичь монопольного доступа к репозиторию, существующие клиенты отключаются от WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="87d80-125">Аргумент *флага* должен быть равен 1 (принудительно отключать пользователей и восстанавливать) или 0 (восстановление по умолчанию, если пользователи не подключены) и указывает режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="87d80-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/ресинкперф** *<Winmgmt-Service-process-ID>*</span><span class="sxs-lookup"><span data-stu-id="87d80-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="87d80-127">Регистрирует библиотеки производительности компьютера с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="87d80-128">WMI PID — это идентификатор процесса для службы WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="87d80-129">Требуется только в том случае, если классы системного монитора не возвращают надежные результаты.</span><span class="sxs-lookup"><span data-stu-id="87d80-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/стандалонехост**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="87d80-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="87d80-131">Перемещает службу Winmgmt в автономный процесс svchost с фиксированной конечной точкой DCOM.</span><span class="sxs-lookup"><span data-stu-id="87d80-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="87d80-132">Конечная точка по умолчанию — "нкакн \_ IP \_ TCP. 0.24158".</span><span class="sxs-lookup"><span data-stu-id="87d80-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="87d80-133">Однако конечную точку можно изменить, запустив Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="87d80-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="87d80-134">Дополнительные сведения о настройке фиксированного порта для WMI см. в разделе [Настройка фиксированного порта для WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="87d80-135">Аргумент *Level* — это уровень проверки подлинности для процесса Svchost.</span><span class="sxs-lookup"><span data-stu-id="87d80-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="87d80-136">WMI обычно работает как часть узла общей службы, и вы не можете увеличить уровень проверки подлинности только для WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="87d80-137">Если параметр *Level* не указан, по умолчанию используется значение 4 (**RPC \_ C \_ AUTHN \_ Level \_ PKT** или **вбемаусентикатионлевелпкт**).</span><span class="sxs-lookup"><span data-stu-id="87d80-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="87d80-138">Вы можете более безопасно запускать Инструментарий WMI, увеличивая уровень проверки подлинности до уровня конфиденциальности пакетов (**RPC \_ C \_ AUTHN на \_ уровне \_ \_ безопасности PKT** или **вбемаусентикатионлевелпктприваци**).</span><span class="sxs-lookup"><span data-stu-id="87d80-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="87d80-139">Уровни проверки подлинности для Visual Basic и сценариев описаны в разделе [**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="87d80-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="87d80-140">Сведения о C++ см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью c++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="87d80-141">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="87d80-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/шаредхост**</span><span class="sxs-lookup"><span data-stu-id="87d80-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="87d80-143">Перемещает службу Winmgmt в общий процесс svchost.</span><span class="sxs-lookup"><span data-stu-id="87d80-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/верифирепоситори\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="87d80-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="87d80-145">Выполняет проверку согласованности в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="87d80-146">При добавлении параметра **/верифирепоситори** без *<path>* аргумента проверяется текущий репозиторий, используемый WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="87d80-147">При указании аргумента *path* можно проверить все сохраненные копии репозитория.</span><span class="sxs-lookup"><span data-stu-id="87d80-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="87d80-148">В этом случае аргумент path должен содержать полный путь к сохраненной копии репозитория.</span><span class="sxs-lookup"><span data-stu-id="87d80-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="87d80-149">Сохраненный репозиторий должен быть копией всей папки репозитория.</span><span class="sxs-lookup"><span data-stu-id="87d80-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="87d80-150">Дополнительные сведения об ошибках, возвращаемых этой командой, см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="87d80-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/салважерепоситори**</span><span class="sxs-lookup"><span data-stu-id="87d80-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="87d80-152">Выполняет проверку согласованности в репозитории WMI и при обнаружении несогласованности перестраивает репозиторий.</span><span class="sxs-lookup"><span data-stu-id="87d80-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="87d80-153">Содержимое несогласованного репозитория объединяется в перестроенный репозиторий, если его можно считать.</span><span class="sxs-lookup"><span data-stu-id="87d80-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="87d80-154">Операция восстановления всегда работает с репозиторием, который в настоящее время использует служба WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="87d80-155">Дополнительные сведения об ошибках, возвращаемых этой командой, см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="87d80-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="87d80-156">% MOF-файлов, содержащих инструкцию препроцессора [**\# pragma автовосстановления**](pragma-autorecover.md) , восстанавливается в репозитории.</span><span class="sxs-lookup"><span data-stu-id="87d80-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="87d80-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/ресетрепоситори**</span><span class="sxs-lookup"><span data-stu-id="87d80-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="87d80-158">При первой установке операционной системы репозиторий сбрасывается в первоначальное состояние.</span><span class="sxs-lookup"><span data-stu-id="87d80-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="87d80-159">В репозиторий будут восстановлены MOF-файлы, содержащие инструкцию препроцессора [**\# pragma автовосстановления**](pragma-autorecover.md) .</span><span class="sxs-lookup"><span data-stu-id="87d80-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87d80-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87d80-160">Remarks</span></span>

<span data-ttu-id="87d80-161">Это средство находится в каталоге% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="87d80-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="87d80-162">Для вывода списка доступных параметров введите `WinMgmt /?` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="87d80-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="87d80-163">Репозиторий WMI, также известный как репозиторий CIM, не просто является отдельным файлом, а коллекцией файлов в папке репозитория, которые работают вместе в качестве базы данных.</span><span class="sxs-lookup"><span data-stu-id="87d80-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="87d80-164">При использовании параметра **/баккуп** для резервного копирования репозитория результирующая резервная копия представляет собой один сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="87d80-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="87d80-165">Инструментарий WMI возвращает **ошибку \_ внутренней \_ базы \_ данных** (net helpmsg 1358), если операция проверки указывает, что репозиторий находится в несогласованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="87d80-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="87d80-166">Эта ошибка может быть возвращена любой командой, выполняющей проверку репозитория, например **/верифирепоситори** или **/салважерепоситори**.</span><span class="sxs-lookup"><span data-stu-id="87d80-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="87d80-167">Если инструментарий WMI возвращает сообщения об ошибках, имейте в виду, что они могут не указывать на проблемы в службе WMI или в поставщиках WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="87d80-168">Сбои могут исходить из других частей операционной системы и возникать как ошибки через инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="87d80-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="87d80-169">При любых обстоятельствах не удаляйте репозиторий WMI как первое действие, поскольку удаление репозитория может привести к повреждению системы или установке приложений.</span><span class="sxs-lookup"><span data-stu-id="87d80-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="87d80-170">Чтобы получить дополнительные сведения об источнике проблемы, скачайте и запустите программу командной строки для диагностики [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="87d80-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="87d80-171">Это средство создает отчет, который обычно может изолировать источник проблемы и предоставить инструкции по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="87d80-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="87d80-172">Этот отчет также помогает в работе со службой поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="87d80-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="87d80-173">Вы можете скачать [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="87d80-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87d80-174">Требования</span><span class="sxs-lookup"><span data-stu-id="87d80-174">Requirements</span></span>



| <span data-ttu-id="87d80-175">Требование</span><span class="sxs-lookup"><span data-stu-id="87d80-175">Requirement</span></span> | <span data-ttu-id="87d80-176">Значение</span><span class="sxs-lookup"><span data-stu-id="87d80-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="87d80-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87d80-177">Minimum supported client</span></span><br/> | <span data-ttu-id="87d80-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87d80-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="87d80-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87d80-179">Minimum supported server</span></span><br/> | <span data-ttu-id="87d80-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87d80-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87d80-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87d80-181">See also</span></span>

<dl> <dt>

<span data-ttu-id="87d80-182">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="87d80-182">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="87d80-183">Удаленное подключение к WMI, начиная с Vista</span><span class="sxs-lookup"><span data-stu-id="87d80-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

