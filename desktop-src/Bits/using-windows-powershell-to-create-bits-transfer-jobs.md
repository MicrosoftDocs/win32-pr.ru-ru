---
title: Использование Windows PowerShell для создания заданий передачи BITS
description: Командлеты PowerShell можно использовать для создания синхронных и асинхронных фоновая интеллектуальная служба передачи (BITS) заданий передачи.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807529"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="71a80-103">Использование Windows PowerShell для создания заданий передачи BITS</span><span class="sxs-lookup"><span data-stu-id="71a80-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="71a80-104">Командлеты PowerShell можно использовать для создания синхронных и асинхронных фоновая интеллектуальная служба передачи (BITS) заданий передачи.</span><span class="sxs-lookup"><span data-stu-id="71a80-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="71a80-105">Во всех примерах в этом разделе используется командлет [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="71a80-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="71a80-106">Чтобы использовать командлет, сначала импортируйте модуль.</span><span class="sxs-lookup"><span data-stu-id="71a80-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="71a80-107">Чтобы установить модуль, выполните следующую команду: Import-Module BitsTransfer.</span><span class="sxs-lookup"><span data-stu-id="71a80-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="71a80-108">Для получения дополнительных сведений введите **Get-Help Start-BitsTransfer** в командной строке PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71a80-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="71a80-109">При использовании командлетов [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) из процесса, который выполняется в неинтерактивном контексте, например в службе Windows, возможно, не удастся добавить файлы в задания BITS, что может привести к приостановке работы.</span><span class="sxs-lookup"><span data-stu-id="71a80-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="71a80-110">Для продолжения задания необходимо войти в систему удостоверение, которое использовалось для создания задания перемещения.</span><span class="sxs-lookup"><span data-stu-id="71a80-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="71a80-111">Например, при создании задания BITS в скрипте PowerShell, который выполнялся как задание планировщик задач, перенос BITS не будет выполнен, если включен параметр задачи планировщик задач "запускать только при входе пользователя в систему".</span><span class="sxs-lookup"><span data-stu-id="71a80-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="71a80-112">Создание задания синхронной передачи BITS</span><span class="sxs-lookup"><span data-stu-id="71a80-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="71a80-113">Создание задания синхронной передачи BITS с несколькими файлами</span><span class="sxs-lookup"><span data-stu-id="71a80-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="71a80-114">Создание задания синхронной передачи BITS и указание учетных данных для удаленного сервера</span><span class="sxs-lookup"><span data-stu-id="71a80-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="71a80-115">Создание задания синхронной передачи BITS из CSV-файла</span><span class="sxs-lookup"><span data-stu-id="71a80-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="71a80-116">Создание задания асинхронной передачи BITS</span><span class="sxs-lookup"><span data-stu-id="71a80-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="71a80-117">Управление удаленными сеансами PowerShell</span><span class="sxs-lookup"><span data-stu-id="71a80-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="71a80-118">См. также</span><span class="sxs-lookup"><span data-stu-id="71a80-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="71a80-119">Создание задания синхронной передачи BITS</span><span class="sxs-lookup"><span data-stu-id="71a80-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="71a80-120">Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="71a80-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="71a80-121">В предыдущем примере локальные и удаленные имена файла указываются в параметрах *источника* и *назначения* соответственно.</span><span class="sxs-lookup"><span data-stu-id="71a80-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="71a80-122">По завершении передачи файла или при появлении состояния ошибки отображается командная строка.</span><span class="sxs-lookup"><span data-stu-id="71a80-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="71a80-123">Тип перемещения по умолчанию — download.</span><span class="sxs-lookup"><span data-stu-id="71a80-123">The default transfer type is Download.</span></span> <span data-ttu-id="71a80-124">При передаче файлов в расположение HTTP для параметра *трансфертипе* необходимо задать значение upload.</span><span class="sxs-lookup"><span data-stu-id="71a80-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="71a80-125">Так как для командлета [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) применяется расположение параметра, для параметров источника и назначения не нужно указывать имена параметров.</span><span class="sxs-lookup"><span data-stu-id="71a80-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="71a80-126">Поэтому эту команду можно упростить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="71a80-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="71a80-127">Создание задания синхронной передачи BITS с несколькими файлами</span><span class="sxs-lookup"><span data-stu-id="71a80-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="71a80-128">В предыдущем примере команда [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) создает новое задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="71a80-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="71a80-129">Все файлы добавляются в это задание и последовательно передаются клиенту.</span><span class="sxs-lookup"><span data-stu-id="71a80-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="71a80-130">Конечный путь не должен содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="71a80-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="71a80-131">Целевой путь поддерживает относительные каталоги, корневые пути или неявные каталоги (т. е. текущий каталог).</span><span class="sxs-lookup"><span data-stu-id="71a80-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="71a80-132">Файлы назначения нельзя переименовывать с помощью подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="71a80-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="71a80-133">Кроме того, URL-адреса HTTP и HTTPS не работают с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="71a80-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="71a80-134">Подстановочные знаки допустимы только для UNC-путей и локальных каталогов.</span><span class="sxs-lookup"><span data-stu-id="71a80-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="71a80-135">Создание задания синхронной передачи BITS и указание учетных данных для удаленного сервера</span><span class="sxs-lookup"><span data-stu-id="71a80-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="71a80-136">В предыдущем примере пользователь создает задание передачи BITS для загрузки файла с сервера, для которого требуется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="71a80-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="71a80-137">Пользователю предлагается ввести учетные данные, а параметр *Credential* передает объект учетных данных командлету [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="71a80-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="71a80-138">Пользователь устанавливает явный прокси-сервер, а задание передачи BITS использует только прокси, определенные параметром *проксилист* .</span><span class="sxs-lookup"><span data-stu-id="71a80-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="71a80-139">Параметр *DisplayName* дает заданию уникальное отображаемое имя для задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="71a80-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="71a80-140">Создание задания синхронной передачи BITS из CSV-файла</span><span class="sxs-lookup"><span data-stu-id="71a80-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="71a80-141">" \| " — Это символ вертикальной черты.</span><span class="sxs-lookup"><span data-stu-id="71a80-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="71a80-142">В предыдущем примере пользователь создает задание передачи BITS, которое отправляет несколько файлов с клиента.</span><span class="sxs-lookup"><span data-stu-id="71a80-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="71a80-143">Командлет [Import-CSV](/previous-versions//dd347665(v=technet.10)) импортирует исходные и конечные расположения файлов и передает их в команду [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="71a80-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="71a80-144">Команда [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) создает новое задание передачи BITS для каждого файла, добавляет файлы в задание и затем передает их последовательно на сервер.</span><span class="sxs-lookup"><span data-stu-id="71a80-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="71a80-145">Содержимое файла Filelist.txt должно быть в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="71a80-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="71a80-146">Создание задания асинхронной передачи BITS</span><span class="sxs-lookup"><span data-stu-id="71a80-146">To create an asynchronous BITS transfer job</span></span>


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



