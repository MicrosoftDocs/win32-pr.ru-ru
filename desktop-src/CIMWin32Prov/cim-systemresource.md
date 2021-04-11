---
description: Класс CIM \_ системресаурце представляет сущность, управляемую BIOS, или операционную систему, доступную для использования программным обеспечением и логическими устройствами.
ms.assetid: f232c940-532d-4723-8e1e-09f983664b84
ms.tgt_platform: multiple
title: Класс CIM_SystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemResource
- CIM_SystemResource.Caption
- CIM_SystemResource.Description
- CIM_SystemResource.InstallDate
- CIM_SystemResource.Name
- CIM_SystemResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0c111aa0d69119a7d9182732fb18dd5109d3dde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262687"
---
# <a name="cim_systemresource-class"></a><span data-ttu-id="36c3b-103">\_Класс CIM системресаурце</span><span class="sxs-lookup"><span data-stu-id="36c3b-103">CIM\_SystemResource class</span></span>

<span data-ttu-id="36c3b-104">Класс **CIM \_ системресаурце** представляет сущность, управляемую BIOS, или операционную систему, доступную для использования программным обеспечением и логическими устройствами.</span><span class="sxs-lookup"><span data-stu-id="36c3b-104">The **CIM\_SystemResource** class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36c3b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="36c3b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36c3b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36c3b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36c3b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="36c3b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="36c3b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="36c3b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36c3b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C519-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SystemResource : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="36c3b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="36c3b-110">Members</span></span>

<span data-ttu-id="36c3b-111">Класс **CIM \_ системресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="36c3b-111">The **CIM\_SystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="36c3b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="36c3b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36c3b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="36c3b-113">Properties</span></span>

<span data-ttu-id="36c3b-114">Класс **CIM \_ системресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="36c3b-114">The **CIM\_SystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36c3b-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="36c3b-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c3b-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="36c3b-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36c3b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="36c3b-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="36c3b-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="36c3b-119">A short textual description of the object.</span></span>

<span data-ttu-id="36c3b-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36c3b-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36c3b-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c3b-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="36c3b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36c3b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-124">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="36c3b-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="36c3b-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="36c3b-125">A textual description of the object.</span></span>

<span data-ttu-id="36c3b-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36c3b-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36c3b-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c3b-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="36c3b-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36c3b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="36c3b-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="36c3b-131">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="36c3b-131">Indicates when the object was installed.</span></span> <span data-ttu-id="36c3b-132">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="36c3b-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="36c3b-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36c3b-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="36c3b-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c3b-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="36c3b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36c3b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-137">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="36c3b-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="36c3b-138">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="36c3b-138">Label by which the object is known.</span></span> <span data-ttu-id="36c3b-139">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="36c3b-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="36c3b-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36c3b-141">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="36c3b-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36c3b-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="36c3b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36c3b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36c3b-144">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="36c3b-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="36c3b-145">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="36c3b-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="36c3b-146">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="36c3b-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="36c3b-147">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="36c3b-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="36c3b-148">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="36c3b-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="36c3b-149">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="36c3b-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="36c3b-150">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="36c3b-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="36c3b-151">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="36c3b-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="36c3b-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="36c3b-153">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="36c3b-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="36c3b-154">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="36c3b-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="36c3b-155">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="36c3b-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36c3b-156">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="36c3b-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36c3b-157">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="36c3b-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="36c3b-158">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="36c3b-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="36c3b-159">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="36c3b-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="36c3b-160">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="36c3b-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="36c3b-161">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="36c3b-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="36c3b-162">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="36c3b-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="36c3b-163">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="36c3b-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="36c3b-164">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="36c3b-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="36c3b-165">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="36c3b-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="36c3b-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36c3b-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="36c3b-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36c3b-167">Remarks</span></span>

<span data-ttu-id="36c3b-168">Класс **CIM \_ системресаурце** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-168">The **CIM\_SystemResource** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="36c3b-169">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="36c3b-169">WMI does not implement this class.</span></span> <span data-ttu-id="36c3b-170">Классы WMI, производные от **CIM \_ системресаурце**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36c3b-170">For WMI classes derived from **CIM\_SystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="36c3b-171">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="36c3b-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36c3b-172">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="36c3b-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c3b-173">Требования</span><span class="sxs-lookup"><span data-stu-id="36c3b-173">Requirements</span></span>



| <span data-ttu-id="36c3b-174">Требование</span><span class="sxs-lookup"><span data-stu-id="36c3b-174">Requirement</span></span> | <span data-ttu-id="36c3b-175">Значение</span><span class="sxs-lookup"><span data-stu-id="36c3b-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36c3b-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c3b-176">Minimum supported client</span></span><br/> | <span data-ttu-id="36c3b-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36c3b-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36c3b-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c3b-178">Minimum supported server</span></span><br/> | <span data-ttu-id="36c3b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36c3b-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36c3b-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36c3b-180">Namespace</span></span><br/>                | <span data-ttu-id="36c3b-181">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="36c3b-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36c3b-182">MOF</span><span class="sxs-lookup"><span data-stu-id="36c3b-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36c3b-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36c3b-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36c3b-184">DLL</span><span class="sxs-lookup"><span data-stu-id="36c3b-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c3b-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36c3b-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c3b-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36c3b-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c3b-187">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="36c3b-187">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

