---
description: Привилегированные операции требуют привилегий безопасности, таких как Селоаддриверпривилеже (Вбемпривилежелоаддривер в константах API скриптов), права доступа, которые должны быть включены для учетной записи, загружая драйвер устройства.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Выполнение привилегированных операций
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702062"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="3dc6b-103">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="3dc6b-103">Executing Privileged Operations</span></span>

<span data-ttu-id="3dc6b-104">Привилегированные операции требуют привилегий безопасности, таких как **селоаддриверпривилеже** (**вбемпривилежелоаддривер** в [константах API скриптов](scripting-api-constants.md)), права доступа, которые должны быть включены для учетной записи, загружая драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="3dc6b-105">Вы не можете добавить привилегии для администратора или пользователя с помощью инструментария WMI. Вы можете включить только те привилегии, которые у учетной записи уже есть.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="3dc6b-106">Список привилегий см. в разделе [**\_ константы прав**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3dc6b-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="3dc6b-107">По умолчанию локальный пользователь на компьютере может считывать статические данные из [*репозитория WMI*](gloss-w.md), записывать их в экземпляры, предоставляемые поставщиками, и выполнять методы поставщика, если только поставщик не применяет специальные требования безопасности.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="3dc6b-108">Только администраторы могут [подключаться к удаленному компьютеру](connecting-to-wmi-on-a-remote-computer.md), изменять дескрипторы безопасности или изменять данные статического репозитория WMI, такие как определение класса WMI.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="3dc6b-109">Для удаленного подключения разрешены все привилегии.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="3dc6b-110">Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3dc6b-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="3dc6b-111">Константы привилегий для C++ отличаются от тех, которые используются в языках автоматизации, таких как Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="3dc6b-112">В скриптах должно использоваться значение константы, а не имя.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="3dc6b-113">Дополнительные сведения см. в статьях [выполнение привилегированных операций с помощью C++](executing-privileged-operations-using-c-.md) или [выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="3dc6b-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="3dc6b-114">Распространенной причиной ошибок отказа в доступе при использовании инструментария WMI является отсутствие включенного права для операций, например получение всех экземпляров [**Win32 \_ нтевентлогфиле**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3dc6b-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="3dc6b-115">Если не включить привилегию **сесекурити** , доступ к файлу журнала безопасности будет невозможен.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="3dc6b-116">В следующем примере кода VBScript показано, как задать привилегию **сесекурити** в строке моникера.</span><span class="sxs-lookup"><span data-stu-id="3dc6b-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="3dc6b-117">При использовании в моникере имя права в круглых скобках удаляет начальную букву "SE".</span><span class="sxs-lookup"><span data-stu-id="3dc6b-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="3dc6b-118">Дополнительные сведения см. [в разделе Создание строки моникера](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="3dc6b-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="3dc6b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3dc6b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc6b-120">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="3dc6b-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
