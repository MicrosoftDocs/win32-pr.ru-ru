---
description: Класс CIM \_ бутсервице представляет функциональные возможности, предоставляемые устройством или программным обеспечением или сетью, для загрузки операционной системы в единой компьютерной системе.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: Класс CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655953"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="a16d1-103">\_Класс CIM бутсервице</span><span class="sxs-lookup"><span data-stu-id="a16d1-103">CIM\_BootService class</span></span>

<span data-ttu-id="a16d1-104">Класс **CIM \_ бутсервице** представляет функциональные возможности, предоставляемые устройством или программным обеспечением или сетью, для загрузки операционной системы в единой компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="a16d1-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a16d1-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a16d1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a16d1-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a16d1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a16d1-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a16d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a16d1-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a16d1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a16d1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="a16d1-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a16d1-110">Members</span></span>

<span data-ttu-id="a16d1-111">Класс **CIM \_ бутсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a16d1-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="a16d1-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a16d1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a16d1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a16d1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a16d1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="a16d1-114">Methods</span></span>

<span data-ttu-id="a16d1-115">Класс **CIM \_ бутсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a16d1-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="a16d1-116">Метод</span><span class="sxs-lookup"><span data-stu-id="a16d1-116">Method</span></span>                                                               | <span data-ttu-id="a16d1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a16d1-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="a16d1-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a16d1-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="a16d1-119">Переводит службу в состояние запущено.</span><span class="sxs-lookup"><span data-stu-id="a16d1-119">Puts the service in the started state.</span></span> <span data-ttu-id="a16d1-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a16d1-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="a16d1-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a16d1-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="a16d1-122">Переводит службу в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="a16d1-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="a16d1-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a16d1-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a16d1-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="a16d1-124">Properties</span></span>

<span data-ttu-id="a16d1-125">Класс **CIM \_ бутсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a16d1-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a16d1-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a16d1-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a16d1-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-130">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a16d1-130">A short textual description of the object.</span></span>

<span data-ttu-id="a16d1-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a16d1-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-135">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="a16d1-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-136">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a16d1-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a16d1-137">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="a16d1-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a16d1-138">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a16d1-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-142">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="a16d1-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-143">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a16d1-143">A textual description of the object.</span></span>

<span data-ttu-id="a16d1-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a16d1-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a16d1-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a16d1-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-149">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="a16d1-149">Indicates when the object was installed.</span></span> <span data-ttu-id="a16d1-150">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="a16d1-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a16d1-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="a16d1-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a16d1-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-156">Свойство name однозначно идентифицирует службу и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="a16d1-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="a16d1-157">Эти функциональные возможности более подробно описаны в свойстве « **Описание** » объекта.</span><span class="sxs-lookup"><span data-stu-id="a16d1-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="a16d1-158">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-159">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="a16d1-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-160">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a16d1-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-162">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="a16d1-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-163">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="a16d1-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="a16d1-164">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="a16d1-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-168">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="a16d1-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-169">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="a16d1-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="a16d1-170">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="a16d1-171">**Автоматически** ("автоматически")</span><span class="sxs-lookup"><span data-stu-id="a16d1-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="a16d1-172">**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="a16d1-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a16d1-173">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a16d1-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-176">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a16d1-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-177">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a16d1-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="a16d1-178">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="a16d1-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a16d1-179">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="a16d1-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a16d1-180">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="a16d1-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a16d1-181">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="a16d1-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a16d1-182">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="a16d1-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a16d1-183">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a16d1-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a16d1-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a16d1-185">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a16d1-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a16d1-186">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a16d1-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a16d1-187">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a16d1-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a16d1-188">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a16d1-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a16d1-189">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a16d1-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a16d1-190">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a16d1-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a16d1-191">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a16d1-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a16d1-192">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a16d1-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a16d1-193">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a16d1-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a16d1-194">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a16d1-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a16d1-195">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a16d1-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a16d1-196">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a16d1-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a16d1-197">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a16d1-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a16d1-198">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a16d1-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-201">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="a16d1-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-202">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a16d1-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="a16d1-203">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16d1-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a16d1-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16d1-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a16d1-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a16d1-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16d1-207">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="a16d1-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a16d1-208">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="a16d1-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="a16d1-209">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a16d1-210">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a16d1-210">Remarks</span></span>

<span data-ttu-id="a16d1-211">Класс **CIM \_ бутсервице** является производным от [**\_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a16d1-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="a16d1-212">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a16d1-212">WMI does not implement this class.</span></span>

<span data-ttu-id="a16d1-213">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a16d1-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a16d1-214">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a16d1-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16d1-215">Требования</span><span class="sxs-lookup"><span data-stu-id="a16d1-215">Requirements</span></span>



| <span data-ttu-id="a16d1-216">Требование</span><span class="sxs-lookup"><span data-stu-id="a16d1-216">Requirement</span></span> | <span data-ttu-id="a16d1-217">Значение</span><span class="sxs-lookup"><span data-stu-id="a16d1-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16d1-218">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a16d1-218">Minimum supported client</span></span><br/> | <span data-ttu-id="a16d1-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a16d1-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a16d1-220">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a16d1-220">Minimum supported server</span></span><br/> | <span data-ttu-id="a16d1-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a16d1-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a16d1-222">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a16d1-222">Namespace</span></span><br/>                | <span data-ttu-id="a16d1-223">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a16d1-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a16d1-224">MOF</span><span class="sxs-lookup"><span data-stu-id="a16d1-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a16d1-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a16d1-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a16d1-226">DLL</span><span class="sxs-lookup"><span data-stu-id="a16d1-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16d1-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16d1-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a16d1-228">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a16d1-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16d1-229">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="a16d1-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

