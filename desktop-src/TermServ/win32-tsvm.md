---
title: Класс Win32_TSVm
description: Представляет удаленный рабочий стол виртуальную машину.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVm службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVm, описание
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672481"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="c685c-105">\_Класс Win32 тсвм</span><span class="sxs-lookup"><span data-stu-id="c685c-105">Win32\_TSVm class</span></span>

<span data-ttu-id="c685c-106">Представляет удаленный рабочий стол виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="c685c-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="c685c-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c685c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c685c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c685c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="c685c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c685c-109">Members</span></span>

<span data-ttu-id="c685c-110">Класс **Win32 \_ тсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c685c-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="c685c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c685c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c685c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c685c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c685c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c685c-113">Methods</span></span>

<span data-ttu-id="c685c-114">Класс **Win32 \_ тсвм** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c685c-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="c685c-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c685c-115">Method</span></span>                                                                | <span data-ttu-id="c685c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c685c-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="c685c-117">**думпвминфо**</span><span class="sxs-lookup"><span data-stu-id="c685c-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="c685c-118">Только в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="c685c-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="c685c-119">**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="c685c-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="c685c-120">Получение данных мониторинга сеанса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c685c-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="c685c-121">**куерйоффлинеинформатион**</span><span class="sxs-lookup"><span data-stu-id="c685c-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="c685c-122">Запрашивает свойства только в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="c685c-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="c685c-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="c685c-123">Properties</span></span>

<span data-ttu-id="c685c-124">Класс **Win32 \_ тсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c685c-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c685c-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c685c-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c685c-128">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c685c-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c685c-129">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="c685c-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c685c-130">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c685c-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c685c-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c685c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c685c-134">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c685c-134">Description of the object.</span></span>

<span data-ttu-id="c685c-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c685c-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c685c-136">**енлигхтментсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c685c-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c685c-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c685c-139">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c685c-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c685c-140">Большой двоичный объект XML, который содержит параметры просвещение для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c685c-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c685c-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c685c-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-142">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c685c-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c685c-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="c685c-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c685c-145">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c685c-145">The date the object was installed.</span></span> <span data-ttu-id="c685c-146">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c685c-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c685c-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c685c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c685c-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="c685c-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c685c-151">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c685c-151">The name of the object.</span></span>

<span data-ttu-id="c685c-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c685c-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c685c-153">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c685c-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c685c-156">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c685c-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c685c-157">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c685c-157">Current status of the object.</span></span> <span data-ttu-id="c685c-158">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="c685c-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c685c-159">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="c685c-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c685c-160">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="c685c-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c685c-161">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="c685c-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c685c-162">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c685c-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c685c-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c685c-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c685c-164">("ОК")</span><span class="sxs-lookup"><span data-stu-id="c685c-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-165">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="c685c-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-166">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="c685c-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-167">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c685c-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-168">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c685c-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-169">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c685c-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-170">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="c685c-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c685c-171">("Служба")</span><span class="sxs-lookup"><span data-stu-id="c685c-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c685c-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="c685c-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c685c-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c685c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c685c-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c685c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c685c-175">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c685c-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c685c-176">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c685c-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c685c-177">Требования</span><span class="sxs-lookup"><span data-stu-id="c685c-177">Requirements</span></span>



| <span data-ttu-id="c685c-178">Требование</span><span class="sxs-lookup"><span data-stu-id="c685c-178">Requirement</span></span> | <span data-ttu-id="c685c-179">Значение</span><span class="sxs-lookup"><span data-stu-id="c685c-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c685c-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c685c-180">Minimum supported client</span></span><br/> | <span data-ttu-id="c685c-181">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c685c-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="c685c-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c685c-182">Minimum supported server</span></span><br/> | <span data-ttu-id="c685c-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c685c-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="c685c-184">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c685c-184">Namespace</span></span><br/>                | <span data-ttu-id="c685c-185">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c685c-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="c685c-186">MOF</span><span class="sxs-lookup"><span data-stu-id="c685c-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c685c-187"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c685c-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c685c-188">DLL</span><span class="sxs-lookup"><span data-stu-id="c685c-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c685c-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c685c-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

