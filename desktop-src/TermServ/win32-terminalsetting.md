---
title: Класс Win32_TerminalSetting
description: Представляет параметры, которые могут быть применены к терминалу.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalSetting, описание
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682064"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="82154-105">\_Класс Win32 терминалсеттинг</span><span class="sxs-lookup"><span data-stu-id="82154-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="82154-106">Класс **WMI \_ Терминалсеттинг для Win32** представляет параметры, которые можно применить к терминалу.</span><span class="sxs-lookup"><span data-stu-id="82154-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="82154-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="82154-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82154-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82154-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="82154-109">Члены</span><span class="sxs-lookup"><span data-stu-id="82154-109">Members</span></span>

<span data-ttu-id="82154-110">Класс **Win32 \_ терминалсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="82154-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="82154-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="82154-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82154-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="82154-112">Properties</span></span>

<span data-ttu-id="82154-113">Класс **Win32 \_ терминалсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="82154-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82154-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="82154-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="82154-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82154-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82154-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="82154-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="82154-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="82154-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="82154-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82154-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82154-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="82154-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="82154-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82154-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82154-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="82154-123">Description of the object.</span></span>

<span data-ttu-id="82154-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82154-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82154-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="82154-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="82154-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="82154-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82154-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="82154-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="82154-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="82154-129">The date the object was installed.</span></span> <span data-ttu-id="82154-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="82154-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="82154-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82154-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82154-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="82154-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="82154-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82154-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82154-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="82154-135">The name of the object.</span></span>

<span data-ttu-id="82154-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82154-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="82154-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="82154-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="82154-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82154-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82154-140">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="82154-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="82154-141">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="82154-141">Current status of the object.</span></span> <span data-ttu-id="82154-142">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="82154-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="82154-143">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="82154-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="82154-144">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="82154-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="82154-145">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="82154-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="82154-146">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="82154-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="82154-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="82154-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="82154-148">("ОК")</span><span class="sxs-lookup"><span data-stu-id="82154-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-149">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="82154-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-150">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="82154-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-151">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="82154-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-152">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="82154-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-153">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="82154-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-154">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="82154-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="82154-155">("Служба")</span><span class="sxs-lookup"><span data-stu-id="82154-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="82154-156">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="82154-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82154-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="82154-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82154-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="82154-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82154-159">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="82154-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82154-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82154-160">Remarks</span></span>

<span data-ttu-id="82154-161">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="82154-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="82154-162">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="82154-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="82154-163">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="82154-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="82154-164">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="82154-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="82154-165">Требования</span><span class="sxs-lookup"><span data-stu-id="82154-165">Requirements</span></span>



| <span data-ttu-id="82154-166">Требование</span><span class="sxs-lookup"><span data-stu-id="82154-166">Requirement</span></span> | <span data-ttu-id="82154-167">Значение</span><span class="sxs-lookup"><span data-stu-id="82154-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82154-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82154-168">Minimum supported client</span></span><br/> | <span data-ttu-id="82154-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82154-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82154-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82154-170">Minimum supported server</span></span><br/> | <span data-ttu-id="82154-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82154-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82154-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="82154-172">Namespace</span></span><br/>                | <span data-ttu-id="82154-173">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="82154-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="82154-174">MOF</span><span class="sxs-lookup"><span data-stu-id="82154-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82154-175"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82154-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="82154-176">DLL</span><span class="sxs-lookup"><span data-stu-id="82154-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82154-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82154-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82154-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82154-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82154-179">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="82154-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="82154-180">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="82154-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="82154-181">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="82154-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

