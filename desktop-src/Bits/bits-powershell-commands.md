---
title: Справочные материалы по командам BITS PowerShell
description: Фоновая интеллектуальная служба передачи (BITS) 4,0 может использовать командлеты Windows PowerShell для управления заданиями передачи.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bd195d2202849c2bf2df580d159ee401911c51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890873"
---
# <a name="managed-reference-for-bits-powershell-commands"></a><span data-ttu-id="20d32-103">Справочные материалы по командам BITS PowerShell</span><span class="sxs-lookup"><span data-stu-id="20d32-103">Managed Reference for BITS PowerShell Commands</span></span>

<span data-ttu-id="20d32-104">Фоновая интеллектуальная служба передачи (BITS) 4,0 может использовать командлеты Windows PowerShell для создания заданий по загрузке файлов и их передачи и управления ими.</span><span class="sxs-lookup"><span data-stu-id="20d32-104">Background Intelligent Transfer Service (BITS) 4.0 can use Windows PowerShell cmdlets to create and manage file download and upload transfer jobs.</span></span>

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

<span data-ttu-id="20d32-105">Командлеты Windows PowerShell для BITS предоставляют практически те же функции, что и программа командной строки битсадмин.</span><span class="sxs-lookup"><span data-stu-id="20d32-105">Windows PowerShell cmdlets for BITS provide much of the same functionality as the bitsadmin command-line utility.</span></span> <span data-ttu-id="20d32-106">Однако Windows PowerShell также выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="20d32-106">However, Windows PowerShell also does the following:</span></span>

-   <span data-ttu-id="20d32-107">Автоматизирует задачи BITS на расширяемом языке программирования, ориентированном на управление.</span><span class="sxs-lookup"><span data-stu-id="20d32-107">Automates BITS tasks in an extensible and management-oriented scripting language.</span></span>
-   <span data-ttu-id="20d32-108">Предоставляет единый инструмент для всех задач, связанных с заданиями.</span><span class="sxs-lookup"><span data-stu-id="20d32-108">Provides a single tool for all job-related tasks.</span></span>

> [!Note]  
> <span data-ttu-id="20d32-109">Чтобы использовать эти команды, необходимо сначала импортировать модуль PowerShell BITS с помощью `Import-Module BitsTransfer` команды.</span><span class="sxs-lookup"><span data-stu-id="20d32-109">To use these commands, you must first import the BITS PowerShell module, using the `Import-Module BitsTransfer` command.</span></span> <span data-ttu-id="20d32-110">Дополнительные сведения см. в следующей [статье TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="20d32-110">For more information, see the following [TechNet article](/previous-versions/technet-magazine/ff382721(v=msdn.10)).</span></span>

 

<span data-ttu-id="20d32-111">Дополнительные сведения об использовании Windows PowerShell см. в разделе [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="20d32-111">For more information on using Windows Powershell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).</span></span>

## <a name="bits-powershell-classes"></a><span data-ttu-id="20d32-112">Классы PowerShell для BITS</span><span class="sxs-lookup"><span data-stu-id="20d32-112">BITS PowerShell Classes</span></span>

<span data-ttu-id="20d32-113">**Пространство имен**: Microsoft. BackgroundIntelligentTransfer. Management</span><span class="sxs-lookup"><span data-stu-id="20d32-113">**Namespace**: Microsoft.BackgroundIntelligentTransfer.Management</span></span>

<span data-ttu-id="20d32-114">**Сборка**: System. Management. Automation</span><span class="sxs-lookup"><span data-stu-id="20d32-114">**Assembly**: System.Management.Automation</span></span>

<span data-ttu-id="20d32-115">Эти классы команд BITS реализуются Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20d32-115">These BITS command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="20d32-116">Эти классы включены в этот пакет средств разработки программного обеспечения (SDK) только для полноты.</span><span class="sxs-lookup"><span data-stu-id="20d32-116">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="20d32-117">Члены этих классов не могут использоваться напрямую и не должны использоваться для наследования других классов.</span><span class="sxs-lookup"><span data-stu-id="20d32-117">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="20d32-118">Класс</span><span class="sxs-lookup"><span data-stu-id="20d32-118">Class</span></span>                           | <span data-ttu-id="20d32-119">Описание</span><span class="sxs-lookup"><span data-stu-id="20d32-119">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d32-120">**аддбитсфилекомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-120">**AddBitsFileCommand**</span></span>          | <span data-ttu-id="20d32-121">Добавляет один или несколько файлов к существующему заданию передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-121">Adds one or more files to an existing BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-122">Подробные сведения о параметрах и примерах см. в разделе командлет [Add-битсфиле](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-122">See the [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                       |
| <span data-ttu-id="20d32-123">**клеарбитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-123">**ClearBitsTransferCommand**</span></span>    | <span data-ttu-id="20d32-124">Отменяет задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-124">Cancels a BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-125">Подробные сведения о параметрах и примерах см. в разделе командлет [clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-125">See the [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |
| <span data-ttu-id="20d32-126">**комплетебитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-126">**CompleteBitsTransferCommand**</span></span> | <span data-ttu-id="20d32-127">Завершает задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-127">Completes a BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-128">Подробные сведения о параметрах и примерах см. в разделе [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-128">See the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                     |
| <span data-ttu-id="20d32-129">**жетбитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-129">**GetBitsTransferCommand**</span></span>      | <span data-ttu-id="20d32-130">Извлекает связанный объект Битсжоб для существующего задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-130">Retrieves the associated BitsJob object for an existing BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-131">Подробные сведения о параметрах и примерах см. в разделе командлет [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-131">See the [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/> |
| <span data-ttu-id="20d32-132">**невбитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-132">**NewBitsTransferCommand**</span></span>      | <span data-ttu-id="20d32-133">Создает новое задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-133">Creates a new BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-134">Дополнительные сведения о параметрах и примерах см. в разделе командлет [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-134">See the [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                           |
| <span data-ttu-id="20d32-135">**ресумебитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-135">**ResumeBitsTransferCommand**</span></span>   | <span data-ttu-id="20d32-136">Возобновляет задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-136">Resumes a BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-137">Подробные сведения о параметрах и примерах см. в разделе командлет [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-137">See the [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                            |
| <span data-ttu-id="20d32-138">**сетбитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-138">**SetBitsTransferCommand**</span></span>      | <span data-ttu-id="20d32-139">Изменяет свойства существующего задания передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-139">Modifies the properties of an existing BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-140">Дополнительные сведения о параметрах и примерах см. в описании командлета [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-140">See the [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                  |
| <span data-ttu-id="20d32-141">**суспендбитстрансферкомманд**</span><span class="sxs-lookup"><span data-stu-id="20d32-141">**SuspendBitsTransferCommand**</span></span>  | <span data-ttu-id="20d32-142">Приостанавливает задание передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="20d32-142">Suspends a BITS transfer job.</span></span><br/> <span data-ttu-id="20d32-143">Подробные сведения о параметрах и примерах см. в разделе командлет [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="20d32-143">See the [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet for detailed information about the parameters and for examples.</span></span><br/>                                          |



 

 

