---
title: Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS
description: Служба удаленного управления Windows командлеты PowerShell могут управлять заданиями передачи фоновая интеллектуальная служба передачи (BITS).
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538987"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="f656e-103">Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS</span><span class="sxs-lookup"><span data-stu-id="f656e-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="f656e-104">Служба удаленного управления Windows командлеты PowerShell могут управлять заданиями передачи фоновая интеллектуальная служба передачи (BITS).</span><span class="sxs-lookup"><span data-stu-id="f656e-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="f656e-105">Дополнительные сведения об удаленном управлении BITS см. в разделе классы поставщиков службы [BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) и поставщика [BITS]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f656e-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="f656e-106">Для следующих примеров требуется [поставщик BITS](/previous-versions/windows/desktop/bitsprov/bits-provider).</span><span class="sxs-lookup"><span data-stu-id="f656e-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="f656e-107">Поставщик BITS доступен после установки сервера BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="f656e-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="f656e-108">Сведения об установке Compact Server см. в документации по [облегченному серверу BITS](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="f656e-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="f656e-109">Создайте задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="f656e-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="f656e-110">Командлет [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя для подключения к удаленному компьютеру и назначает учетные данные объекту $cred.</span><span class="sxs-lookup"><span data-stu-id="f656e-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="f656e-111">Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) создает задание передачи BITS на компьютере КЛИЕНТ1, создавая экземпляр класса [битсклиентжоб](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) и используя сведения в хэш-таблице, определенной в параметре набора *значений* .</span><span class="sxs-lookup"><span data-stu-id="f656e-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="f656e-112">Параметр набора *значений* задает сведения, необходимые для заполнения параметров метода [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="f656e-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="f656e-113">В предыдущем примере пользователь задает для параметра *типа* значение 0 (download).</span><span class="sxs-lookup"><span data-stu-id="f656e-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="f656e-114">Пользователь также задает имя удаленного и локального файлов для задания загрузки.</span><span class="sxs-lookup"><span data-stu-id="f656e-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="f656e-115">Дополнительные сведения о создании заданий передачи BITS и подробные сведения о параметрах см. в разделе метод [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) .</span><span class="sxs-lookup"><span data-stu-id="f656e-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="f656e-116">Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) присваивает результат переменной $result.</span><span class="sxs-lookup"><span data-stu-id="f656e-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="f656e-117">Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="f656e-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="f656e-118">Задайте приоритет задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="f656e-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="f656e-119">Командлет [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) изменяет приоритет задания передачи BITS на 0 (**\_ \_ \_ передний план задания BG**).</span><span class="sxs-lookup"><span data-stu-id="f656e-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="f656e-120">Дополнительные сведения об уровнях приоритета см. в разделе Перечисление [**\_ \_ приоритетов заданий BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) .</span><span class="sxs-lookup"><span data-stu-id="f656e-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="f656e-121">Возобновите задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="f656e-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="f656e-122">Командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) , который устанавливает состояние задания 2 (возобновление задания).</span><span class="sxs-lookup"><span data-stu-id="f656e-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="f656e-123">Управление заданием передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="f656e-123">Manage the BITS transfer job.</span></span>

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

    

    <span data-ttu-id="f656e-124">Предыдущий пример — сценарий для опроса состояния задания и выполнения действия на основе состояния.</span><span class="sxs-lookup"><span data-stu-id="f656e-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="f656e-125">Возможны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f656e-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="f656e-126">Если $result. Состояние равно 4 (**\_ \_ \_ Ошибка состояния задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="f656e-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="f656e-127">Если $result. Состояние равно 5 (**\_ \_ \_ временная \_ Ошибка состояния задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="f656e-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="f656e-128">Если $result. Состояние равно 6 (**\_ \_ \_ передано состояние задания BG**), командлет [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) вызывает метод [сетжобстате](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) и устанавливает для состояния значение Complete.</span><span class="sxs-lookup"><span data-stu-id="f656e-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="f656e-129">Дополнительные сведения о состояниях заданий см. в разделе Перечисление [**\_ \_ состояний заданий BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) .</span><span class="sxs-lookup"><span data-stu-id="f656e-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f656e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f656e-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f656e-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="f656e-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="f656e-132">Invoke-WsmanAction</span><span class="sxs-lookup"><span data-stu-id="f656e-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="f656e-133">Set-WsmanInstance</span><span class="sxs-lookup"><span data-stu-id="f656e-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
