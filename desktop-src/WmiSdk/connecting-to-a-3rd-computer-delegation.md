---
description: При запуске скрипта в локальной системе, получающей данные из удаленной системы, Инструментарий WMI предоставляет учетные данные поставщику данных в удаленной системе.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Делегирование с помощью WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424134"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="39ec1-103">Делегирование с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="39ec1-103">Delegating with WMI</span></span>

<span data-ttu-id="39ec1-104">При запуске скрипта в локальной системе, получающей данные из удаленной системы, Инструментарий WMI предоставляет учетные данные поставщику данных в удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="39ec1-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="39ec1-105">Для этого требуется только уровень олицетворения **олицетворения**, поскольку требуется только один прыжок сети.</span><span class="sxs-lookup"><span data-stu-id="39ec1-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="39ec1-106">Однако если сценарий подключается к WMI в удаленной системе и пытается открыть файл журнала в дополнительной удаленной системе, сценарий завершается ошибкой, если только уровень олицетворения не является **делегатом**.</span><span class="sxs-lookup"><span data-stu-id="39ec1-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="39ec1-107">Уровень олицетворения **делегата** требуется для любой операции, включающей более одного прыжка в сеть.</span><span class="sxs-lookup"><span data-stu-id="39ec1-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="39ec1-108">Дополнительные сведения о безопасности DCOM в WMI см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="39ec1-109">Дополнительные сведения о соединении между двумя компьютерами в односетевой трансляции см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="39ec1-110">**Использование делегирования для подключения к компьютеру через другой компьютер**</span><span class="sxs-lookup"><span data-stu-id="39ec1-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="39ec1-111">Включите делегирование в Active Directory (**Active Directory пользователи и компьютеры** в **административных задачах** **панели управления** ) на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="39ec1-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="39ec1-112">Учетная запись в удаленной системе должна быть помечена как **Доверенная для делегирования** , а учетная запись в локальной системе не должна быть помечена как **учетная запись конфиденциальная и не может быть делегирована**.</span><span class="sxs-lookup"><span data-stu-id="39ec1-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="39ec1-113">Локальная система, удаленная система и контроллер домена должны быть членами одного домена или доверенных доменов.</span><span class="sxs-lookup"><span data-stu-id="39ec1-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="39ec1-114">**Примечание**  .  Использование делегирования является угрозой безопасности, так как предоставляет процессам за пределами прямого управления возможность использования ваших учетных данных.</span><span class="sxs-lookup"><span data-stu-id="39ec1-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="39ec1-115">Измените код следующим образом, чтобы указать, что вы хотите использовать делегирование.</span><span class="sxs-lookup"><span data-stu-id="39ec1-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="39ec1-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>Оболочк</span><span class="sxs-lookup"><span data-stu-id="39ec1-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="39ec1-117">Задайте параметр *-Impersonation* в командлете WMI для **делегирования**.</span><span class="sxs-lookup"><span data-stu-id="39ec1-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="39ec1-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>Сценариев</span><span class="sxs-lookup"><span data-stu-id="39ec1-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="39ec1-119">Задайте для параметра *имперсонатионлевел* значение **Delegate** в вызове [SWbemLocator. коннектсервер](swbemlocator-connectserver.md) или **Delegate** в строке [моникера](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="39ec1-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="39ec1-120">Олицетворение также можно задать в объекте [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="39ec1-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="39ec1-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="39ec1-122">Задайте для параметра уровня олицетворения **\_ \_ \_ \_ делегат уровня "RPC C** " в вызове [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="39ec1-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="39ec1-123">Дополнительные сведения о том, когда следует выполнять эти вызовы, см. [в разделе Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="39ec1-124">Чтобы передать удостоверение клиента удаленным COM-серверам в C++, установите маскировку в вызове [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="39ec1-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="39ec1-125">Дополнительные сведения см. в разделе [маскировка](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="39ec1-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="39ec1-126">Examples</span></span>

<span data-ttu-id="39ec1-127">В следующем примере кода показана строка моникера, которая задает **Делегирование** олицетворения.</span><span class="sxs-lookup"><span data-stu-id="39ec1-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="39ec1-128">Имейте в виду, что для центра необходимо задать значение Kerberos.</span><span class="sxs-lookup"><span data-stu-id="39ec1-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="39ec1-129">В следующем примере кода показано, как настроить олицетворение для **делегирования** (значение 4) с помощью [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="39ec1-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="39ec1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="39ec1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ec1-131">Защита удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="39ec1-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="39ec1-132">Удаленное создание процессов с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="39ec1-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