<span data-ttu-id="71a80-147">В предыдущем примере задание передачи BITS было назначено переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="71a80-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="71a80-148">Файлы загружаются последовательно.</span><span class="sxs-lookup"><span data-stu-id="71a80-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="71a80-149">После завершения задания перемещения файлы немедленно становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="71a80-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="71a80-150">Если $Job. JobState возвращает "передано", объект $Job отправляется в командлет [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="71a80-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="71a80-151">Если $Job. JobState возвращает "Error", объект $Job отправляется в командлет [Format-List]( /previous-versions//dd347700(v=technet.10)) для вывода списка ошибок.</span><span class="sxs-lookup"><span data-stu-id="71a80-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="71a80-152">Управление удаленными сеансами PowerShell</span><span class="sxs-lookup"><span data-stu-id="71a80-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="71a80-153">Начиная с Windows 10 версии 1607 можно запускать командлеты PowerShell, Битсадмин или другие приложения, использующие [интерфейсы](bits-interfaces.md) BITS из удаленной командной строки PowerShell, подключенной к другому компьютеру (физическому или виртуальному).</span><span class="sxs-lookup"><span data-stu-id="71a80-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="71a80-154">Эта возможность недоступна при использовании командной строки [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) для виртуальной машины на том же физическом компьютере и недоступна при использовании командлетов WinRM.</span><span class="sxs-lookup"><span data-stu-id="71a80-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="71a80-155">Задание BITS, созданное из удаленного сеанса PowerShell, выполняется в контексте учетной записи пользователя этого сеанса и выполняется только при наличии хотя бы одного активного локального сеанса входа или удаленного сеанса PowerShell, связанного с этой учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="71a80-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="71a80-156">Вы можете использовать хранимую PSSession PowerShell для выполнения удаленных команд без необходимости открывать окно PowerShell для каждого задания, чтобы продолжить выполнение, как описано в статье [основы PowerShell: удаленное управление](https://techgenix.com/remote-management-powershell-part1/).</span><span class="sxs-lookup"><span data-stu-id="71a80-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="71a80-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) создает постоянный удаленный сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71a80-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="71a80-158">После создания объекты PSSession сохраняются на удаленном компьютере до тех пор, пока они не будут удалены явным образом.</span><span class="sxs-lookup"><span data-stu-id="71a80-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="71a80-159">Все задания BITS, инициированные в активном сеансе, проводят передачу данных даже после отключения клиента от сеанса.</span><span class="sxs-lookup"><span data-stu-id="71a80-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="71a80-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) отключает клиентский компьютер от удаленного сеанса PowerShell, и состояние сеанса сохраняется на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="71a80-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="71a80-161">Что более важно, процессы удаленного сеанса будут продолжать выполняться, и задания BITS продолжат выполнение.</span><span class="sxs-lookup"><span data-stu-id="71a80-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="71a80-162">Клиентский компьютер может даже перезагружаться или отключаться после вызова метода Disconnect-PSSession.</span><span class="sxs-lookup"><span data-stu-id="71a80-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="71a80-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) повторно подключает клиентский компьютер к активному удаленному сеансу PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71a80-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="71a80-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) слезами удаленный сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71a80-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="71a80-165">В приведенном ниже примере показано, как использовать Remote PowerShell для работы с асинхронными заданиями передачи BITS, что позволяет продолжить выполнение задания даже в том случае, если вы не подключены к удаленному сеансу.</span><span class="sxs-lookup"><span data-stu-id="71a80-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a><span data-ttu-id="71a80-166">См. также</span><span class="sxs-lookup"><span data-stu-id="71a80-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="71a80-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="71a80-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="71a80-168">[Complete — BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="71a80-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
