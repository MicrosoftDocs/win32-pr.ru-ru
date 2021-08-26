---
title: Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS
description: Windows Командлеты PowerShell для удаленного управления могут управлять заданиями передачи фоновая интеллектуальная служба передачи (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f24f4776d8a8431ac8c910fb8145633961bf353721698f8c3e5b4737ee0a1c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004644"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS

Windows Командлеты PowerShell для удаленного управления могут управлять заданиями передачи фоновая интеллектуальная служба передачи (BITS). Дополнительные сведения об удаленном управлении BITS см. в разделе классы поставщиков службы [BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) и поставщика [BITS]( /previous-versions//dd904507(v=vs.85)).

Для следующих примеров требуется [поставщик BITS](/previous-versions/windows/desktop/bitsprov/bits-provider). Поставщик BITS доступен после установки сервера BITS Compact Server. Сведения об установке Compact Server см. в документации по [облегченному серверу BITS](bits-compact-server.md) .

1.  Создайте задание передачи BITS.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    Командлет [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя для подключения к удаленному компьютеру и назначает учетные данные объекту $cred.

    Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) создает задание передачи BITS на компьютере КЛИЕНТ1, создавая экземпляр класса [битсклиентжоб](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) и используя сведения в хэш-таблице, определенной в параметре набора *значений* . Параметр набора *значений* задает сведения, необходимые для заполнения параметров метода [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) . В предыдущем примере пользователь задает для параметра *типа* значение 0 (download). Пользователь также задает имя удаленного и локального файлов для задания загрузки. Дополнительные сведения о создании заданий передачи BITS и подробные сведения о параметрах см. в разделе метод [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .

    Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) присваивает результат переменной $result.

    > [!Note]  
    > Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.

     

2.  Задайте приоритет задания передачи BITS.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    Командлет [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) изменяет приоритет задания передачи BITS на 0 (**\_ \_ \_ передний план задания BG**). Дополнительные сведения об уровнях приоритета см. в разделе Перечисление [**\_ \_ приоритетов заданий BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .

3.  Возобновите задание передачи BITS.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , который устанавливает состояние задания 2 (возобновление задания).

4.  Управление заданием передачи BITS.

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    Предыдущий пример — сценарий для опроса состояния задания и выполнения действия на основе состояния. Возможны следующие действия.

    -   Если $result. Состояние равно 4 (**\_ \_ \_ Ошибка состояния задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и отменяет задание.
    -   Если $result. Состояние равно 5 (**\_ \_ \_ временная \_ Ошибка состояния задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и отменяет задание.
    -   Если $result. Состояние равно 6 (**\_ \_ \_ передано состояние задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и устанавливает для состояния значение Complete.

    Дополнительные сведения о состояниях заданий см. в разделе Перечисление [**\_ \_ состояний заданий BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
