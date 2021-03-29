---
title: Класс Win32_TSVmMetadataItem
description: Представляет элемент метаданных для удаленный рабочий стол виртуальной машины.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVmMetadataItem службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVmMetadataItem, описание
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988252"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="ed623-105">\_Класс Win32 тсвмметадатаитем</span><span class="sxs-lookup"><span data-stu-id="ed623-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="ed623-106">Представляет элемент метаданных для удаленный рабочий стол виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed623-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="ed623-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ed623-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed623-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed623-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="ed623-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ed623-109">Members</span></span>

<span data-ttu-id="ed623-110">Класс **Win32 \_ тсвмметадатаитем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed623-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="ed623-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed623-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed623-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed623-112">Properties</span></span>

<span data-ttu-id="ed623-113">Класс **Win32 \_ тсвмметадатаитем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ed623-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed623-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ed623-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed623-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ed623-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ed623-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="ed623-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ed623-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ed623-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed623-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed623-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed623-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ed623-123">Description of the object.</span></span>

<span data-ttu-id="ed623-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ed623-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed623-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ed623-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ed623-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed623-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="ed623-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ed623-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ed623-129">The date the object was installed.</span></span> <span data-ttu-id="ed623-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="ed623-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ed623-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ed623-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed623-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="ed623-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed623-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ed623-135">The name of the object.</span></span>

<span data-ttu-id="ed623-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ed623-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed623-137">**сектионид**</span><span class="sxs-lookup"><span data-stu-id="ed623-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed623-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed623-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed623-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed623-141">Указывает раздел в метаданных, в котором находится этот элемент.</span><span class="sxs-lookup"><span data-stu-id="ed623-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="ed623-142">0</span><span class="sxs-lookup"><span data-stu-id="ed623-142">0</span></span>
</dt> <dd>

<span data-ttu-id="ed623-143">Раздел конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ed623-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="ed623-144">1</span><span class="sxs-lookup"><span data-stu-id="ed623-144">1</span></span>
</dt> <dd>

<span data-ttu-id="ed623-145">Раздел параметров просвещение.</span><span class="sxs-lookup"><span data-stu-id="ed623-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ed623-146">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ed623-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed623-149">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ed623-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ed623-150">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ed623-150">Current status of the object.</span></span> <span data-ttu-id="ed623-151">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="ed623-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ed623-152">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="ed623-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ed623-153">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="ed623-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ed623-154">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="ed623-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ed623-155">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="ed623-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ed623-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ed623-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ed623-157">("ОК")</span><span class="sxs-lookup"><span data-stu-id="ed623-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-158">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="ed623-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-159">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="ed623-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-160">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ed623-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-161">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ed623-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-162">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ed623-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-163">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="ed623-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ed623-164">("Служба")</span><span class="sxs-lookup"><span data-stu-id="ed623-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ed623-165">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ed623-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed623-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ed623-168">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="ed623-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="ed623-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="ed623-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed623-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed623-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed623-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed623-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed623-172">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed623-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed623-173">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed623-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed623-174">Требования</span><span class="sxs-lookup"><span data-stu-id="ed623-174">Requirements</span></span>



| <span data-ttu-id="ed623-175">Требование</span><span class="sxs-lookup"><span data-stu-id="ed623-175">Requirement</span></span> | <span data-ttu-id="ed623-176">Значение</span><span class="sxs-lookup"><span data-stu-id="ed623-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed623-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed623-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ed623-178">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed623-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ed623-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed623-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ed623-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed623-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ed623-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed623-181">Namespace</span></span><br/>                | <span data-ttu-id="ed623-182">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ed623-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ed623-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ed623-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed623-184"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed623-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ed623-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ed623-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed623-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed623-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

