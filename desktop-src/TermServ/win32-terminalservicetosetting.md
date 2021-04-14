---
title: Класс Win32_TerminalServiceToSetting
description: Представляет связь между экземпляром \_ класса Win32 терминалсервице и параметром определенного \_ Свойства терминалсервицесеттинг Win32.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalServiceToSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalServiceToSetting, описание
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415413"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="de690-105">\_Класс Win32 терминалсервицетосеттинг</span><span class="sxs-lookup"><span data-stu-id="de690-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="de690-106">Класс **WMI \_ терминалсервицетосеттинг** инструментария Win32 представляет связь между экземпляром класса [**Win32 \_ терминалсервице**](win32-terminalservice.md) и параметром конкретного свойства [**Win32 \_ терминалсервицесеттинг**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="de690-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="de690-107">Параметры конфигурации включают режим сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов), лицензирование, активный рабочий стол, возможность разрешения, удаление временных папок и временных папок за сеанс.</span><span class="sxs-lookup"><span data-stu-id="de690-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="de690-108">Следующий синтаксис упрощен из MOF-кода и включает все определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="de690-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de690-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de690-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="de690-110">Члены</span><span class="sxs-lookup"><span data-stu-id="de690-110">Members</span></span>

<span data-ttu-id="de690-111">Класс **Win32 \_ терминалсервицетосеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="de690-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="de690-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="de690-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de690-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="de690-113">Properties</span></span>

<span data-ttu-id="de690-114">Класс **Win32 \_ терминалсервицетосеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="de690-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de690-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="de690-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de690-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de690-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de690-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de690-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de690-119">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="de690-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="de690-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de690-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de690-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de690-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de690-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de690-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de690-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="de690-124">Description of the object.</span></span>

<span data-ttu-id="de690-125">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de690-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de690-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="de690-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-127">Тип данных: **Win32 \_ терминалсервице**</span><span class="sxs-lookup"><span data-stu-id="de690-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="de690-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de690-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de690-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de690-130">Представляет экземпляр [**Win32 \_ терминалсервице**](win32-terminalservice.md) , который можно настроить с помощью свойства **Setting** .</span><span class="sxs-lookup"><span data-stu-id="de690-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="de690-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="de690-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-132">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de690-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de690-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de690-134">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="de690-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="de690-135">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="de690-135">The date the object was installed.</span></span> <span data-ttu-id="de690-136">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="de690-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="de690-137">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de690-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de690-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="de690-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de690-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de690-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de690-141">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="de690-141">The name of the object.</span></span>

<span data-ttu-id="de690-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de690-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de690-143">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="de690-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-144">Тип данных: **Win32 \_ терминалсервицесеттинг**</span><span class="sxs-lookup"><span data-stu-id="de690-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="de690-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de690-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de690-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de690-147">Представляет параметры конфигурации службы удаленных рабочих столов, которые могут быть применены к связанному серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="de690-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="de690-148">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="de690-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de690-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de690-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de690-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de690-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de690-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="de690-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="de690-152">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="de690-152">Current status of the object.</span></span> <span data-ttu-id="de690-153">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="de690-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="de690-154">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="de690-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="de690-155">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="de690-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="de690-156">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="de690-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="de690-157">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="de690-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="de690-158">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de690-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="de690-159">("ОК")</span><span class="sxs-lookup"><span data-stu-id="de690-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-160">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="de690-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-161">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="de690-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-162">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="de690-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-163">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="de690-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-164">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="de690-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-165">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="de690-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="de690-166">("Служба")</span><span class="sxs-lookup"><span data-stu-id="de690-166">("Service")</span></span>


<span data-ttu-id="de690-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="de690-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="de690-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de690-168">Remarks</span></span>

<span data-ttu-id="de690-169">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="de690-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de690-170">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="de690-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="de690-171">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="de690-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de690-172">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="de690-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="de690-173">Требования</span><span class="sxs-lookup"><span data-stu-id="de690-173">Requirements</span></span>



| <span data-ttu-id="de690-174">Требование</span><span class="sxs-lookup"><span data-stu-id="de690-174">Requirement</span></span> | <span data-ttu-id="de690-175">Значение</span><span class="sxs-lookup"><span data-stu-id="de690-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de690-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de690-176">Minimum supported client</span></span><br/> | <span data-ttu-id="de690-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de690-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de690-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de690-178">Minimum supported server</span></span><br/> | <span data-ttu-id="de690-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de690-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de690-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de690-180">Namespace</span></span><br/>                | <span data-ttu-id="de690-181">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="de690-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="de690-182">MOF</span><span class="sxs-lookup"><span data-stu-id="de690-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de690-183"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de690-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="de690-184">DLL</span><span class="sxs-lookup"><span data-stu-id="de690-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de690-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de690-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de690-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de690-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de690-187">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="de690-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="de690-188">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="de690-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="de690-189">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="de690-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="de690-190">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="de690-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

