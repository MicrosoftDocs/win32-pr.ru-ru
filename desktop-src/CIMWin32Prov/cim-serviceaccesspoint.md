---
description: Класс CIM \_ сервицеакцесспоинт представляет возможность использования или вызова службы. Точки доступа представляют службы, доступные для использования другими сущностями.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: Класс CIM_ServiceAccessPoint (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538765"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="cafe2-104">Класс CIM_ServiceAccessPoint (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cafe2-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cafe2-105">Класс **CIM \_ сервицеакцесспоинт** представляет возможность использования или вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cafe2-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="cafe2-106">Точки доступа представляют службы, доступные для использования другими сущностями.</span><span class="sxs-lookup"><span data-stu-id="cafe2-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cafe2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cafe2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cafe2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cafe2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cafe2-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cafe2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cafe2-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cafe2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafe2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cafe2-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="cafe2-112">Члены</span><span class="sxs-lookup"><span data-stu-id="cafe2-112">Members</span></span>

<span data-ttu-id="cafe2-113">Класс **CIM \_ сервицеакцесспоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cafe2-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="cafe2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="cafe2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cafe2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="cafe2-115">Properties</span></span>

<span data-ttu-id="cafe2-116">Класс **CIM \_ сервицеакцесспоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cafe2-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cafe2-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cafe2-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cafe2-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cafe2-121">A short textual description of the object.</span></span>

<span data-ttu-id="cafe2-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cafe2-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-126">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cafe2-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cafe2-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cafe2-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="cafe2-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cafe2-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-132">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="cafe2-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-133">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cafe2-133">A textual description of the object.</span></span>

<span data-ttu-id="cafe2-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cafe2-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-136">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cafe2-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="cafe2-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-139">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="cafe2-139">Indicates when the object was installed.</span></span> <span data-ttu-id="cafe2-140">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="cafe2-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cafe2-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="cafe2-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-145">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cafe2-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-146">Уникально идентифицирует точку доступа службы и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="cafe2-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="cafe2-147">Эти функциональные возможности более подробно описаны в свойстве «описание» объекта.</span><span class="sxs-lookup"><span data-stu-id="cafe2-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-148">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="cafe2-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="cafe2-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-152">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="cafe2-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="cafe2-153">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="cafe2-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cafe2-154">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="cafe2-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cafe2-155">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="cafe2-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cafe2-156">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="cafe2-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cafe2-157">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="cafe2-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cafe2-158">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="cafe2-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cafe2-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cafe2-160">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="cafe2-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cafe2-161">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="cafe2-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cafe2-162">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="cafe2-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cafe2-163">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="cafe2-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe2-164">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="cafe2-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cafe2-165">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="cafe2-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cafe2-166">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="cafe2-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cafe2-167">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="cafe2-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cafe2-168">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="cafe2-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cafe2-169">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="cafe2-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cafe2-170">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="cafe2-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cafe2-171">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="cafe2-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cafe2-172">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="cafe2-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe2-173">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cafe2-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-176">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cafe2-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-177">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="cafe2-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cafe2-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cafe2-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-181">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cafe2-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-182">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="cafe2-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="cafe2-183">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cafe2-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe2-184">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe2-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cafe2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe2-186">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cafe2-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cafe2-187">Тип SAP, например "подключено" или "перенаправлено".</span><span class="sxs-lookup"><span data-stu-id="cafe2-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="cafe2-188">**Запись** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe2-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="cafe2-189">**Чтение** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe2-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="cafe2-190">**Перенаправлено** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe2-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="cafe2-191">**Команда NET \_ Подключено** (8)</span><span class="sxs-lookup"><span data-stu-id="cafe2-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe2-192">**неизвестно** (16)</span><span class="sxs-lookup"><span data-stu-id="cafe2-192">**unknown** (16)</span></span>


<span data-ttu-id="cafe2-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cafe2-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cafe2-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cafe2-194">Remarks</span></span>

<span data-ttu-id="cafe2-195">Класс **CIM \_ сервицеакцесспоинт** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="cafe2-196">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cafe2-196">WMI does not implement this class.</span></span> <span data-ttu-id="cafe2-197">Классы WMI, производные от **CIM \_ сервицеакцесспоинт**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cafe2-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cafe2-198">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cafe2-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cafe2-199">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cafe2-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cafe2-200">Требования</span><span class="sxs-lookup"><span data-stu-id="cafe2-200">Requirements</span></span>



| <span data-ttu-id="cafe2-201">Требование</span><span class="sxs-lookup"><span data-stu-id="cafe2-201">Requirement</span></span> | <span data-ttu-id="cafe2-202">Значение</span><span class="sxs-lookup"><span data-stu-id="cafe2-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cafe2-203">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cafe2-203">Minimum supported client</span></span><br/> | <span data-ttu-id="cafe2-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cafe2-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cafe2-205">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cafe2-205">Minimum supported server</span></span><br/> | <span data-ttu-id="cafe2-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cafe2-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cafe2-207">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cafe2-207">Namespace</span></span><br/>                | <span data-ttu-id="cafe2-208">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cafe2-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cafe2-209">MOF</span><span class="sxs-lookup"><span data-stu-id="cafe2-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cafe2-210"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cafe2-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cafe2-211">DLL</span><span class="sxs-lookup"><span data-stu-id="cafe2-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cafe2-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cafe2-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafe2-213">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cafe2-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafe2-214">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="cafe2-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

