---
description: Класс CIM \_ клустерингсап представляет точки доступа службы кластеров.
ms.assetid: 7a95f4b0-b9fc-4dba-ad2d-1b6db1539a57
ms.tgt_platform: multiple
title: Класс CIM_ClusteringSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringSAP
- CIM_ClusteringSAP.Caption
- CIM_ClusteringSAP.Description
- CIM_ClusteringSAP.InstallDate
- CIM_ClusteringSAP.Status
- CIM_ClusteringSAP.CreationClassName
- CIM_ClusteringSAP.Name
- CIM_ClusteringSAP.SystemCreationClassName
- CIM_ClusteringSAP.SystemName
- CIM_ClusteringSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc2d0296201e06382563cc3a0c34fec4d668cd58
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262689"
---
# <a name="cim_clusteringsap-class"></a><span data-ttu-id="f39bf-103">\_Класс CIM клустерингсап</span><span class="sxs-lookup"><span data-stu-id="f39bf-103">CIM\_ClusteringSAP class</span></span>

<span data-ttu-id="f39bf-104">Класс **CIM \_ клустерингсап** представляет точки доступа службы кластеров.</span><span class="sxs-lookup"><span data-stu-id="f39bf-104">The **CIM\_ClusteringSAP** class represents the access points of a clustering service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f39bf-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f39bf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f39bf-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f39bf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f39bf-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f39bf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f39bf-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f39bf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39bf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f39bf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2bb2b772-ffed-4aa6-b1b3-3d0cb74fc613}"), AMENDMENT]
class CIM_ClusteringSAP : CIM_ServiceAccessPoint
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

## <a name="members"></a><span data-ttu-id="f39bf-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f39bf-110">Members</span></span>

<span data-ttu-id="f39bf-111">Класс **CIM \_ клустерингсап** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f39bf-111">The **CIM\_ClusteringSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="f39bf-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f39bf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f39bf-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f39bf-113">Properties</span></span>

<span data-ttu-id="f39bf-114">Класс **CIM \_ клустерингсап** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f39bf-114">The **CIM\_ClusteringSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f39bf-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f39bf-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f39bf-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f39bf-119">A short textual description of the object.</span></span>

<span data-ttu-id="f39bf-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f39bf-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-124">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f39bf-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-125">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f39bf-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f39bf-126">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f39bf-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f39bf-127">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f39bf-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-131">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f39bf-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-132">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f39bf-132">A textual description of the object.</span></span>

<span data-ttu-id="f39bf-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f39bf-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f39bf-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f39bf-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-138">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="f39bf-138">Indicates when the object was installed.</span></span> <span data-ttu-id="f39bf-139">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f39bf-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f39bf-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="f39bf-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-144">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f39bf-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-145">Уникально идентифицирует точку доступа службы и предоставляет сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="f39bf-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="f39bf-146">Эти функциональные возможности более подробно описаны в свойстве «описание» объекта.</span><span class="sxs-lookup"><span data-stu-id="f39bf-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="f39bf-147">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-148">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f39bf-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f39bf-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-152">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f39bf-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="f39bf-153">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="f39bf-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f39bf-154">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="f39bf-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f39bf-155">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="f39bf-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f39bf-156">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="f39bf-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f39bf-157">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="f39bf-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f39bf-158">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f39bf-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f39bf-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f39bf-160">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f39bf-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f39bf-161">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f39bf-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f39bf-162">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f39bf-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f39bf-163">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f39bf-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f39bf-164">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f39bf-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f39bf-165">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f39bf-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f39bf-166">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f39bf-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f39bf-167">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f39bf-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f39bf-168">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f39bf-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f39bf-169">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f39bf-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f39bf-170">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f39bf-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f39bf-171">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f39bf-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f39bf-172">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f39bf-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f39bf-173">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f39bf-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-176">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f39bf-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-177">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f39bf-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="f39bf-178">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f39bf-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f39bf-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-182">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f39bf-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-183">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="f39bf-183">The scoping system's name.</span></span>

<span data-ttu-id="f39bf-184">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f39bf-185">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f39bf-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39bf-186">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f39bf-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f39bf-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39bf-188">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f39bf-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f39bf-189">Тип SAP, например "подключено" или "перенаправлено".</span><span class="sxs-lookup"><span data-stu-id="f39bf-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="f39bf-190">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f39bf-191">**Запись** (1)</span><span class="sxs-lookup"><span data-stu-id="f39bf-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f39bf-192">**Чтение** (2)</span><span class="sxs-lookup"><span data-stu-id="f39bf-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="f39bf-193">**Перенаправлено** (4)</span><span class="sxs-lookup"><span data-stu-id="f39bf-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="f39bf-194">**Команда NET \_ Подключено** (8)</span><span class="sxs-lookup"><span data-stu-id="f39bf-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f39bf-195">**неизвестно** (16)</span><span class="sxs-lookup"><span data-stu-id="f39bf-195">**unknown** (16)</span></span>


<span data-ttu-id="f39bf-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f39bf-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f39bf-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f39bf-197">Remarks</span></span>

<span data-ttu-id="f39bf-198">Класс **CIM \_ клустерингсап** является производным от [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f39bf-198">The **CIM\_ClusteringSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="f39bf-199">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f39bf-199">WMI does not implement this class.</span></span>

<span data-ttu-id="f39bf-200">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f39bf-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f39bf-201">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f39bf-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39bf-202">Требования</span><span class="sxs-lookup"><span data-stu-id="f39bf-202">Requirements</span></span>



| <span data-ttu-id="f39bf-203">Требование</span><span class="sxs-lookup"><span data-stu-id="f39bf-203">Requirement</span></span> | <span data-ttu-id="f39bf-204">Значение</span><span class="sxs-lookup"><span data-stu-id="f39bf-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f39bf-205">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f39bf-205">Minimum supported client</span></span><br/> | <span data-ttu-id="f39bf-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f39bf-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f39bf-207">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f39bf-207">Minimum supported server</span></span><br/> | <span data-ttu-id="f39bf-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f39bf-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f39bf-209">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f39bf-209">Namespace</span></span><br/>                | <span data-ttu-id="f39bf-210">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f39bf-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f39bf-211">MOF</span><span class="sxs-lookup"><span data-stu-id="f39bf-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f39bf-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f39bf-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f39bf-213">DLL</span><span class="sxs-lookup"><span data-stu-id="f39bf-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f39bf-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f39bf-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f39bf-215">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f39bf-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39bf-216">**\_СЕРВИЦЕАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f39bf-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

