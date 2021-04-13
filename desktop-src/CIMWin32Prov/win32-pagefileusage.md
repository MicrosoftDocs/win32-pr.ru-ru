---
description: '&Win32 \_ пажефилеусаже \# 8194; Класс WMI представляет файл, используемый для обработки обмена файлами виртуальной памяти в системе Win32. Сведения, содержащиеся в объектах, созданных из этого класса, указывают состояние файла подкачки во время выполнения.'
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Класс Win32_PageFileUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539224"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="10acc-104">\_Класс Win32 пажефилеусаже</span><span class="sxs-lookup"><span data-stu-id="10acc-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="10acc-105"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ пажефилеусаже для Win32** представляет файл, используемый для обработки обмена файлами виртуальной памяти в системе Win32.</span><span class="sxs-lookup"><span data-stu-id="10acc-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="10acc-106">Сведения, содержащиеся в объектах, созданных из этого класса, указывают состояние файла подкачки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="10acc-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="10acc-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="10acc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="10acc-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="10acc-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10acc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10acc-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="10acc-110">Члены</span><span class="sxs-lookup"><span data-stu-id="10acc-110">Members</span></span>

<span data-ttu-id="10acc-111">Класс **Win32 \_ пажефилеусаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="10acc-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="10acc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="10acc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10acc-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="10acc-113">Properties</span></span>

<span data-ttu-id="10acc-114">Класс **Win32 \_ пажефилеусаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="10acc-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10acc-115">**аллокатедбасесизе**</span><span class="sxs-lookup"><span data-stu-id="10acc-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10acc-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-118">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| двтоталпажефиле"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="10acc-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-119">Фактический объем дискового пространства, выделенный для использования с этим файлом страницы.</span><span class="sxs-lookup"><span data-stu-id="10acc-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="10acc-120">Это значение соответствует диапазону, установленному в [**Win32 \_ пажефилесеттинг**](win32-pagefilesetting.md) в свойствах **инитиалсизе** и **MaximumSize** , которые устанавливаются при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="10acc-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="10acc-121">Пример: 178</span><span class="sxs-lookup"><span data-stu-id="10acc-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="10acc-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="10acc-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10acc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-125">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="10acc-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-126">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="10acc-126">A short textual description of the object.</span></span>

<span data-ttu-id="10acc-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10acc-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10acc-128">**куррентусаже**</span><span class="sxs-lookup"><span data-stu-id="10acc-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10acc-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-131">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="10acc-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-132">Объем места на диске, занятый в настоящий момент файлом подкачки.</span><span class="sxs-lookup"><span data-stu-id="10acc-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="10acc-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10acc-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10acc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-136">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="10acc-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-137">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="10acc-137">A textual description of the object.</span></span>

<span data-ttu-id="10acc-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10acc-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10acc-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10acc-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10acc-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-142">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="10acc-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-143">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="10acc-143">Indicates when the object was installed.</span></span> <span data-ttu-id="10acc-144">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="10acc-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="10acc-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10acc-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10acc-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="10acc-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10acc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-149">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="10acc-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-150">Имя файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="10acc-150">Name of the page file.</span></span>

<span data-ttu-id="10acc-151">Пример: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="10acc-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="10acc-152">**пеакусаже**</span><span class="sxs-lookup"><span data-stu-id="10acc-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10acc-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-155">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="10acc-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-156">Файл подкачки с наибольшим использованием.</span><span class="sxs-lookup"><span data-stu-id="10acc-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="10acc-157">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="10acc-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10acc-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-160">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="10acc-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-161">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="10acc-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="10acc-162">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="10acc-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="10acc-163">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="10acc-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="10acc-164">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="10acc-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="10acc-165">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="10acc-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="10acc-166">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="10acc-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10acc-167">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="10acc-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="10acc-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10acc-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="10acc-169">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="10acc-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10acc-170">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="10acc-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="10acc-171">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="10acc-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10acc-172">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="10acc-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10acc-173">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="10acc-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="10acc-174">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="10acc-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="10acc-175">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="10acc-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="10acc-176">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="10acc-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="10acc-177">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="10acc-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="10acc-178">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="10acc-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="10acc-179">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="10acc-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="10acc-180">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="10acc-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="10acc-181">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="10acc-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10acc-182">**темппажефиле**</span><span class="sxs-lookup"><span data-stu-id="10acc-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10acc-183">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10acc-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10acc-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10acc-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10acc-185">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Управление \\ \\ \\ \\ памятью диспетчер сеансов \| темппажефиле")</span><span class="sxs-lookup"><span data-stu-id="10acc-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="10acc-186">**Значение true** показывает, что временный файл подкачки был создан, обычно потому, что в текущей компьютерной системе нет постоянного файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="10acc-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10acc-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10acc-187">Remarks</span></span>

<span data-ttu-id="10acc-188">Класс **Win32 \_ пажефилеусаже** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="10acc-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10acc-189">Требования</span><span class="sxs-lookup"><span data-stu-id="10acc-189">Requirements</span></span>



| <span data-ttu-id="10acc-190">Требование</span><span class="sxs-lookup"><span data-stu-id="10acc-190">Requirement</span></span> | <span data-ttu-id="10acc-191">Значение</span><span class="sxs-lookup"><span data-stu-id="10acc-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10acc-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10acc-192">Minimum supported client</span></span><br/> | <span data-ttu-id="10acc-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10acc-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10acc-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10acc-194">Minimum supported server</span></span><br/> | <span data-ttu-id="10acc-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10acc-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10acc-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10acc-196">Namespace</span></span><br/>                | <span data-ttu-id="10acc-197">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10acc-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10acc-198">MOF</span><span class="sxs-lookup"><span data-stu-id="10acc-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10acc-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10acc-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10acc-200">DLL</span><span class="sxs-lookup"><span data-stu-id="10acc-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10acc-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10acc-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10acc-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10acc-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10acc-203">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="10acc-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="10acc-204">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="10acc-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
