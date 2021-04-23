---
title: Класс Win32_TSAccount
description: Разрешает удаление учетной записи, которая существует на \_ терминале Win32, и изменение существующих разрешений.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSAccount службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSAccount, описание
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682061"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="b1def-105">\_Класс Win32 тсаккаунт</span><span class="sxs-lookup"><span data-stu-id="b1def-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="b1def-106">Класс **WMI \_ Тсаккаунт для Win32** позволяет удалять учетную запись, которая существует на [**\_ терминале Win32**](win32-terminal.md) , и изменять существующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="b1def-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="b1def-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="b1def-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="b1def-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b1def-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1def-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1def-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="b1def-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b1def-110">Members</span></span>

<span data-ttu-id="b1def-111">Класс **Win32 \_ тсаккаунт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b1def-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="b1def-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b1def-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1def-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1def-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1def-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b1def-114">Methods</span></span>

<span data-ttu-id="b1def-115">Класс **Win32 \_ тсаккаунт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b1def-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="b1def-116">Метод</span><span class="sxs-lookup"><span data-stu-id="b1def-116">Method</span></span>                                                                   | <span data-ttu-id="b1def-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b1def-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1def-118">**Удален**</span><span class="sxs-lookup"><span data-stu-id="b1def-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="b1def-119">Удаляет указанную учетную запись пользователя, группы или компьютера.</span><span class="sxs-lookup"><span data-stu-id="b1def-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="b1def-120">**модифяудитпермиссионс**</span><span class="sxs-lookup"><span data-stu-id="b1def-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="b1def-121">Изменяет гранулярность набора разрешений аудита для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="b1def-122">**модифипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="b1def-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="b1def-123">Задает более детализированный набор разрешений для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="b1def-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1def-124">Properties</span></span>

<span data-ttu-id="b1def-125">Класс **Win32 \_ тсаккаунт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b1def-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1def-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="b1def-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1def-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1def-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b1def-130">Текущее имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-130">The current name of the account.</span></span> <span data-ttu-id="b1def-131">Имя домена включено.</span><span class="sxs-lookup"><span data-stu-id="b1def-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="b1def-132">**аудитфаил**</span><span class="sxs-lookup"><span data-stu-id="b1def-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1def-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-135">Указывает [разрешения служб узла удаленный рабочий стол сеансов](terminal-services-permissions.md) , которые подлежат аудиту для состояния сбоя.</span><span class="sxs-lookup"><span data-stu-id="b1def-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="b1def-136">Значением этого свойства является битовая маска, которой можно присвоить одно или несколько значений свойства **пермиссионсалловед** .</span><span class="sxs-lookup"><span data-stu-id="b1def-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="b1def-137">**Винстатион \_ ЗАПРОС = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="b1def-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="b1def-138">**Винстатион \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="b1def-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="b1def-139">**Винстатион \_ Выход из системы = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="b1def-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="b1def-140">**Винстатион \_ \| Требуются права на виртуальные стандартные \_ \_ = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="b1def-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="b1def-141">**Винстатион \_ SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="b1def-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="b1def-142">**Винстатион \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="b1def-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="b1def-143">**Винстатион \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="b1def-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="b1def-144">**Винстатион \_ CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="b1def-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="b1def-145">**Винстатион \_ DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="b1def-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1def-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="b1def-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1def-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-149">Указывает разрешения, относящиеся к серверу узла сеансов удаленных рабочих столов, которые подлежат аудиту для условия успеха.</span><span class="sxs-lookup"><span data-stu-id="b1def-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="b1def-150">Значением этого свойства является битовая маска, которой можно присвоить одно или несколько значений свойства **пермиссионсалловед** .</span><span class="sxs-lookup"><span data-stu-id="b1def-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="b1def-151">**Винстатион \_ ЗАПРОС = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="b1def-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="b1def-152">**Винстатион \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="b1def-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="b1def-153">**Винстатион \_ LOGOFF = 0x4WINSTATION \_ . \| требуются права на виртуальные стандартные \_ \_ = 0xF008** (2)</span><span class="sxs-lookup"><span data-stu-id="b1def-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="b1def-154">**Винстатион \_ SHADOW = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="b1def-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="b1def-155">**Винстатион \_ LOGON = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="b1def-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="b1def-156">**Винстатион \_ MSG = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="b1def-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="b1def-157">**Винстатион \_ CONNECT = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="b1def-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="b1def-158">**Винстатион \_ DISCONNECT = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="b1def-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1def-159">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b1def-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1def-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b1def-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1def-163">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="b1def-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b1def-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1def-165">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b1def-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-168">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b1def-168">Description of the object.</span></span>

<span data-ttu-id="b1def-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1def-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1def-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-171">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1def-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1def-173">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="b1def-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b1def-174">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b1def-174">The date the object was installed.</span></span> <span data-ttu-id="b1def-175">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b1def-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b1def-176">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1def-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1def-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-180">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b1def-180">The name of the object.</span></span>

