---
description: Формат строки моникера аналогичен стандартному пути к объекту WMI. Дополнительные сведения см. в разделе Требования к пути к объектам WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Создание строки моникера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344935"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="05524-104">Создание строки моникера</span><span class="sxs-lookup"><span data-stu-id="05524-104">Constructing a Moniker String</span></span>

<span data-ttu-id="05524-105">Формат строки моникера аналогичен стандартному пути к объекту WMI.</span><span class="sxs-lookup"><span data-stu-id="05524-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="05524-106">Дополнительные сведения см. в разделе [требования к пути к объектам WMI](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="05524-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="05524-107">Моникер состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="05524-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="05524-108">Префикс Винмгмтс: (обязательный).</span><span class="sxs-lookup"><span data-stu-id="05524-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="05524-109">Префикс инструктирует сервер сценариев Windows (WSH), что следующий код будет использовать [объекты API скрипта](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="05524-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="05524-110">Компонент параметров безопасности (необязательно)</span><span class="sxs-lookup"><span data-stu-id="05524-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="05524-111">Компонент пути объекта WMI (необязательно)</span><span class="sxs-lookup"><span data-stu-id="05524-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="05524-112">В строке моникера WMI нельзя указать пароль.</span><span class="sxs-lookup"><span data-stu-id="05524-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="05524-113">Если необходимо изменить пароль (параметр *стрпассворд* ) или тип проверки подлинности (параметр *страусорити* ) при подключении к WMI, вызовите [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="05524-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="05524-114">Имейте в виду, что в подключениях к удаленным компьютерам можно указать только пароль и полномочия.</span><span class="sxs-lookup"><span data-stu-id="05524-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="05524-115">Попытка задать эти значения в скрипте, который выполняется на локальном компьютере, приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="05524-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="05524-116">Дополнительные сведения о том, когда используются параметры безопасности и компоненты пути к объекту, см. в разделе [Параметры безопасности WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="05524-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="05524-117">В следующем моникере указывается объект [**SwbemServices**](swbemservices.md) , представляющий корневой элемент пространства имен \\ по умолчанию с включенным параметром олицетворения и привилегией вбемпривилежедебуг (SeDebugPrivilege), а также разрешение вбемпривилежесекурити (SeSecurityPrivilege).</span><span class="sxs-lookup"><span data-stu-id="05524-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="05524-118">Все строковые литералы не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="05524-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="05524-119">Префикс "!" в привилегии означает, что привилегия должна быть отключена; упущение этого префикса означает, что права доступа должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="05524-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="05524-120">Префикс "!" используется для имени компьютера или пространства имен, если параметры безопасности указаны в квадратных скобках перед именем компьютера или пространством имен.</span><span class="sxs-lookup"><span data-stu-id="05524-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="05524-121">При указании пути к объекту разрешены следующие назначения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="05524-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="05524-122">Имя компьютера может быть опущено в пути к объекту, в этом случае предполагается имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="05524-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="05524-123">Пространство имен можно опустить из пути объекта. в этом случае предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05524-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="05524-124">Это определяется по значению раздела реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Скрипт** \\ **по умолчанию**, значение по умолчанию — root \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="05524-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="05524-125">Можно также указать класс или экземпляр, в этом случае возвращаемый объект является WMI-объектом, а не объектом служб.</span><span class="sxs-lookup"><span data-stu-id="05524-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="05524-126">Если указан класс или экземпляр, пространство имен нельзя опустить при указании имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="05524-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="05524-127">Ссылки на константы прав доступа, используемые в строке моникера WMI, см. в разделе [константы прав](privilege-constants.md)и дескрипторы "краткое имя скрипта".</span><span class="sxs-lookup"><span data-stu-id="05524-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="05524-128">Допустимые строки моникера</span><span class="sxs-lookup"><span data-stu-id="05524-128">Valid Moniker Strings</span></span>

<span data-ttu-id="05524-129">В следующих примерах показаны допустимые строки моникера.</span><span class="sxs-lookup"><span data-stu-id="05524-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="05524-130">Следующий моникер определяет пространство имен по умолчанию на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="05524-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="05524-131">Возвращается объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="05524-132">Следующий моникер определяет пространство имен по умолчанию на компьютере myServer.</span><span class="sxs-lookup"><span data-stu-id="05524-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="05524-133">Возвращается объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="05524-134">Следующий моникер определяет корневое \\ пространство имен CIMV2 на компьютере MyServer.</span><span class="sxs-lookup"><span data-stu-id="05524-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="05524-135">Возвращается объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="05524-136">Следующий моникер определяет корневое \\ пространство имен CIMV2 на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="05524-137">Возвращается объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="05524-138">Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в корневом \\ пространстве имен CIMV2 на сервере MyServer.</span><span class="sxs-lookup"><span data-stu-id="05524-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="05524-139">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="05524-140">Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в корневом \\ пространстве имен CIMV2 на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="05524-141">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="05524-142">Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в пространстве имен по умолчанию на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="05524-143">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="05524-144">Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в пространстве имен сценариев по умолчанию на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="05524-145">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="05524-146">Пространство имен по умолчанию для сценариев определяется параметром конфигурации пространства имен по умолчанию, как указано в элементе управления WMI.</span><span class="sxs-lookup"><span data-stu-id="05524-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="05524-147">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="05524-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="05524-148">Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в корневом \\ пространстве имен CIMV2 на сервере MyServer.</span><span class="sxs-lookup"><span data-stu-id="05524-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="05524-149">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="05524-150">Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в корневом \\ пространстве имен CIMV2 на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="05524-151">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="05524-152">Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в пространстве имен по умолчанию на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="05524-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="05524-153">Возвращается объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05524-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="05524-154">Следующий моникер задает уровень олицетворения для олицетворения и устанавливает \_ право доступа для отладки SE.</span><span class="sxs-lookup"><span data-stu-id="05524-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="05524-155">Следующий моникер задает уровень олицетворения для олицетворения и устанавливает \_ право доступа для отладки SE.</span><span class="sxs-lookup"><span data-stu-id="05524-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="05524-156">Он также отменяет \_ право на завершение работы SE.</span><span class="sxs-lookup"><span data-stu-id="05524-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="05524-157">Следующий моникер извлекает локализованные описания для класса **MyClass** на английском языке из корневого \\ пространства имен WMI.</span><span class="sxs-lookup"><span data-stu-id="05524-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="05524-158">Следующий моникер запрашивает проверку подлинности Kerberos с помощью основного \\ сервера mydomain.</span><span class="sxs-lookup"><span data-stu-id="05524-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="05524-159">Следующий моникер запрашивает проверку подлинности NTLM с помощью домена mydomain.</span><span class="sxs-lookup"><span data-stu-id="05524-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="05524-160">В следующем примере кода VBScript показано, как объединить параметры безопасности и языкового стандарта в моникере.</span><span class="sxs-lookup"><span data-stu-id="05524-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Хотя моникеры предоставляют более прямой доступ к объектам, в некоторых обстоятельствах многократное использование моникеров может оказаться менее эффективным, чем эквивалентный код, который явно подключается к инструментарию WMI. <span data-ttu-id="05524-162">Если необходимо учитывать производительность приложения, попробуйте использовать альтернативные механизмы.</span><span class="sxs-lookup"><span data-stu-id="05524-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="05524-163">Функцию **GetObject** , предоставляемую сценарием VBScript, нельзя использовать для обновления или установки данных при выполнении скриптов, внедренных в HTML-страницу, так как Microsoft Internet Explorer запрещает использование этого вызова в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="05524-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
