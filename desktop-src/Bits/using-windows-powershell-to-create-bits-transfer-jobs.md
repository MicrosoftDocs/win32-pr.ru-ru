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
ms.openlocfilehash: e939342414d62e4e1af0551318dfec0fb9a5ca59a7e310f13de7b6b67b0440cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679896"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Использование Windows PowerShell для создания заданий передачи BITS

Командлеты PowerShell можно использовать для создания синхронных и асинхронных фоновая интеллектуальная служба передачи (BITS) заданий передачи.

Во всех примерах в этом разделе используется командлет [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Чтобы использовать командлет, сначала импортируйте модуль. Чтобы установить модуль, выполните следующую команду: Import-Module BitsTransfer. Для получения дополнительных сведений введите **Get-Help Start-BitsTransfer** в командной строке PowerShell.

> [!IMPORTANT]
>
> при использовании командлетов [ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) из процесса, который выполняется в неинтерактивном контексте, например в службе Windows, может отсутствовать возможность добавления файлов в задания BITS, что может привести к приостановке работы. Для продолжения задания необходимо войти в систему удостоверение, которое использовалось для создания задания перемещения. Например, при создании задания BITS в скрипте PowerShell, который выполнялся как задание планировщик задач, перенос BITS не будет выполнен, если включен параметр задачи планировщик задач "запускать только при входе пользователя в систему".

 

-   [Создание задания синхронной передачи BITS](#to-create-a-synchronous-bits-transfer-job)
-   [Создание задания синхронной передачи BITS с несколькими файлами](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [Создание задания синхронной передачи BITS и указание учетных данных для удаленного сервера](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [Создание задания синхронной передачи BITS из CSV-файла](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [Создание задания асинхронной передачи BITS](#to-create-an-asynchronous-bits-transfer-job)
-   [Управление удаленными сеансами PowerShell](#to-manage-powershell-remote-sessions)
-   [Связанные темы](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>Создание задания синхронной передачи BITS


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.

 

В предыдущем примере локальные и удаленные имена файла указываются в параметрах *источника* и *назначения* соответственно. По завершении передачи файла или при появлении состояния ошибки отображается командная строка.

Тип перемещения по умолчанию — download. При передаче файлов в расположение HTTP параметру *трансфертипе* должно быть присвоено значение upload.

Так как для командлета [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) применяется расположение параметра, для параметров источника и назначения не нужно указывать имена параметров. Поэтому эту команду можно упростить следующим образом.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>Создание задания синхронной передачи BITS с несколькими файлами


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



В предыдущем примере команда [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) создает новое задание передачи BITS. Все файлы добавляются в это задание и последовательно передаются клиенту.

> [!Note]  
> Конечный путь не должен содержать подстановочные знаки. Целевой путь поддерживает относительные каталоги, корневые пути или неявные каталоги (т. е. текущий каталог). Файлы назначения нельзя переименовывать с помощью подстановочных знаков. Кроме того, URL-адреса HTTP и HTTPS не работают с подстановочными знаками. Подстановочные знаки допустимы только для UNC-путей и локальных каталогов.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>Создание задания синхронной передачи BITS и указание учетных данных для удаленного сервера


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



В предыдущем примере пользователь создает задание передачи BITS для загрузки файла с сервера, для которого требуется проверка подлинности. Пользователю предлагается ввести учетные данные, а параметр *Credential* передает объект учетных данных командлету [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Пользователь устанавливает явный прокси-сервер, а задание передачи BITS использует только прокси, определенные параметром *проксилист* . Параметр *DisplayName* дает заданию уникальное отображаемое имя для задания передачи BITS.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>Создание задания синхронной передачи BITS из CSV-файла


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> " \| " — Это символ вертикальной черты.

 

В предыдущем примере пользователь создает задание передачи BITS, которое отправляет несколько файлов с клиента. Командлет [Import-CSV](/previous-versions//dd347665(v=technet.10)) импортирует исходные и конечные расположения файлов и передает их в команду [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) . Команда [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) создает новое задание передачи BITS для каждого файла, добавляет файлы в задание и затем передает их последовательно на сервер.

Содержимое файла Filelist.txt должно быть в следующем формате:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>Создание задания асинхронной передачи BITS


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



В предыдущем примере задание передачи BITS было назначено переменной $Job. Файлы загружаются последовательно. После завершения задания перемещения файлы немедленно становятся доступными. Если $Job. JobState возвращает "передано", объект $Job отправляется в командлет [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .

Если $Job. JobState возвращает "Error", объект $Job отправляется в командлет [Format-List]( /previous-versions//dd347700(v=technet.10)) для вывода списка ошибок.

## <a name="to-manage-powershell-remote-sessions"></a>Управление удаленными сеансами PowerShell

начиная с Windows 10 версии 1607 можно запускать командлеты powershell, битсадмин или другие приложения, использующие [интерфейсы](bits-interfaces.md) BITS из удаленной командной строки powershell, подключенной к другому компьютеру (физическому или виртуальному). Эта возможность недоступна при использовании командной строки [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) для виртуальной машины на том же физическом компьютере и недоступна при использовании командлетов WinRM.

Задание BITS, созданное из удаленного сеанса PowerShell, выполняется в контексте учетной записи пользователя этого сеанса и выполняется только при наличии хотя бы одного активного локального сеанса входа или удаленного сеанса PowerShell, связанного с этой учетной записью пользователя. Вы можете использовать хранимую PSSession PowerShell для выполнения удаленных команд без необходимости открывать окно PowerShell для каждого задания, чтобы продолжить выполнение, как описано в статье [основы PowerShell: удаленное управление](https://techgenix.com/remote-management-powershell-part1/).

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) создает постоянный удаленный сеанс PowerShell. После создания объекты PSSession сохраняются на удаленном компьютере до тех пор, пока они не будут удалены явным образом. Все задания BITS, инициированные в активном сеансе, проводят передачу данных даже после отключения клиента от сеанса.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) отключает клиентский компьютер от удаленного сеанса PowerShell, и состояние сеанса сохраняется на удаленном компьютере. Что более важно, процессы удаленного сеанса будут продолжать выполняться, и задания BITS продолжат выполнение. Клиентский компьютер может даже перезагружаться или отключаться после вызова метода Disconnect-PSSession.
-   [Подключение-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) повторно подключает клиентский компьютер к активному удаленному сеансу PowerShell.
-   [Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) слезами удаленный сеанс PowerShell.

В приведенном ниже примере показано, как использовать Remote PowerShell для работы с асинхронными заданиями передачи BITS, что позволяет продолжить выполнение задания даже в том случае, если вы не подключены к удаленному сеансу.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete — BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
