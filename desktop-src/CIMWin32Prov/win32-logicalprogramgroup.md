---
description: '&Win32 \_ логикалпрограмграуп \# 8194; Класс WMI представляет группу программ в компьютерной системе под Windows. Например, аксессуары или Startup.'
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Класс Win32_LogicalProgramGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896269"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="e629d-104">\_Класс Win32 логикалпрограмграуп</span><span class="sxs-lookup"><span data-stu-id="e629d-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="e629d-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ логикалпрограмграуп для Win32** представляет группу программ в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="e629d-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="e629d-106">Например, аксессуары или Startup.</span><span class="sxs-lookup"><span data-stu-id="e629d-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="e629d-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e629d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e629d-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="e629d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e629d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e629d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="e629d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e629d-110">Members</span></span>

<span data-ttu-id="e629d-111">Класс **Win32 \_ логикалпрограмграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e629d-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="e629d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e629d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e629d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e629d-113">Properties</span></span>

<span data-ttu-id="e629d-114">Класс **Win32 \_ логикалпрограмграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e629d-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e629d-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e629d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e629d-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e629d-119">A short textual description of the object.</span></span>

<span data-ttu-id="e629d-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e629d-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e629d-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e629d-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-124">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e629d-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e629d-125">A textual description of the object.</span></span>

<span data-ttu-id="e629d-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e629d-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e629d-127">**Группа**</span><span class="sxs-lookup"><span data-stu-id="e629d-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| методы класса Win32API квбемпровидерглуе \| [**жеталлинстанцес**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="e629d-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-131">Имя группы программ Windows.</span><span class="sxs-lookup"><span data-stu-id="e629d-131">Name of the Windows program group.</span></span> <span data-ttu-id="e629d-132">Группы программ реализуются в виде файловых папок в Win32.</span><span class="sxs-lookup"><span data-stu-id="e629d-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="e629d-133">Пример: "стандартные служебные \\ программы"</span><span class="sxs-lookup"><span data-stu-id="e629d-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="e629d-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e629d-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e629d-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e629d-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-138">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="e629d-138">Indicates when the object was installed.</span></span> <span data-ttu-id="e629d-139">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="e629d-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e629d-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e629d-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e629d-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="e629d-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-144">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| квбемпровидерглуе методы класса \| [**жеталлинстанцес**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="e629d-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-145">Назначенное пользователем имя, за которым следует имя группы.</span><span class="sxs-lookup"><span data-stu-id="e629d-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="e629d-146">Группы программ реализуются в виде файловых папок в Win32.</span><span class="sxs-lookup"><span data-stu-id="e629d-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="e629d-147">Пример: "все пользователи: стандартные \\ Служебные программы"</span><span class="sxs-lookup"><span data-stu-id="e629d-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="e629d-148">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e629d-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e629d-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-152">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e629d-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="e629d-153">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="e629d-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e629d-154">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="e629d-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e629d-155">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="e629d-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e629d-156">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="e629d-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e629d-157">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="e629d-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e629d-158">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="e629d-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e629d-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e629d-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e629d-160">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e629d-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e629d-161">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e629d-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e629d-162">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e629d-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e629d-163">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e629d-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e629d-164">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e629d-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e629d-165">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e629d-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e629d-166">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e629d-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e629d-167">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e629d-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e629d-168">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e629d-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e629d-169">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e629d-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e629d-170">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e629d-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e629d-171">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e629d-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e629d-172">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e629d-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e629d-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="e629d-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e629d-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e629d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e629d-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e629d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e629d-176">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| методы класса Win32API квбемпровидерглуе \| [**жеталлинстанцес**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="e629d-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="e629d-177">Пользователи, которые имеют доступ к группе программ Windows.</span><span class="sxs-lookup"><span data-stu-id="e629d-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="e629d-178">Группы программ реализуются в виде файловых папок в Win32.</span><span class="sxs-lookup"><span data-stu-id="e629d-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="e629d-179">Пример: "все пользователи"</span><span class="sxs-lookup"><span data-stu-id="e629d-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e629d-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e629d-180">Remarks</span></span>

<span data-ttu-id="e629d-181">Класс **Win32 \_ логикалпрограмграуп** является производным от [**Win32 \_ програмграупоритем**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="e629d-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="e629d-182">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="e629d-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="e629d-183">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="e629d-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="e629d-184">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="e629d-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="e629d-185">Требования</span><span class="sxs-lookup"><span data-stu-id="e629d-185">Requirements</span></span>



| <span data-ttu-id="e629d-186">Требование</span><span class="sxs-lookup"><span data-stu-id="e629d-186">Requirement</span></span> | <span data-ttu-id="e629d-187">Значение</span><span class="sxs-lookup"><span data-stu-id="e629d-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e629d-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e629d-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e629d-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e629d-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e629d-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e629d-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e629d-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e629d-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e629d-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e629d-192">Namespace</span></span><br/>                | <span data-ttu-id="e629d-193">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e629d-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e629d-194">MOF</span><span class="sxs-lookup"><span data-stu-id="e629d-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e629d-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e629d-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e629d-196">DLL</span><span class="sxs-lookup"><span data-stu-id="e629d-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e629d-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e629d-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e629d-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e629d-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e629d-199">**\_Програмграупоритем Win32**</span><span class="sxs-lookup"><span data-stu-id="e629d-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="e629d-200">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e629d-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

