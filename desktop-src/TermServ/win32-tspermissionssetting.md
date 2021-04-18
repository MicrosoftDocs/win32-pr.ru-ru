---
title: Класс Win32_TSPermissionsSetting
description: Включает метод для добавления новых учетных записей в терминал и метод восстановления разрешений по умолчанию для терминала.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSPermissionsSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSPermissionsSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672819"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="9df57-105">\_Класс Win32 тспермиссионссеттинг</span><span class="sxs-lookup"><span data-stu-id="9df57-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="9df57-106">Класс **WMI \_ Тспермиссионссеттинг для Win32** включает метод добавления новых учетных записей в терминал и метод для восстановления разрешений по умолчанию для терминала.</span><span class="sxs-lookup"><span data-stu-id="9df57-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="9df57-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="9df57-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="9df57-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9df57-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df57-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9df57-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="9df57-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9df57-110">Members</span></span>

<span data-ttu-id="9df57-111">Класс **Win32 \_ тспермиссионссеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9df57-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9df57-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9df57-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9df57-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9df57-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9df57-114">Методы</span><span class="sxs-lookup"><span data-stu-id="9df57-114">Methods</span></span>

<span data-ttu-id="9df57-115">Класс **Win32 \_ тспермиссионссеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9df57-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="9df57-116">Метод</span><span class="sxs-lookup"><span data-stu-id="9df57-116">Method</span></span>                                                                | <span data-ttu-id="9df57-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9df57-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9df57-118">**аддаккаунт**</span><span class="sxs-lookup"><span data-stu-id="9df57-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="9df57-119">Добавляет учетную запись в терминал с набором разрешений, указанным в значении параметра *пермиссионпресет* .</span><span class="sxs-lookup"><span data-stu-id="9df57-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="9df57-120">**ресторедефаултс**</span><span class="sxs-lookup"><span data-stu-id="9df57-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="9df57-121">Восстанавливает значения набора разрешений по умолчанию для терминала.</span><span class="sxs-lookup"><span data-stu-id="9df57-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="9df57-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="9df57-122">Properties</span></span>

<span data-ttu-id="9df57-123">Класс **Win32 \_ тспермиссионссеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9df57-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9df57-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9df57-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df57-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9df57-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9df57-128">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="9df57-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9df57-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9df57-130">**денядминпермиссионфоркустомизатион**</span><span class="sxs-lookup"><span data-stu-id="9df57-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9df57-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df57-133">Указывает, имеет ли локальный администратор разрешение на настройку.</span><span class="sxs-lookup"><span data-stu-id="9df57-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="9df57-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9df57-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df57-137">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9df57-137">Description of the object.</span></span>

<span data-ttu-id="9df57-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9df57-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9df57-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9df57-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df57-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="9df57-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9df57-143">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="9df57-143">The date the object was installed.</span></span> <span data-ttu-id="9df57-144">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="9df57-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9df57-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9df57-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="9df57-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df57-149">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9df57-149">The name of the object.</span></span>

<span data-ttu-id="9df57-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9df57-151">**полицисаурцеденядминпермиссионфоркустомизатион**</span><span class="sxs-lookup"><span data-stu-id="9df57-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9df57-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df57-154">Указывает, настроено ли свойство **миненкриптионлевел** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9df57-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="9df57-155">0</span><span class="sxs-lookup"><span data-stu-id="9df57-155">0</span></span>
</dt> <dd>

<span data-ttu-id="9df57-156">Сервер</span><span class="sxs-lookup"><span data-stu-id="9df57-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="9df57-157">1</span><span class="sxs-lookup"><span data-stu-id="9df57-157">1</span></span>
</dt> <dd>

<span data-ttu-id="9df57-158">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="9df57-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9df57-159">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9df57-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df57-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9df57-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9df57-163">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9df57-163">Current status of the object.</span></span> <span data-ttu-id="9df57-164">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="9df57-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9df57-165">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="9df57-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9df57-166">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="9df57-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9df57-167">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="9df57-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9df57-168">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="9df57-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9df57-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9df57-170">("ОК")</span><span class="sxs-lookup"><span data-stu-id="9df57-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-171">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="9df57-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-172">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="9df57-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-173">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9df57-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-174">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9df57-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-175">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9df57-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-176">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="9df57-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9df57-177">("Служба")</span><span class="sxs-lookup"><span data-stu-id="9df57-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9df57-178">**стрингсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="9df57-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9df57-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9df57-181">Дескриптор безопасности, связанный с терминалом в двоичном формате байтового массива.</span><span class="sxs-lookup"><span data-stu-id="9df57-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="9df57-182">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="9df57-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df57-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9df57-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df57-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9df57-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df57-185">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="9df57-185">The name of the terminal.</span></span>

<span data-ttu-id="9df57-186">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9df57-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9df57-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9df57-187">Remarks</span></span>

<span data-ttu-id="9df57-188">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="9df57-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="9df57-189">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="9df57-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="9df57-190">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="9df57-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="9df57-191">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="9df57-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="9df57-192">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9df57-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9df57-193">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9df57-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9df57-194">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9df57-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9df57-195">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9df57-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9df57-196">Требования</span><span class="sxs-lookup"><span data-stu-id="9df57-196">Requirements</span></span>



| <span data-ttu-id="9df57-197">Требование</span><span class="sxs-lookup"><span data-stu-id="9df57-197">Requirement</span></span> | <span data-ttu-id="9df57-198">Значение</span><span class="sxs-lookup"><span data-stu-id="9df57-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9df57-199">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9df57-199">Minimum supported client</span></span><br/> | <span data-ttu-id="9df57-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9df57-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9df57-201">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9df57-201">Minimum supported server</span></span><br/> | <span data-ttu-id="9df57-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9df57-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9df57-203">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9df57-203">Namespace</span></span><br/>                | <span data-ttu-id="9df57-204">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="9df57-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9df57-205">MOF</span><span class="sxs-lookup"><span data-stu-id="9df57-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9df57-206"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9df57-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9df57-207">DLL</span><span class="sxs-lookup"><span data-stu-id="9df57-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9df57-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9df57-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df57-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9df57-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df57-210">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9df57-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

