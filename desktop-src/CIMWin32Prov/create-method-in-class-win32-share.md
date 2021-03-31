---
description: Инициирует общий доступ к ресурсу сервера.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Метод Create класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990810"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="8b0a3-103">Метод Create \_ класса общего ресурса Win32</span><span class="sxs-lookup"><span data-stu-id="8b0a3-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="8b0a3-104">Метод **создания**   [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) инициирует общий доступ для ресурса сервера.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="8b0a3-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b0a3-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b0a3-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="8b0a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b0a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0a3-109">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-110">Локальный путь к общей папке Windows.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-110">Local path of the Windows share.</span></span>

<span data-ttu-id="8b0a3-111">Например, "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="8b0a3-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="8b0a3-112">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-113">Передает псевдоним в путь, настроенный как общий ресурс в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="8b0a3-114">Например, "Public".</span><span class="sxs-lookup"><span data-stu-id="8b0a3-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="8b0a3-115">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-116">Передает тип общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="8b0a3-117">Типы включают диски, очереди печати, межпроцессные коммуникации (IPC) и общие устройства.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="8b0a3-118">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="8b0a3-119">**Дисковый накопитель** (0)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="8b0a3-120">**Очередь печати** (1)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="8b0a3-121">**Устройство** (2)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="8b0a3-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="8b0a3-123">**Администратор дискового накопителя** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="8b0a3-124">**Администратор очереди печати** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="8b0a3-125">**Администратор устройства** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="8b0a3-126">**Администратор IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8b0a3-127">*MaximumAllowed* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-128">Максимальное количество пользователей, которым разрешено одновременно использовать этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="8b0a3-129">Пример: 10.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-129">Example: 10.</span></span> <span data-ttu-id="8b0a3-130">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8b0a3-131">*Описание* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-132">Необязательный комментарий для описания ресурса, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="8b0a3-133">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8b0a3-134">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-135">Пароль (если сервер работает с безопасностью на уровне общих ресурсов) для общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="8b0a3-136">Если сервер работает с защитой на уровне пользователя, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="8b0a3-137">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8b0a3-138">*Доступ к* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8b0a3-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0a3-139">Дескриптор безопасности для разрешений уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="8b0a3-140">Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="8b0a3-141">Если этот параметр не указан или имеет **значение NULL**, у каждого пользователя есть доступ на чтение к общей папке.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="8b0a3-142">Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) и [изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0a3-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b0a3-143">Return value</span></span>

<span data-ttu-id="8b0a3-144">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8b0a3-145">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8b0a3-146">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8b0a3-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8b0a3-147">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-148">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-149">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-150">**Недопустимое имя** (9)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-151">**Недопустимый уровень** (10)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-152">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-153">**Повторяющаяся общая папка** (22)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-154">**Путь перенаправления** (23)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-155">**Неизвестное устройство или каталог** (24)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-156">**Не найдено сетевое имя** (25)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="8b0a3-157">**Другие** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="8b0a3-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8b0a3-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b0a3-158">Remarks</span></span>

<span data-ttu-id="8b0a3-159">**CREATE** является статическим методом.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-159">**Create** is a static method.</span></span>

<span data-ttu-id="8b0a3-160">Только члены локальной группы "Администраторы" или "Операторы учетных записей" могут успешно выполнять инструкцию **CREATE**.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="8b0a3-161">Оператор Print может добавлять только очереди принтера.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="8b0a3-162">Оператор связи может добавлять только очереди устройств связи.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="8b0a3-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b0a3-163">Examples</span></span>

<span data-ttu-id="8b0a3-164">В примере [экспорта и импорта общие папки](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell экспортируются и импортируются файловые ресурсы и устанавливаются разрешения для общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="8b0a3-165">Аналогичным образом, пример [создания общего доступа и Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) также создает новый общий ресурс и задает разрешения для общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="8b0a3-166">Следующий код PowerShell создает общую папку.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="8b0a3-167">Предыдущий пример кода возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="8b0a3-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="8b0a3-168">В следующем \# образце кода C описывается вызов метода Create.</span><span class="sxs-lookup"><span data-stu-id="8b0a3-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="8b0a3-169">Требования</span><span class="sxs-lookup"><span data-stu-id="8b0a3-169">Requirements</span></span>



| <span data-ttu-id="8b0a3-170">Требование</span><span class="sxs-lookup"><span data-stu-id="8b0a3-170">Requirement</span></span> | <span data-ttu-id="8b0a3-171">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0a3-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0a3-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b0a3-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0a3-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b0a3-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b0a3-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b0a3-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0a3-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b0a3-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b0a3-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8b0a3-176">Namespace</span></span><br/>                | <span data-ttu-id="8b0a3-177">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8b0a3-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b0a3-178">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0a3-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0a3-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b0a3-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0a3-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0a3-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0a3-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b0a3-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b0a3-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b0a3-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b0a3-183">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b0a3-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8b0a3-184">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="8b0a3-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

