---
title: Класс Win32_TSVirtualIPSetting
description: Представляет ассоциацию между \_ классом элемента Win32 терминалсервице и \_ классом параметра Win32 тсвиртуалип.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVirtualIPSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVirtualIPSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681768"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="e2862-105">\_Класс Win32 тсвиртуалипсеттинг</span><span class="sxs-lookup"><span data-stu-id="e2862-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="e2862-106">Представляет ассоциацию между классом элемента [**Win32 \_ терминалсервице**](win32-terminalservice.md) и классом параметра [**Win32 \_ тсвиртуалип**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="e2862-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="e2862-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e2862-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2862-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2862-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e2862-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e2862-109">Members</span></span>

<span data-ttu-id="e2862-110">Класс **Win32 \_ тсвиртуалипсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e2862-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e2862-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2862-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2862-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2862-112">Properties</span></span>

<span data-ttu-id="e2862-113">Класс **Win32 \_ тсвиртуалипсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e2862-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2862-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e2862-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2862-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2862-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e2862-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e2862-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="e2862-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e2862-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2862-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2862-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2862-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2862-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2862-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e2862-123">Description of the object.</span></span>

<span data-ttu-id="e2862-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2862-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2862-125">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e2862-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-126">Тип данных: **[ **Win32 \_ терминалсервице**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="e2862-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2862-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2862-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2862-129">Ссылка на объект [**Win32 \_ терминалсервице**](win32-terminalservice.md) , который является классом элемента для ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e2862-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="e2862-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2862-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2862-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2862-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="e2862-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e2862-134">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="e2862-134">The date the object was installed.</span></span> <span data-ttu-id="e2862-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="e2862-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e2862-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2862-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2862-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="e2862-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2862-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2862-140">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e2862-140">The name of the object.</span></span>

<span data-ttu-id="e2862-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2862-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2862-142">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="e2862-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-143">Тип данных: **[ **Win32 \_ тсвиртуалип**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="e2862-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2862-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2862-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2862-146">Ссылка на объект [**Win32 \_ тсвиртуалип**](win32-tsvirtualip.md) , который является классом параметров для ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e2862-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="e2862-147">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e2862-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2862-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2862-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2862-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2862-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2862-150">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e2862-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e2862-151">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e2862-151">Current status of the object.</span></span> <span data-ttu-id="e2862-152">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="e2862-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e2862-153">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="e2862-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e2862-154">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="e2862-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e2862-155">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="e2862-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e2862-156">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="e2862-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e2862-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2862-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e2862-158">("ОК")</span><span class="sxs-lookup"><span data-stu-id="e2862-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-159">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="e2862-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-160">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="e2862-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-161">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e2862-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-162">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e2862-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-163">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e2862-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-164">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="e2862-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e2862-165">("Служба")</span><span class="sxs-lookup"><span data-stu-id="e2862-165">("Service")</span></span>


<span data-ttu-id="e2862-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2862-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e2862-167">Требования</span><span class="sxs-lookup"><span data-stu-id="e2862-167">Requirements</span></span>



| <span data-ttu-id="e2862-168">Требование</span><span class="sxs-lookup"><span data-stu-id="e2862-168">Requirement</span></span> | <span data-ttu-id="e2862-169">Значение</span><span class="sxs-lookup"><span data-stu-id="e2862-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2862-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2862-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e2862-171">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e2862-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e2862-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2862-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e2862-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2862-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e2862-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2862-174">Namespace</span></span><br/>                | <span data-ttu-id="e2862-175">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e2862-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e2862-176">MOF</span><span class="sxs-lookup"><span data-stu-id="e2862-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2862-177"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2862-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2862-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e2862-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2862-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2862-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2862-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2862-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2862-181">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="e2862-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e2862-182">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="e2862-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="e2862-183">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="e2862-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

