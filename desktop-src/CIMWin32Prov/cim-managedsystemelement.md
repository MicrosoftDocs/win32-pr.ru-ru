---
description: Класс CIM \_ манажедсистемелемент является базовым классом для иерархии системных элементов. Любой различимый системный компонент является кандидатом для включения в этот класс.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: Класс CIM_ManagedSystemElement (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141692"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="fbf38-104">Класс CIM_ManagedSystemElement (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="fbf38-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fbf38-105">Класс **CIM \_ манажедсистемелемент** является базовым классом для иерархии системных элементов.</span><span class="sxs-lookup"><span data-stu-id="fbf38-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="fbf38-106">Любой различимый системный компонент является кандидатом для включения в этот класс.</span><span class="sxs-lookup"><span data-stu-id="fbf38-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="fbf38-107">Примеры включают в себя программные компоненты, такие как файлы; устройства, такие как дисковые накопители и контроллеры; и физические компоненты, такие как микросхемы и карты.</span><span class="sxs-lookup"><span data-stu-id="fbf38-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbf38-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fbf38-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fbf38-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fbf38-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fbf38-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fbf38-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fbf38-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fbf38-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf38-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbf38-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="fbf38-113">Члены</span><span class="sxs-lookup"><span data-stu-id="fbf38-113">Members</span></span>

<span data-ttu-id="fbf38-114">Класс **CIM \_ манажедсистемелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fbf38-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="fbf38-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fbf38-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbf38-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="fbf38-116">Properties</span></span>

<span data-ttu-id="fbf38-117">Класс **CIM \_ манажедсистемелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fbf38-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbf38-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="fbf38-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf38-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fbf38-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf38-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fbf38-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fbf38-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fbf38-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="fbf38-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbf38-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf38-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fbf38-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf38-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-126">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="fbf38-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fbf38-127">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fbf38-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="fbf38-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fbf38-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf38-129">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fbf38-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf38-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="fbf38-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fbf38-132">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="fbf38-132">Indicates when the object was installed.</span></span> <span data-ttu-id="fbf38-133">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="fbf38-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="fbf38-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="fbf38-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf38-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fbf38-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf38-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-137">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="fbf38-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fbf38-138">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="fbf38-138">Label by which the object is known.</span></span> <span data-ttu-id="fbf38-139">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="fbf38-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="fbf38-140">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="fbf38-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf38-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fbf38-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fbf38-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf38-143">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="fbf38-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fbf38-144">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="fbf38-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="fbf38-145">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="fbf38-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fbf38-146">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="fbf38-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fbf38-147">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="fbf38-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fbf38-148">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="fbf38-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fbf38-149">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="fbf38-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fbf38-150">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="fbf38-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fbf38-151">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="fbf38-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fbf38-152">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="fbf38-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fbf38-153">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="fbf38-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fbf38-154">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="fbf38-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fbf38-155">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="fbf38-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fbf38-156">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="fbf38-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fbf38-157">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="fbf38-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fbf38-158">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="fbf38-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fbf38-159">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="fbf38-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fbf38-160">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="fbf38-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fbf38-161">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="fbf38-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fbf38-162">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="fbf38-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fbf38-163">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="fbf38-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="fbf38-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fbf38-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fbf38-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbf38-165">Remarks</span></span>

<span data-ttu-id="fbf38-166">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="fbf38-166">WMI does not implement this class.</span></span> <span data-ttu-id="fbf38-167">Классы WMI, производные от этого класса, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fbf38-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fbf38-168">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fbf38-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fbf38-169">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fbf38-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf38-170">Требования</span><span class="sxs-lookup"><span data-stu-id="fbf38-170">Requirements</span></span>



| <span data-ttu-id="fbf38-171">Требование</span><span class="sxs-lookup"><span data-stu-id="fbf38-171">Requirement</span></span> | <span data-ttu-id="fbf38-172">Значение</span><span class="sxs-lookup"><span data-stu-id="fbf38-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf38-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbf38-173">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf38-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbf38-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbf38-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbf38-175">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf38-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf38-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbf38-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbf38-177">Namespace</span></span><br/>                | <span data-ttu-id="fbf38-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fbf38-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fbf38-179">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf38-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf38-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf38-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf38-181">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf38-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf38-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf38-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

