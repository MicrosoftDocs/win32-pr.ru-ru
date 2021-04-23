---
title: Использование BITS
description: Использование BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Фоновая интеллектуальная служба передачи
- Фоновая интеллектуальная служба передачи, задачи
- БИТЫ передачи файлов
- Использование битов BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654343"
---
# <a name="using-bits"></a><span data-ttu-id="2a5c8-107">Использование BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-107">Using BITS</span></span>

<span data-ttu-id="2a5c8-108">Ниже показано, как выполнить перенос файлов с помощью  [интерфейсов](bits-interfaces.md)ФОНОВАЯ интеллектуальная служба передачи (BITS).</span><span class="sxs-lookup"><span data-stu-id="2a5c8-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="2a5c8-109">**Выполнение обмена файлами**</span><span class="sxs-lookup"><span data-stu-id="2a5c8-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="2a5c8-110">Подключение к службе BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="2a5c8-111">Создание задания перемещения</span><span class="sxs-lookup"><span data-stu-id="2a5c8-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="2a5c8-112">Добавление файлов в задание</span><span class="sxs-lookup"><span data-stu-id="2a5c8-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="2a5c8-113">Запустите задание</span><span class="sxs-lookup"><span data-stu-id="2a5c8-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="2a5c8-114">Определение успешной передачи файлов службой BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="2a5c8-115">Завершение задания</span><span class="sxs-lookup"><span data-stu-id="2a5c8-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="2a5c8-116">На предыдущих шагах показано, как передавать файлы, используя значения свойств по умолчанию для задания.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="2a5c8-117">Поведение по умолчанию можно изменить, изменив одно или несколько значений свойств задания.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="2a5c8-118">Например, можно изменить приоритет обработки задания относительно других заданий в очереди, указать свой собственный параметр прокси-сервера и зарегистрироваться для получения уведомления о событии при передаче файлов службой BITS.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="2a5c8-119">Дополнительные сведения см. [в разделе Установка и получение свойств задания](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="2a5c8-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="2a5c8-120">Windows PowerShell предоставляет простой механизм управления множеством задач BITS.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="2a5c8-121">Этот раздел содержит следующие разделы, в которых показано, как использовать командлеты Windows PowerShell с BITS.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="2a5c8-122">Использование Windows PowerShell для создания заданий передачи BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="2a5c8-123">Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="2a5c8-124">Использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="2a5c8-125">Начиная с Windows 10 версии 1607 можно также запускать командлеты PowerShell и использовать Битсадмин или другие приложения, использующие [интерфейсы](bits-interfaces.md) BITS из удаленной командной строки PowerShell, подключенной к другому компьютеру (физическому или виртуальному).</span><span class="sxs-lookup"><span data-stu-id="2a5c8-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="2a5c8-126">Эта возможность недоступна при использовании командной строки [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) для виртуальной машины на том же физическом компьютере и недоступна при использовании командлетов WinRM.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="2a5c8-127">Задание BITS, созданное на основе удаленного сеанса PowerShell, будет выполняться в контексте учетной записи пользователя этого сеанса и будет работать только при наличии хотя бы одного активного локального сеанса входа или удаленного сеанса PowerShell, связанного с этой учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a5c8-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="2a5c8-128">Дополнительные сведения см. [в разделе Управление удаленными сеансами PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="2a5c8-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="2a5c8-129">Этот раздел также содержит следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="2a5c8-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="2a5c8-130">Рекомендации по использованию BITS</span><span class="sxs-lookup"><span data-stu-id="2a5c8-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="2a5c8-131">Перечисление заданий в очереди на перемещение</span><span class="sxs-lookup"><span data-stu-id="2a5c8-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="2a5c8-132">Перечисление файлов в задании</span><span class="sxs-lookup"><span data-stu-id="2a5c8-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="2a5c8-133">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="2a5c8-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="2a5c8-134">Получение ответа из задания отправки и ответа</span><span class="sxs-lookup"><span data-stu-id="2a5c8-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="2a5c8-135">Пример кода, в котором используются интерфейсы BITS, см. в разделе [примеры и средства BITS](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2a5c8-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 