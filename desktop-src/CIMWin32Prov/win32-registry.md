---
description: Реестр Win32 \_&\# 8194; Класс WMI представляет системный реестр в компьютерной системе под Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Класс Win32_Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990410"
---
# <a name="win32_registry-class"></a><span data-ttu-id="0ba3d-103">\_Класс реестра Win32</span><span class="sxs-lookup"><span data-stu-id="0ba3d-103">Win32\_Registry class</span></span>

<span data-ttu-id="0ba3d-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ реестра Win32** представляет системный реестр в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="0ba3d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0ba3d-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba3d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ba3d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="0ba3d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0ba3d-108">Members</span></span>

<span data-ttu-id="0ba3d-109">Класс **\_ реестра Win32** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0ba3d-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="0ba3d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ba3d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ba3d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ba3d-111">Properties</span></span>

<span data-ttu-id="0ba3d-112">Класс **\_ реестра Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ba3d-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-117">A short textual description of the object.</span></span>

<span data-ttu-id="0ba3d-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-122">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \|NTDLL.DLL\| [**Нткуерисистеминформатион**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| системрегистрикуотаинформатион"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-123">Текущий физический размер реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="0ba3d-124">Пример: 10</span><span class="sxs-lookup"><span data-stu-id="0ba3d-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-128">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-129">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-129">A textual description of the object.</span></span>

<span data-ttu-id="0ba3d-130">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-132">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-134">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-135">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-135">Indicates when the object was installed.</span></span> <span data-ttu-id="0ba3d-136">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0ba3d-137">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-141">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| регистрисизелимит"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-142">Максимальный размер реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="0ba3d-143">Если система успешно использует свойство **пропоседсизе** , **MaximumSize** должно содержать то же значение.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-147">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-148">Имя реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-148">Name of the Windows registry.</span></span> <span data-ttu-id="0ba3d-149">Максимальная длина составляет 256 символов.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-150">**пропоседсизе**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0ba3d-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-153">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| регистрисизелимит"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-154">Предложенный размер реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="0ba3d-155">Это единственный параметр реестра, который можно изменить, и его предложение предпринимается при следующем запуске системы.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="0ba3d-156">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba3d-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ba3d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ba3d-159">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0ba3d-160">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="0ba3d-161">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0ba3d-162">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="0ba3d-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0ba3d-163">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0ba3d-164">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="0ba3d-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0ba3d-165">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0ba3d-166">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0ba3d-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0ba3d-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0ba3d-168">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="0ba3d-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0ba3d-169">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0ba3d-170">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0ba3d-171">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="0ba3d-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ba3d-172">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0ba3d-173">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0ba3d-174">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0ba3d-175">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0ba3d-176">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0ba3d-177">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0ba3d-178">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0ba3d-179">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0ba3d-180">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="0ba3d-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="0ba3d-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ba3d-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0ba3d-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ba3d-182">Remarks</span></span>

<span data-ttu-id="0ba3d-183">Класс **\_ реестра Win32** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ba3d-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba3d-184">Требования</span><span class="sxs-lookup"><span data-stu-id="0ba3d-184">Requirements</span></span>



| <span data-ttu-id="0ba3d-185">Требование</span><span class="sxs-lookup"><span data-stu-id="0ba3d-185">Requirement</span></span> | <span data-ttu-id="0ba3d-186">Значение</span><span class="sxs-lookup"><span data-stu-id="0ba3d-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba3d-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ba3d-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba3d-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ba3d-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ba3d-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ba3d-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba3d-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba3d-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ba3d-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ba3d-191">Namespace</span></span><br/>                | <span data-ttu-id="0ba3d-192">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0ba3d-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0ba3d-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0ba3d-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ba3d-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ba3d-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ba3d-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba3d-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba3d-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba3d-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba3d-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ba3d-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba3d-198">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="0ba3d-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="0ba3d-199">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="0ba3d-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
