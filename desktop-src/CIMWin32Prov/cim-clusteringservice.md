---
description: Класс CIM \_ клустерингсервице представляет функциональные возможности, предоставляемые кластером. Например, возможность отработки отказа может быть смоделирована как служба отказоустойчивого кластера.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: Класс CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655947"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="cde0a-104">\_Класс CIM клустерингсервице</span><span class="sxs-lookup"><span data-stu-id="cde0a-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="cde0a-105">Класс **CIM \_ клустерингсервице** представляет функциональные возможности, предоставляемые кластером.</span><span class="sxs-lookup"><span data-stu-id="cde0a-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="cde0a-106">Например, возможность отработки отказа может быть смоделирована как служба отказоустойчивого кластера.</span><span class="sxs-lookup"><span data-stu-id="cde0a-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cde0a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cde0a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cde0a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cde0a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cde0a-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cde0a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cde0a-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cde0a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde0a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cde0a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="cde0a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="cde0a-112">Members</span></span>

<span data-ttu-id="cde0a-113">Класс **CIM \_ клустерингсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cde0a-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="cde0a-114">Методы</span><span class="sxs-lookup"><span data-stu-id="cde0a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cde0a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="cde0a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cde0a-116">Методы</span><span class="sxs-lookup"><span data-stu-id="cde0a-116">Methods</span></span>

<span data-ttu-id="cde0a-117">Класс **CIM \_ клустерингсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cde0a-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="cde0a-118">Метод</span><span class="sxs-lookup"><span data-stu-id="cde0a-118">Method</span></span>                                                                     | <span data-ttu-id="cde0a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="cde0a-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cde0a-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="cde0a-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="cde0a-121">Метод класса, который переносит новую компьютерную систему в кластер.</span><span class="sxs-lookup"><span data-stu-id="cde0a-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="cde0a-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cde0a-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="cde0a-123">**евиктноде**</span><span class="sxs-lookup"><span data-stu-id="cde0a-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="cde0a-124">Метод класса, который удаляет компьютерную систему из кластера.</span><span class="sxs-lookup"><span data-stu-id="cde0a-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="cde0a-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cde0a-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="cde0a-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="cde0a-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="cde0a-127">Метод класса, который пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="cde0a-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="cde0a-128">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cde0a-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="cde0a-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="cde0a-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="cde0a-130">Метод класса, который помещает службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="cde0a-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="cde0a-131">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cde0a-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="cde0a-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="cde0a-132">Properties</span></span>

<span data-ttu-id="cde0a-133">Класс **CIM \_ клустерингсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cde0a-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cde0a-134">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cde0a-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-137">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cde0a-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-138">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cde0a-138">A short textual description of the object.</span></span>

<span data-ttu-id="cde0a-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cde0a-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-143">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="cde0a-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-144">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cde0a-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cde0a-145">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="cde0a-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cde0a-146">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-147">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cde0a-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-150">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="cde0a-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-151">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cde0a-151">A textual description of the object.</span></span>

<span data-ttu-id="cde0a-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cde0a-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-154">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cde0a-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-156">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="cde0a-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-157">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="cde0a-157">Indicates when the object was installed.</span></span> <span data-ttu-id="cde0a-158">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="cde0a-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cde0a-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="cde0a-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-163">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cde0a-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-164">Свойство name однозначно идентифицирует службу и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="cde0a-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="cde0a-165">Эти функциональные возможности более подробно описаны в свойстве «описание» объекта.</span><span class="sxs-lookup"><span data-stu-id="cde0a-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="cde0a-166">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-167">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="cde0a-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cde0a-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-170">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="cde0a-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-171">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="cde0a-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="cde0a-172">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="cde0a-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-176">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="cde0a-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-177">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="cde0a-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="cde0a-178">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="cde0a-179">**Автоматически** ("автоматически")</span><span class="sxs-lookup"><span data-stu-id="cde0a-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="cde0a-180">**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="cde0a-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cde0a-181">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="cde0a-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-184">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="cde0a-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-185">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="cde0a-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="cde0a-186">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="cde0a-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cde0a-187">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="cde0a-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cde0a-188">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="cde0a-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cde0a-189">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="cde0a-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cde0a-190">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="cde0a-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cde0a-191">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="cde0a-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cde0a-192">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cde0a-193">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="cde0a-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cde0a-194">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="cde0a-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cde0a-195">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="cde0a-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cde0a-196">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="cde0a-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cde0a-197">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="cde0a-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cde0a-198">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="cde0a-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cde0a-199">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="cde0a-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cde0a-200">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="cde0a-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cde0a-201">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="cde0a-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cde0a-202">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="cde0a-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cde0a-203">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="cde0a-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cde0a-204">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="cde0a-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cde0a-205">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="cde0a-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cde0a-206">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cde0a-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-209">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="cde0a-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-210">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="cde0a-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="cde0a-211">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde0a-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cde0a-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde0a-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cde0a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cde0a-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde0a-215">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="cde0a-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="cde0a-216">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="cde0a-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="cde0a-217">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cde0a-218">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cde0a-218">Remarks</span></span>

<span data-ttu-id="cde0a-219">Класс **CIM \_ клустерингсервице** является производным от [**\_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="cde0a-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="cde0a-220">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cde0a-220">WMI does not implement this class.</span></span>

<span data-ttu-id="cde0a-221">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cde0a-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cde0a-222">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cde0a-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde0a-223">Требования</span><span class="sxs-lookup"><span data-stu-id="cde0a-223">Requirements</span></span>



| <span data-ttu-id="cde0a-224">Требование</span><span class="sxs-lookup"><span data-stu-id="cde0a-224">Requirement</span></span> | <span data-ttu-id="cde0a-225">Значение</span><span class="sxs-lookup"><span data-stu-id="cde0a-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde0a-226">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cde0a-226">Minimum supported client</span></span><br/> | <span data-ttu-id="cde0a-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cde0a-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cde0a-228">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cde0a-228">Minimum supported server</span></span><br/> | <span data-ttu-id="cde0a-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cde0a-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cde0a-230">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cde0a-230">Namespace</span></span><br/>                | <span data-ttu-id="cde0a-231">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cde0a-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cde0a-232">MOF</span><span class="sxs-lookup"><span data-stu-id="cde0a-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde0a-233"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde0a-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde0a-234">DLL</span><span class="sxs-lookup"><span data-stu-id="cde0a-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde0a-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde0a-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde0a-236">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cde0a-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde0a-237">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="cde0a-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

