---
title: Класс Win32_TSNetworkAdapterListSetting
description: Перечисляет список сетевых адаптеров, которые могут быть настроены для терминала Win32 \_ на основе указанного протокола и метода транспорта.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSNetworkAdapterListSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSNetworkAdapterListSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681956"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="9ec53-105">\_Класс Win32 тснетворкадаптерлистсеттинг</span><span class="sxs-lookup"><span data-stu-id="9ec53-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="9ec53-106">Класс **WMI \_ Тснетворкадаптерлистсеттинг для Win32** перечисляет список сетевых адаптеров, которые могут быть настроены для [**\_ терминала Win32**](win32-terminal.md), на основе указанного протокола и метода транспорта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="9ec53-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="9ec53-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ec53-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="9ec53-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9ec53-109">Members</span></span>

<span data-ttu-id="9ec53-110">Класс **Win32 \_ тснетворкадаптерлистсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ec53-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9ec53-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ec53-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ec53-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ec53-112">Properties</span></span>

<span data-ttu-id="9ec53-113">Класс **Win32 \_ тснетворкадаптерлистсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ec53-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ec53-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9ec53-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9ec53-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9ec53-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9ec53-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-123">Description of the object.</span></span>

<span data-ttu-id="9ec53-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ec53-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ec53-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="9ec53-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-129">The date the object was installed.</span></span> <span data-ttu-id="9ec53-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="9ec53-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9ec53-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ec53-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-135">The name of the object.</span></span>

<span data-ttu-id="9ec53-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-137">**нетворкадаптерид**</span><span class="sxs-lookup"><span data-stu-id="9ec53-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-140">Идентификатор GUID сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="9ec53-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-141">**нетворкадаптерип**</span><span class="sxs-lookup"><span data-stu-id="9ec53-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-144">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ec53-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-145">IP-адрес сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="9ec53-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-146">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9ec53-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-149">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9ec53-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-150">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9ec53-150">Current status of the object.</span></span> <span data-ttu-id="9ec53-151">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="9ec53-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9ec53-152">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="9ec53-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9ec53-153">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="9ec53-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9ec53-154">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="9ec53-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9ec53-155">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="9ec53-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9ec53-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9ec53-157">("ОК")</span><span class="sxs-lookup"><span data-stu-id="9ec53-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-158">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="9ec53-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-159">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="9ec53-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-160">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9ec53-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-161">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9ec53-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-162">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9ec53-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-163">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="9ec53-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9ec53-164">("Служба")</span><span class="sxs-lookup"><span data-stu-id="9ec53-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ec53-165">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="9ec53-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ec53-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ec53-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ec53-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ec53-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ec53-168">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="9ec53-168">The name of the terminal.</span></span>

<span data-ttu-id="9ec53-169">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ec53-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ec53-170">Remarks</span></span>

<span data-ttu-id="9ec53-171">Чтобы подключиться к \\ \\ пространству имен root cimv2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="9ec53-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="9ec53-172">Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="9ec53-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="9ec53-173">Для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="9ec53-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="9ec53-174">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="9ec53-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="9ec53-175">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9ec53-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9ec53-176">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9ec53-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ec53-177">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9ec53-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9ec53-178">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9ec53-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec53-179">Требования</span><span class="sxs-lookup"><span data-stu-id="9ec53-179">Requirements</span></span>



| <span data-ttu-id="9ec53-180">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec53-180">Requirement</span></span> | <span data-ttu-id="9ec53-181">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec53-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec53-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ec53-182">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec53-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ec53-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ec53-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ec53-184">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec53-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ec53-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ec53-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ec53-186">Namespace</span></span><br/>                | <span data-ttu-id="9ec53-187">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="9ec53-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9ec53-188">MOF</span><span class="sxs-lookup"><span data-stu-id="9ec53-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ec53-189"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ec53-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ec53-190">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec53-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec53-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec53-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec53-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ec53-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec53-193">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9ec53-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="9ec53-194">**\_Тснетворкадаптерсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="9ec53-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

