---
description: Методы объекта SWbemLocator можно использовать для получения объекта SWbemServices, который представляет соединение с пространством имен на локальном или удаленном компьютере.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Объект SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693156"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="bc079-103">Объект SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="bc079-103">SWbemLocator object</span></span>

<span data-ttu-id="bc079-104">Методы объекта **SWbemLocator** можно использовать для получения объекта [**SwbemServices**](swbemservices.md) , который представляет соединение с пространством имен на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc079-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="bc079-105">Затем можно использовать методы объекта **SwbemServices** для доступа к WMI.</span><span class="sxs-lookup"><span data-stu-id="bc079-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="bc079-106">Этот объект может быть создан вызовом метода **CreateObject** VBScript.</span><span class="sxs-lookup"><span data-stu-id="bc079-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="bc079-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bc079-107">Members</span></span>

<span data-ttu-id="bc079-108">Объект **SWbemLocator** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bc079-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="bc079-109">Методы</span><span class="sxs-lookup"><span data-stu-id="bc079-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc079-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc079-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc079-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bc079-111">Methods</span></span>

<span data-ttu-id="bc079-112">Объект **SWbemLocator** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="bc079-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="bc079-113">Метод</span><span class="sxs-lookup"><span data-stu-id="bc079-113">Method</span></span>                                              | <span data-ttu-id="bc079-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bc079-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="bc079-115">**коннектсервер**</span><span class="sxs-lookup"><span data-stu-id="bc079-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="bc079-116">Подключается к инструментарию WMI на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc079-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc079-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc079-117">Properties</span></span>

<span data-ttu-id="bc079-118">Объект **SWbemLocator** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bc079-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="bc079-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="bc079-119">Property</span></span>                                                | <span data-ttu-id="bc079-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="bc079-120">Access type</span></span>          | <span data-ttu-id="bc079-121">Описание</span><span class="sxs-lookup"><span data-stu-id="bc079-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="bc079-122">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="bc079-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="bc079-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc079-123">Read-only</span></span><br/> | <span data-ttu-id="bc079-124">Используется для чтения или изменения параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="bc079-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc079-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc079-125">Remarks</span></span>

<span data-ttu-id="bc079-126">В верхней части объектной модели библиотеки сценариев WMI находится объект SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="bc079-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="bc079-127">SWbemLocator используется для установления подключения с проверкой подлинности к пространству имен WMI, точно так же, как функция VBScript GetObject и моникер WMI "винмгмтс:" используются для установления подключения к WMI с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="bc079-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="bc079-128">Однако SWbemLocator предназначен для выполнения двух конкретных сценариев сценариев, которые не могут быть выполнены с помощью GetObject и моникера WMI.</span><span class="sxs-lookup"><span data-stu-id="bc079-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="bc079-129">SWbemLocator необходимо использовать, если необходимо:</span><span class="sxs-lookup"><span data-stu-id="bc079-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="bc079-130">Укажите учетные данные пользователя и пароль для подключения к инструментарию WMI на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc079-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="bc079-131">Моникер WMI, используемый с функцией GetObject, не включает механизм для указания учетных данных.</span><span class="sxs-lookup"><span data-stu-id="bc079-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="bc079-132">Для большинства действий WMI (включая все, что выполняется на удаленных компьютерах) требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="bc079-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="bc079-133">Если обычно используется обычная учетная запись пользователя, а не учетная запись администратора, то выполнение большинства задач WMI будет невозможным, если не запустить сценарий в разделе альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="bc079-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="bc079-134">Подключитесь к инструментарию WMI, если на веб-странице выполняется сценарий WMI.</span><span class="sxs-lookup"><span data-stu-id="bc079-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="bc079-135">Нельзя использовать функцию GetObject при выполнении скриптов, внедренных в HTML-страницу, так как Internet Explorer запрещает использование GetObject в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="bc079-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="bc079-136">Кроме того, можно использовать SWbemLocator для подключения к инструментарию WMI, если найдена строка подключения WMI, используемая с GetObject, запутанной или сложной.</span><span class="sxs-lookup"><span data-stu-id="bc079-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="bc079-137">Для создания ссылки на SWbemLocator используется CreateObject, а не GetObject.</span><span class="sxs-lookup"><span data-stu-id="bc079-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="bc079-138">Чтобы создать ссылку, необходимо передать функции CreateObject программный идентификатор SWbemLocator (ProgID) "Вбемскриптинг. SWbemLocator", как показано в строке 2 в следующем примере скрипта.</span><span class="sxs-lookup"><span data-stu-id="bc079-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="bc079-139">После получения ссылки на объект SWbemLocator вызывается метод Коннектсервер для подключения к WMI и получения ссылки на объект SWbemServices.</span><span class="sxs-lookup"><span data-stu-id="bc079-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="bc079-140">Это продемонстрировано в строке 3 следующего сценария.</span><span class="sxs-lookup"><span data-stu-id="bc079-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bc079-141">Чтобы выполнить сценарий с дополнительными учетными данными, укажите имя пользователя и пароль в качестве дополнительных параметров, передаваемых в Коннектсервер.</span><span class="sxs-lookup"><span data-stu-id="bc079-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="bc079-142">Например, этот сценарий выполняется с учетными данными пользователя с именем кенмер с паролем хомерж.</span><span class="sxs-lookup"><span data-stu-id="bc079-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bc079-143">\\Для указания имени пользователя также можно использовать формат имени пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="bc079-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="bc079-144">Пример:</span><span class="sxs-lookup"><span data-stu-id="bc079-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="bc079-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="bc079-145">Examples</span></span>

<span data-ttu-id="bc079-146">В следующем примере PowerShell для подключения к серверу используется **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="bc079-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="bc079-147">Требования</span><span class="sxs-lookup"><span data-stu-id="bc079-147">Requirements</span></span>



| <span data-ttu-id="bc079-148">Требование</span><span class="sxs-lookup"><span data-stu-id="bc079-148">Requirement</span></span> | <span data-ttu-id="bc079-149">Значение</span><span class="sxs-lookup"><span data-stu-id="bc079-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc079-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc079-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bc079-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc079-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc079-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc079-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bc079-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc079-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc079-154">Header</span><span class="sxs-lookup"><span data-stu-id="bc079-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc079-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc079-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc079-156">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bc079-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc079-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc079-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc079-158">DLL</span><span class="sxs-lookup"><span data-stu-id="bc079-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc079-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc079-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc079-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc079-160">CLSID</span></span><br/>                    | <span data-ttu-id="bc079-161">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="bc079-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="bc079-162">IID</span><span class="sxs-lookup"><span data-stu-id="bc079-162">IID</span></span><br/>                      | <span data-ttu-id="bc079-163">IID \_ исвбемлокатор</span><span class="sxs-lookup"><span data-stu-id="bc079-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="bc079-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc079-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc079-165">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="bc079-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




