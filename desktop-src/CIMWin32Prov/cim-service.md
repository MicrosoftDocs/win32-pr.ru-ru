---
description: '\_Класс службы CIM представляет логический элемент, который содержит сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.'
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: Класс CIM_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655826"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ae2b3-103">Класс CIM_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ae2b3-104">Класс **\_ службы CIM** представляет логический элемент, который содержит сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="ae2b3-105">Служба — это объект общего назначения для настройки и управления реализацией функциональности; Это не сама функциональность.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae2b3-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ae2b3-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ae2b3-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ae2b3-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2b3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae2b3-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="ae2b3-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ae2b3-111">Members</span></span>

<span data-ttu-id="ae2b3-112">Класс **\_ службы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ae2b3-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="ae2b3-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ae2b3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae2b3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae2b3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae2b3-115">Методы</span><span class="sxs-lookup"><span data-stu-id="ae2b3-115">Methods</span></span>

<span data-ttu-id="ae2b3-116">Класс **\_ службы CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="ae2b3-117">Метод</span><span class="sxs-lookup"><span data-stu-id="ae2b3-117">Method</span></span>                                                           | <span data-ttu-id="ae2b3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ae2b3-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2b3-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="ae2b3-120">Пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="ae2b3-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="ae2b3-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="ae2b3-123">Метод класса, который помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="ae2b3-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae2b3-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae2b3-125">Properties</span></span>

<span data-ttu-id="ae2b3-126">Класс **\_ службы CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae2b3-127">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-131">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-131">A short textual description of the object.</span></span>

<span data-ttu-id="ae2b3-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-136">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-137">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ae2b3-138">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-142">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-143">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-143">A textual description of the object.</span></span>

<span data-ttu-id="ae2b3-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-149">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-149">Indicates when the object was installed.</span></span> <span data-ttu-id="ae2b3-150">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ae2b3-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-155">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-156">Свойство name однозначно идентифицирует службу и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="ae2b3-157">Эти функциональные возможности более подробно описаны в свойстве «описание» объекта.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-158">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-159">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-161">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-162">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-166">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-167">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ae2b3-168">**Автоматически** ("автоматически")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="ae2b3-169">**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae2b3-170">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-173">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-174">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="ae2b3-175">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ae2b3-176">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="ae2b3-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ae2b3-177">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ae2b3-178">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="ae2b3-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ae2b3-179">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ae2b3-180">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ae2b3-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ae2b3-182">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="ae2b3-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ae2b3-183">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ae2b3-184">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae2b3-185">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae2b3-186">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ae2b3-187">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ae2b3-188">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ae2b3-189">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ae2b3-190">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ae2b3-191">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ae2b3-192">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ae2b3-193">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ae2b3-194">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae2b3-195">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-198">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-199">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="ae2b3-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae2b3-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae2b3-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae2b3-203">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="ae2b3-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae2b3-204">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae2b3-205">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae2b3-205">Remarks</span></span>

<span data-ttu-id="ae2b3-206">Класс **\_ службы CIM** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ae2b3-207">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-207">WMI does not implement this class.</span></span> <span data-ttu-id="ae2b3-208">Сведения о классах WMI, которые являются производными от **\_ службы CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ae2b3-209">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ae2b3-210">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2b3-211">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2b3-211">Requirements</span></span>



| <span data-ttu-id="ae2b3-212">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2b3-212">Requirement</span></span> | <span data-ttu-id="ae2b3-213">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2b3-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2b3-214">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae2b3-214">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2b3-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae2b3-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae2b3-216">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae2b3-216">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2b3-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae2b3-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae2b3-218">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ae2b3-218">Namespace</span></span><br/>                | <span data-ttu-id="ae2b3-219">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae2b3-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae2b3-220">MOF</span><span class="sxs-lookup"><span data-stu-id="ae2b3-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae2b3-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b3-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae2b3-222">DLL</span><span class="sxs-lookup"><span data-stu-id="ae2b3-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae2b3-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b3-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2b3-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae2b3-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2b3-225">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