<span data-ttu-id="b1def-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1def-182">**пермиссионсалловед**</span><span class="sxs-lookup"><span data-stu-id="b1def-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1def-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-185">Указывает [разрешения службы удаленных рабочих столов](terminal-services-permissions.md) , разрешенные для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="b1def-186">Значением этого свойства является битовая маска, которой можно присвоить одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b1def-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="b1def-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**Винстатион \_ ЗАПРОС = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="b1def-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-188">Разрешение на запрос сведений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="b1def-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="b1def-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Винстатион \_ SET** (2)</span><span class="sxs-lookup"><span data-stu-id="b1def-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-190">Разрешение на изменение параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="b1def-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="b1def-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Винстатион \_ Сброс** (64)</span><span class="sxs-lookup"><span data-stu-id="b1def-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-192">Разрешение на сброс или завершение сеанса или соединения.</span><span class="sxs-lookup"><span data-stu-id="b1def-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="b1def-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Винстатион \_ \| \_ \_ Требуются права на виртуальные стандартные** (983048)</span><span class="sxs-lookup"><span data-stu-id="b1def-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-194">Разрешение на использование виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="b1def-194">Permission to use virtual channels.</span></span> <span data-ttu-id="b1def-195">Виртуальные каналы обеспечивают доступ из серверной программы к клиентским устройствам.</span><span class="sxs-lookup"><span data-stu-id="b1def-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="b1def-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Винстатион \_ Тень** (16)</span><span class="sxs-lookup"><span data-stu-id="b1def-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-197">Разрешение на теневое или удаленное управление сеансом другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1def-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="b1def-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Винстатион \_ Вход в систему** (32)</span><span class="sxs-lookup"><span data-stu-id="b1def-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-199">Разрешение на вход в сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="b1def-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="b1def-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Винстатион \_ Выход из системы** (4)</span><span class="sxs-lookup"><span data-stu-id="b1def-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-201">Разрешение на выход пользователя из сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1def-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="b1def-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Винстатион \_ СООБЩЕНИЕ** (128)</span><span class="sxs-lookup"><span data-stu-id="b1def-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-203">Разрешение на отправку сообщений в сеанс другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1def-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="b1def-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Винстатион \_ Подключение** (256)</span><span class="sxs-lookup"><span data-stu-id="b1def-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-205">Разрешение на подключение к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="b1def-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="b1def-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Винстатион \_ Отключение** (512)</span><span class="sxs-lookup"><span data-stu-id="b1def-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="b1def-207">Разрешение на отключение сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1def-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1def-208">**пермиссионсдениед**</span><span class="sxs-lookup"><span data-stu-id="b1def-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-209">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1def-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-211">Указывает разрешения, относящиеся к серверу узла сеансов удаленных рабочих столов, запрещенные для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="b1def-212">Значением этого свойства является битовая маска, которой можно присвоить одно или несколько значений свойства **пермиссионсалловед** .</span><span class="sxs-lookup"><span data-stu-id="b1def-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="b1def-213">**Винстатион \_ ЗАПРОС = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="b1def-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="b1def-214">**Винстатион \_ SET = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="b1def-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="b1def-215">**Винстатион \_ Выход из системы = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="b1def-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="b1def-216">**Винстатион \_ \| Требуются права на виртуальные стандартные \_ \_ = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="b1def-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="b1def-217">**Винстатион \_ SHADOW = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="b1def-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="b1def-218">**Винстатион \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="b1def-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="b1def-219">**Винстатион \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="b1def-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="b1def-220">**Винстатион \_ CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="b1def-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="b1def-221">**Винстатион \_ DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="b1def-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1def-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="b1def-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-225">Указывает [идентификаторы безопасности](/windows/desktop/SecAuthZ/security-identifiers) учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b1def-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="b1def-226">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b1def-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1def-229">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b1def-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b1def-230">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b1def-230">Current status of the object.</span></span> <span data-ttu-id="b1def-231">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b1def-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b1def-232">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b1def-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b1def-233">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b1def-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1def-234">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="b1def-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1def-235">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b1def-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1def-236">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b1def-237">("ОК")</span><span class="sxs-lookup"><span data-stu-id="b1def-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-238">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="b1def-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-239">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="b1def-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-240">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b1def-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-241">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b1def-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-242">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b1def-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-243">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="b1def-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b1def-244">("Служба")</span><span class="sxs-lookup"><span data-stu-id="b1def-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1def-245">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="b1def-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1def-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1def-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1def-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1def-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1def-248">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="b1def-248">The name of the terminal.</span></span>

<span data-ttu-id="b1def-249">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="b1def-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1def-250">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1def-250">Remarks</span></span>

<span data-ttu-id="b1def-251">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="b1def-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b1def-252">Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="b1def-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="b1def-253">Для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="b1def-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="b1def-254">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="b1def-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b1def-255">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b1def-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b1def-256">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b1def-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b1def-257">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b1def-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b1def-258">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b1def-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1def-259">Требования</span><span class="sxs-lookup"><span data-stu-id="b1def-259">Requirements</span></span>



| <span data-ttu-id="b1def-260">Требование</span><span class="sxs-lookup"><span data-stu-id="b1def-260">Requirement</span></span> | <span data-ttu-id="b1def-261">Значение</span><span class="sxs-lookup"><span data-stu-id="b1def-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1def-262">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1def-262">Minimum supported client</span></span><br/> | <span data-ttu-id="b1def-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1def-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1def-264">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1def-264">Minimum supported server</span></span><br/> | <span data-ttu-id="b1def-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1def-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1def-266">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b1def-266">Namespace</span></span><br/>                | <span data-ttu-id="b1def-267">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b1def-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b1def-268">MOF</span><span class="sxs-lookup"><span data-stu-id="b1def-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1def-269"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1def-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1def-270">DLL</span><span class="sxs-lookup"><span data-stu-id="b1def-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1def-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1def-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1def-272">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1def-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1def-273">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="b1def-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

