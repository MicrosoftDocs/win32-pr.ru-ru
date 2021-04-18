---
description: Управляемый Справочник по классам команд WMI Windows PowerShell
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Управляемый Справочник по классам команд WMI Windows PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693447"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="6fcab-103">Управляемый Справочник по классам команд WMI Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fcab-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="6fcab-104">Windows PowerShell реализует функции инструментарий управления Windows (WMI) (WMI) с помощью набора командлетов.</span><span class="sxs-lookup"><span data-stu-id="6fcab-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="6fcab-105">Эти командлеты можно использовать для выполнения комплексных задач, необходимых для управления локальными и удаленными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="6fcab-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="6fcab-106">Дополнительные сведения см. в разделе [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="6fcab-107">Классы WMI PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fcab-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="6fcab-108">**Пространство имен**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="6fcab-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="6fcab-109">**Сборка**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="6fcab-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="6fcab-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="6fcab-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="6fcab-111">Эти классы команд WMI реализуются Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fcab-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="6fcab-112">Эти классы включены в этот пакет средств разработки программного обеспечения (SDK) только для полноты.</span><span class="sxs-lookup"><span data-stu-id="6fcab-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="6fcab-113">Члены этих классов не могут использоваться напрямую и не должны использоваться для наследования других классов.</span><span class="sxs-lookup"><span data-stu-id="6fcab-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="6fcab-114">Класс</span><span class="sxs-lookup"><span data-stu-id="6fcab-114">Class</span></span>                   | <span data-ttu-id="6fcab-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6fcab-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcab-116">жетвмиобжекткомманд</span><span class="sxs-lookup"><span data-stu-id="6fcab-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="6fcab-117">Возвращает экземпляры классов WMI или сведения о доступных классах.</span><span class="sxs-lookup"><span data-stu-id="6fcab-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="6fcab-118">Примеры и подробные сведения о параметрах см. в разделе командлет [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="6fcab-119">инвокевмимесод</span><span class="sxs-lookup"><span data-stu-id="6fcab-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="6fcab-120">Вызывает методы WMI.</span><span class="sxs-lookup"><span data-stu-id="6fcab-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="6fcab-121">Примеры и подробные сведения о параметрах см. в разделе командлет [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="6fcab-122">регистервмиевенткомманд</span><span class="sxs-lookup"><span data-stu-id="6fcab-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="6fcab-123">Подписывается на событие WMI.</span><span class="sxs-lookup"><span data-stu-id="6fcab-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="6fcab-124">Примеры и подробные сведения о параметрах см. в разделе командлет [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="6fcab-125">ремовевмиобжект</span><span class="sxs-lookup"><span data-stu-id="6fcab-125">RemoveWmiObject</span></span>         | <span data-ttu-id="6fcab-126">Удаляет экземпляр существующего класса WMI.</span><span class="sxs-lookup"><span data-stu-id="6fcab-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="6fcab-127">Примеры и подробные сведения о параметрах см. в описании командлета [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="6fcab-128">сетвмиинстанце</span><span class="sxs-lookup"><span data-stu-id="6fcab-128">SetWmiInstance</span></span>          | <span data-ttu-id="6fcab-129">Создает или обновляет экземпляр существующего класса WMI.</span><span class="sxs-lookup"><span data-stu-id="6fcab-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="6fcab-130">Примеры и подробные сведения о параметрах см. в разделе командлет [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="6fcab-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

