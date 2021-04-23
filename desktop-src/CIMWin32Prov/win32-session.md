---
description: '\_Класс сеанса Win32 определяет сведения о состоянии взаимодействия между пользователем и ресурсом, например компьютерной системой или сеансом терминала.'
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Класс Win32_Session
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072370"
---
# <a name="win32_session-class"></a><span data-ttu-id="d1bb5-103">\_Класс сеанса Win32</span><span class="sxs-lookup"><span data-stu-id="d1bb5-103">Win32\_Session class</span></span>

<span data-ttu-id="d1bb5-104">Класс **\_ сеанса Win32** определяет сведения о состоянии взаимодействия между пользователем и ресурсом, например компьютерной системой или сеансом терминала.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="d1bb5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1bb5-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bb5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1bb5-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="d1bb5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d1bb5-108">Members</span></span>

<span data-ttu-id="d1bb5-109">Класс **\_ сеанса Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1bb5-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="d1bb5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1bb5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1bb5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1bb5-111">Properties</span></span>

<span data-ttu-id="d1bb5-112">Класс **\_ сеанса Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1bb5-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-117">A short textual description of the object.</span></span>

<span data-ttu-id="d1bb5-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1bb5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-122">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-123">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-123">A textual description of the object.</span></span>

<span data-ttu-id="d1bb5-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1bb5-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-128">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-129">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-129">Indicates when the object was installed.</span></span> <span data-ttu-id="d1bb5-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1bb5-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1bb5-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-135">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-136">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-136">Label by which the object is known.</span></span> <span data-ttu-id="d1bb5-137">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d1bb5-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1bb5-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-142">Время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb5-143">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1bb5-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1bb5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1bb5-146">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1bb5-147">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1bb5-148">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1bb5-149">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="d1bb5-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1bb5-150">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1bb5-151">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="d1bb5-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1bb5-152">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1bb5-153">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d1bb5-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1bb5-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1bb5-155">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d1bb5-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1bb5-156">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1bb5-157">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1bb5-158">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d1bb5-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1bb5-159">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1bb5-160">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1bb5-161">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1bb5-162">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1bb5-163">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1bb5-164">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1bb5-165">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1bb5-166">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1bb5-167">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d1bb5-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d1bb5-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d1bb5-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d1bb5-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1bb5-169">Remarks</span></span>

<span data-ttu-id="d1bb5-170">Класс **\_ сеанса Win32** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1bb5-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1bb5-171">Требования</span><span class="sxs-lookup"><span data-stu-id="d1bb5-171">Requirements</span></span>



| <span data-ttu-id="d1bb5-172">Требование</span><span class="sxs-lookup"><span data-stu-id="d1bb5-172">Requirement</span></span> | <span data-ttu-id="d1bb5-173">Значение</span><span class="sxs-lookup"><span data-stu-id="d1bb5-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bb5-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1bb5-174">Minimum supported client</span></span><br/> | <span data-ttu-id="d1bb5-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1bb5-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1bb5-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1bb5-176">Minimum supported server</span></span><br/> | <span data-ttu-id="d1bb5-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1bb5-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1bb5-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1bb5-178">Namespace</span></span><br/>                | <span data-ttu-id="d1bb5-179">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1bb5-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1bb5-180">MOF</span><span class="sxs-lookup"><span data-stu-id="d1bb5-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1bb5-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1bb5-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1bb5-182">DLL</span><span class="sxs-lookup"><span data-stu-id="d1bb5-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1bb5-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1bb5-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bb5-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1bb5-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bb5-185">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="d1bb5-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
