---
description: '\_Абстрактный класс WMI Програмграупоритем Win32 представляет логическую группу программ в меню "Запуск программ" пользователя \\ . Он содержит группы программ и элементы группы программ.'
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Класс Win32_ProgramGroupOrItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141043"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="8c810-104">\_Класс Win32 програмграупоритем</span><span class="sxs-lookup"><span data-stu-id="8c810-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="8c810-105">Абстрактный [класс WMI](../wmisdk/retrieving-a-class.md) **\_ програмграупоритем Win32** представляет логическую группу программ в меню " **Запуск \\ программ** " пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c810-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="8c810-106">Он содержит группы программ и элементы группы программ.</span><span class="sxs-lookup"><span data-stu-id="8c810-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="8c810-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8c810-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8c810-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="8c810-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c810-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c810-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8c810-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8c810-110">Members</span></span>

<span data-ttu-id="8c810-111">Класс **Win32 \_ програмграупоритем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8c810-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="8c810-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c810-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c810-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c810-113">Properties</span></span>

<span data-ttu-id="8c810-114">Класс **Win32 \_ програмграупоритем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8c810-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c810-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8c810-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c810-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c810-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c810-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c810-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c810-118">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8c810-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8c810-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8c810-119">A short textual description of the object.</span></span>

<span data-ttu-id="8c810-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c810-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c810-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c810-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c810-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c810-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c810-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c810-124">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="8c810-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8c810-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8c810-125">A textual description of the object.</span></span>

<span data-ttu-id="8c810-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c810-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8c810-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c810-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c810-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c810-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c810-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c810-130">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="8c810-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8c810-131">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="8c810-131">Indicates when the object was installed.</span></span> <span data-ttu-id="8c810-132">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="8c810-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8c810-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c810-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c810-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c810-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c810-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c810-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c810-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c810-137">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="8c810-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8c810-138">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8c810-138">Label by which the object is known.</span></span> <span data-ttu-id="8c810-139">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="8c810-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8c810-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c810-141">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8c810-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c810-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8c810-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c810-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c810-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c810-144">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="8c810-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8c810-145">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8c810-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="8c810-146">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="8c810-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8c810-147">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="8c810-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8c810-148">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="8c810-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8c810-149">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="8c810-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8c810-150">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="8c810-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8c810-151">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="8c810-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8c810-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8c810-153">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="8c810-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8c810-154">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="8c810-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8c810-155">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="8c810-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c810-156">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="8c810-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c810-157">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8c810-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8c810-158">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8c810-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8c810-159">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8c810-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8c810-160">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="8c810-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8c810-161">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="8c810-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8c810-162">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="8c810-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8c810-163">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="8c810-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8c810-164">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="8c810-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8c810-165">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="8c810-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8c810-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8c810-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8c810-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c810-167">Remarks</span></span>

<span data-ttu-id="8c810-168">Класс **Win32 \_ програмграупоритем** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c810-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c810-169">Требования</span><span class="sxs-lookup"><span data-stu-id="8c810-169">Requirements</span></span>



| <span data-ttu-id="8c810-170">Требование</span><span class="sxs-lookup"><span data-stu-id="8c810-170">Requirement</span></span> | <span data-ttu-id="8c810-171">Значение</span><span class="sxs-lookup"><span data-stu-id="8c810-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c810-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c810-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8c810-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c810-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c810-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c810-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8c810-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c810-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c810-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8c810-176">Namespace</span></span><br/>                | <span data-ttu-id="8c810-177">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c810-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c810-178">MOF</span><span class="sxs-lookup"><span data-stu-id="8c810-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c810-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c810-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c810-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8c810-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c810-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c810-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c810-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c810-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c810-183">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="8c810-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="8c810-184">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="8c810-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
