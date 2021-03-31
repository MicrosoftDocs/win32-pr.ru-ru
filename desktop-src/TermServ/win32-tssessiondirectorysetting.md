---
title: Класс Win32_TSSessionDirectorySetting
description: Представляет связь между экземпляром \_ класса Win32 терминалсервице и экземпляром \_ класса тссессиондиректори Win32.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSessionDirectorySetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSessionDirectorySetting, описание
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071212"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="64c3c-105">\_Класс Win32 тссессиондиректорисеттинг</span><span class="sxs-lookup"><span data-stu-id="64c3c-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="64c3c-106">Представляет связь между экземпляром класса [**Win32 \_ терминалсервице**](win32-terminalservice.md) и экземпляром класса [**\_ тссессиондиректори Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="64c3c-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="64c3c-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="64c3c-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c3c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64c3c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="64c3c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="64c3c-109">Members</span></span>

<span data-ttu-id="64c3c-110">Класс **Win32 \_ тссессиондиректорисеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="64c3c-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="64c3c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="64c3c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64c3c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="64c3c-112">Properties</span></span>

<span data-ttu-id="64c3c-113">Класс **Win32 \_ тссессиондиректорисеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="64c3c-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64c3c-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="64c3c-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64c3c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="64c3c-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="64c3c-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="64c3c-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64c3c-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64c3c-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64c3c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="64c3c-123">Description of the object.</span></span>

<span data-ttu-id="64c3c-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64c3c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-125">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="64c3c-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-126">Тип данных: **Win32 \_ терминалсервице**</span><span class="sxs-lookup"><span data-stu-id="64c3c-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64c3c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-129">Представляет экземпляр **Win32 \_ терминалсервице** , который можно настроить с помощью свойства **Setting** .</span><span class="sxs-lookup"><span data-stu-id="64c3c-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="64c3c-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="64c3c-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="64c3c-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-134">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="64c3c-134">The date the object was installed.</span></span> <span data-ttu-id="64c3c-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="64c3c-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="64c3c-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64c3c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="64c3c-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64c3c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-140">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="64c3c-140">The name of the object.</span></span>

<span data-ttu-id="64c3c-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64c3c-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-142">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="64c3c-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-143">Тип данных: **Win32 \_ тссессиондиректори**</span><span class="sxs-lookup"><span data-stu-id="64c3c-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64c3c-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-146">Представляет параметры RDCB, которые могут быть применены к связанному серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="64c3c-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="64c3c-147">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="64c3c-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c3c-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64c3c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64c3c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c3c-150">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="64c3c-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="64c3c-151">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="64c3c-151">Current status of the object.</span></span> <span data-ttu-id="64c3c-152">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="64c3c-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="64c3c-153">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="64c3c-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="64c3c-154">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="64c3c-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="64c3c-155">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="64c3c-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="64c3c-156">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="64c3c-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="64c3c-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64c3c-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="64c3c-158">("ОК")</span><span class="sxs-lookup"><span data-stu-id="64c3c-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-159">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="64c3c-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-160">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="64c3c-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-161">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="64c3c-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-162">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="64c3c-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-163">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="64c3c-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-164">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="64c3c-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64c3c-165">("Служба")</span><span class="sxs-lookup"><span data-stu-id="64c3c-165">("Service")</span></span>


<span data-ttu-id="64c3c-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="64c3c-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="64c3c-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64c3c-167">Remarks</span></span>

<span data-ttu-id="64c3c-168">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="64c3c-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64c3c-169">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="64c3c-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64c3c-170">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="64c3c-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64c3c-171">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="64c3c-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="64c3c-172">Требования</span><span class="sxs-lookup"><span data-stu-id="64c3c-172">Requirements</span></span>



| <span data-ttu-id="64c3c-173">Требование</span><span class="sxs-lookup"><span data-stu-id="64c3c-173">Requirement</span></span> | <span data-ttu-id="64c3c-174">Значение</span><span class="sxs-lookup"><span data-stu-id="64c3c-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c3c-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64c3c-175">Minimum supported client</span></span><br/> | <span data-ttu-id="64c3c-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64c3c-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64c3c-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64c3c-177">Minimum supported server</span></span><br/> | <span data-ttu-id="64c3c-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64c3c-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64c3c-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64c3c-179">Namespace</span></span><br/>                | <span data-ttu-id="64c3c-180">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="64c3c-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="64c3c-181">MOF</span><span class="sxs-lookup"><span data-stu-id="64c3c-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64c3c-182"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64c3c-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="64c3c-183">DLL</span><span class="sxs-lookup"><span data-stu-id="64c3c-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64c3c-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64c3c-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c3c-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64c3c-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c3c-186">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="64c3c-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="64c3c-187">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="64c3c-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="64c3c-188">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="64c3c-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

