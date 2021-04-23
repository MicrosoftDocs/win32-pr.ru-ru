---
title: Класс Win32_TerminalTerminalSetting
description: Представляет связь между терминалом и его параметрами конфигурации.
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalTerminalSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalTerminalSetting, описание
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490290"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="8fc4d-105">\_Класс Win32 терминалтерминалсеттинг</span><span class="sxs-lookup"><span data-stu-id="8fc4d-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="8fc4d-106">Класс **WMI \_ Терминалтерминалсеттинг для Win32** представляет связь между терминалом и его параметрами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="8fc4d-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc4d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fc4d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="8fc4d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="8fc4d-109">Members</span></span>

<span data-ttu-id="8fc4d-110">Класс **Win32 \_ терминалтерминалсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8fc4d-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8fc4d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8fc4d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fc4d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8fc4d-112">Properties</span></span>

<span data-ttu-id="8fc4d-113">Класс **Win32 \_ терминалтерминалсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fc4d-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8fc4d-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8fc4d-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-123">Description of the object.</span></span>

<span data-ttu-id="8fc4d-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-125">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-126">Тип данных: **\_ терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fc4d-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-129">Представляет терминал, который можно настроить с помощью свойства **Setting** .</span><span class="sxs-lookup"><span data-stu-id="8fc4d-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="8fc4d-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-134">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-134">The date the object was installed.</span></span> <span data-ttu-id="8fc4d-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8fc4d-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-140">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-140">The name of the object.</span></span>

<span data-ttu-id="8fc4d-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-142">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-143">Тип данных: **Win32 \_ терминалсеттинг**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fc4d-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-146">Представляет параметры, которые могут быть применены к указанному терминалу.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="8fc4d-147">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc4d-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc4d-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc4d-150">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8fc4d-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8fc4d-151">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-151">Current status of the object.</span></span> <span data-ttu-id="8fc4d-152">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8fc4d-153">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8fc4d-154">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="8fc4d-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8fc4d-155">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8fc4d-156">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8fc4d-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8fc4d-158">("ОК")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-159">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-160">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-161">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-162">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-163">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-164">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8fc4d-165">("Служба")</span><span class="sxs-lookup"><span data-stu-id="8fc4d-165">("Service")</span></span>


<span data-ttu-id="8fc4d-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fc4d-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8fc4d-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fc4d-167">Remarks</span></span>

<span data-ttu-id="8fc4d-168">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8fc4d-169">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8fc4d-170">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8fc4d-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8fc4d-171">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8fc4d-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc4d-172">Требования</span><span class="sxs-lookup"><span data-stu-id="8fc4d-172">Requirements</span></span>



| <span data-ttu-id="8fc4d-173">Требование</span><span class="sxs-lookup"><span data-stu-id="8fc4d-173">Requirement</span></span> | <span data-ttu-id="8fc4d-174">Значение</span><span class="sxs-lookup"><span data-stu-id="8fc4d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc4d-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fc4d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc4d-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fc4d-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fc4d-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fc4d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc4d-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc4d-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fc4d-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fc4d-179">Namespace</span></span><br/>                | <span data-ttu-id="8fc4d-180">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8fc4d-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8fc4d-181">MOF</span><span class="sxs-lookup"><span data-stu-id="8fc4d-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fc4d-182"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fc4d-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fc4d-183">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc4d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc4d-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc4d-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc4d-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fc4d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc4d-186">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="8fc4d-187">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8fc4d-188">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc4d-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

