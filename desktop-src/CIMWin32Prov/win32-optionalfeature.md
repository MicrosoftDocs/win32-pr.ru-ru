---
description: Представляет состояние дополнительных функций, имеющихся в операционной системе.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Класс Win32_OptionalFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656016"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="72254-103">\_Класс Win32 оптионалфеатуре</span><span class="sxs-lookup"><span data-stu-id="72254-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="72254-104">Представляет состояние дополнительных функций, имеющихся в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="72254-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="72254-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="72254-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72254-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72254-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="72254-107">Члены</span><span class="sxs-lookup"><span data-stu-id="72254-107">Members</span></span>

<span data-ttu-id="72254-108">Класс **Win32 \_ оптионалфеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72254-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="72254-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="72254-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72254-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="72254-110">Properties</span></span>

<span data-ttu-id="72254-111">Класс **Win32 \_ оптионалфеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="72254-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72254-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="72254-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72254-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72254-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72254-115">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) (заголовок), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="72254-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="72254-116">Необязательное отображаемое имя компонента.</span><span class="sxs-lookup"><span data-stu-id="72254-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="72254-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72254-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72254-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72254-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72254-120">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="72254-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="72254-121">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="72254-121">A textual description of the object.</span></span>

<span data-ttu-id="72254-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72254-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72254-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="72254-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-124">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="72254-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72254-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72254-126">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="72254-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="72254-127">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="72254-127">Indicates when the object was installed.</span></span> <span data-ttu-id="72254-128">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="72254-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="72254-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72254-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72254-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="72254-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72254-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72254-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72254-133">Определяет состояние необязательного компонента.</span><span class="sxs-lookup"><span data-stu-id="72254-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="72254-134">Возможны следующие состояния.</span><span class="sxs-lookup"><span data-stu-id="72254-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="72254-135">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="72254-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="72254-136">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="72254-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="72254-137">**Отсутствует** (3)</span><span class="sxs-lookup"><span data-stu-id="72254-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72254-138">**Неизвестно** (4)</span><span class="sxs-lookup"><span data-stu-id="72254-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72254-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="72254-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72254-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72254-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72254-142">Квалификаторы: [**Переопределение**](../wmisdk/standard-qualifiers.md) (имя), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="72254-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="72254-143">Представляет имя необязательного компонента.</span><span class="sxs-lookup"><span data-stu-id="72254-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="72254-144">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="72254-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72254-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="72254-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72254-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72254-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72254-147">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="72254-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="72254-148">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="72254-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="72254-149">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="72254-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="72254-150">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="72254-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="72254-151">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="72254-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="72254-152">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="72254-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="72254-153">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="72254-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="72254-154">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="72254-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="72254-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72254-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="72254-156">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="72254-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="72254-157">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="72254-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="72254-158">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="72254-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="72254-159">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="72254-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72254-160">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="72254-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="72254-161">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="72254-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="72254-162">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="72254-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="72254-163">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="72254-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="72254-164">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="72254-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="72254-165">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="72254-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="72254-166">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="72254-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="72254-167">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="72254-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="72254-168">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="72254-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="72254-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="72254-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="72254-170">Требования</span><span class="sxs-lookup"><span data-stu-id="72254-170">Requirements</span></span>



| <span data-ttu-id="72254-171">Требование</span><span class="sxs-lookup"><span data-stu-id="72254-171">Requirement</span></span> | <span data-ttu-id="72254-172">Значение</span><span class="sxs-lookup"><span data-stu-id="72254-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72254-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72254-173">Minimum supported client</span></span><br/> | <span data-ttu-id="72254-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72254-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="72254-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72254-175">Minimum supported server</span></span><br/> | <span data-ttu-id="72254-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72254-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="72254-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72254-177">Namespace</span></span><br/>                | <span data-ttu-id="72254-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="72254-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72254-179">MOF</span><span class="sxs-lookup"><span data-stu-id="72254-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72254-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72254-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72254-181">DLL</span><span class="sxs-lookup"><span data-stu-id="72254-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72254-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72254-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72254-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72254-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72254-184">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="72254-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="72254-185">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="72254-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="72254-186">Запрос состояния дополнительных функций</span><span class="sxs-lookup"><span data-stu-id="72254-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
