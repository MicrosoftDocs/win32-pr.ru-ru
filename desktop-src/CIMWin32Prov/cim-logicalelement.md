---
description: Класс CIM \_ логикалелемент является базовым классом для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: Класс CIM_LogicalElement (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895533"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="5fbd8-103">Класс CIM_LogicalElement (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="5fbd8-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5fbd8-104">Класс **CIM \_ логикалелемент** является базовым классом для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fbd8-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5fbd8-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5fbd8-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5fbd8-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbd8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fbd8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="5fbd8-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5fbd8-110">Members</span></span>

<span data-ttu-id="5fbd8-111">Класс **CIM \_ логикалелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5fbd8-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="5fbd8-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fbd8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fbd8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fbd8-113">Properties</span></span>

<span data-ttu-id="5fbd8-114">Класс **CIM \_ логикалелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fbd8-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fbd8-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fbd8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5fbd8-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-119">A short textual description of the object.</span></span>

<span data-ttu-id="5fbd8-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fbd8-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fbd8-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fbd8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-124">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5fbd8-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-125">A textual description of the object.</span></span>

<span data-ttu-id="5fbd8-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fbd8-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fbd8-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fbd8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5fbd8-131">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-131">Indicates when the object was installed.</span></span> <span data-ttu-id="5fbd8-132">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5fbd8-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fbd8-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fbd8-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fbd8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-137">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5fbd8-138">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-138">Label by which the object is known.</span></span> <span data-ttu-id="5fbd8-139">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5fbd8-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fbd8-141">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fbd8-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fbd8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fbd8-144">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5fbd8-145">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="5fbd8-146">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5fbd8-147">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="5fbd8-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5fbd8-148">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5fbd8-149">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="5fbd8-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5fbd8-150">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5fbd8-151">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5fbd8-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5fbd8-153">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="5fbd8-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5fbd8-154">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5fbd8-155">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5fbd8-156">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="5fbd8-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5fbd8-157">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5fbd8-158">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5fbd8-159">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5fbd8-160">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5fbd8-161">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5fbd8-162">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5fbd8-163">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5fbd8-164">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5fbd8-165">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="5fbd8-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5fbd8-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5fbd8-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5fbd8-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fbd8-167">Remarks</span></span>

<span data-ttu-id="5fbd8-168">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-168">WMI does not implement this class.</span></span> <span data-ttu-id="5fbd8-169">Классы, производные от **CIM \_ логикалелемент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5fbd8-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5fbd8-170">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5fbd8-171">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5fbd8-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbd8-172">Требования</span><span class="sxs-lookup"><span data-stu-id="5fbd8-172">Requirements</span></span>



| <span data-ttu-id="5fbd8-173">Требование</span><span class="sxs-lookup"><span data-stu-id="5fbd8-173">Requirement</span></span> | <span data-ttu-id="5fbd8-174">Значение</span><span class="sxs-lookup"><span data-stu-id="5fbd8-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbd8-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fbd8-175">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbd8-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fbd8-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5fbd8-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fbd8-177">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbd8-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fbd8-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5fbd8-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5fbd8-179">Namespace</span></span><br/>                | <span data-ttu-id="5fbd8-180">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5fbd8-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5fbd8-181">MOF</span><span class="sxs-lookup"><span data-stu-id="5fbd8-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fbd8-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fbd8-183">DLL</span><span class="sxs-lookup"><span data-stu-id="5fbd8-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fbd8-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbd8-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbd8-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fbd8-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbd8-186">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="5fbd8-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

