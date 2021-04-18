---
description: Представляет экземпляр компонента расширения, установленного в системе узла.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Класс Msvm_InstalledEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662513"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="c8e2d-103">\_Класс мсвм инсталледесернетсвитчекстенсион</span><span class="sxs-lookup"><span data-stu-id="c8e2d-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="c8e2d-104">Представляет экземпляр компонента расширения, установленного в системе узла.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="c8e2d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e2d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8e2d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="c8e2d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c8e2d-107">Members</span></span>

<span data-ttu-id="c8e2d-108">Класс **мсвм \_ инсталледесернетсвитчекстенсион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8e2d-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="c8e2d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8e2d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8e2d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8e2d-110">Properties</span></span>

<span data-ttu-id="c8e2d-111">Класс **мсвм \_ инсталледесернетсвитчекстенсион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8e2d-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-115">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-116">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-116">A short description of the object.</span></span> <span data-ttu-id="c8e2d-117">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-118">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-121">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c8e2d-122">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c8e2d-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-127">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-127">A description of the object.</span></span> <span data-ttu-id="c8e2d-128">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-132">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c8e2d-133">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c8e2d-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-138">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-138">A display name for the object.</span></span> <span data-ttu-id="c8e2d-139">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-141">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-143">Указывает тип компонента расширения.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8e2d-144">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="c8e2d-145">**Захват** (1)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="c8e2d-146">**Фильтр** (2)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="c8e2d-147">**Пересылка** (3)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="c8e2d-148">**Мониторинг** (4)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="c8e2d-149">**Машинный код** (5)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8e2d-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-153">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-153">The current health of the element.</span></span> <span data-ttu-id="c8e2d-154">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c8e2d-155">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c8e2d-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-158">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-160">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-160">The date and time when the object was installed.</span></span> <span data-ttu-id="c8e2d-161">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="c8e2d-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-166">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-167">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c8e2d-168">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-172">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c8e2d-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-173">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-173">The label by which the object is known.</span></span> <span data-ttu-id="c8e2d-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-175">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-176">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-178">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c8e2d-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c8e2d-179">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c8e2d-180">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-182">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c8e2d-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-184">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-184">The current statuses of the object.</span></span> <span data-ttu-id="c8e2d-185">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-186">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-189">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-189">Provides high level status information.</span></span> <span data-ttu-id="c8e2d-190">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c8e2d-191">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c8e2d-192">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-193">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-196">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-196">The current status of the object.</span></span> <span data-ttu-id="c8e2d-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8e2d-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c8e2d-198">'</span><span class="sxs-lookup"><span data-stu-id="c8e2d-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-199"><span id="OK"></span><span id="ok"></span>**Хорошо**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**План**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Пред — сбой**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Start**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Идет**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служеб**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Груз**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Невосстановление**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Потеря связи**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8e2d-211">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-212">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-214">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c8e2d-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c8e2d-215">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="c8e2d-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-216">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-219">Указывает поставщика, предоставляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c8e2d-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="c8e2d-220">**Version**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8e2d-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8e2d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8e2d-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8e2d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8e2d-223">Версия расширения в формате "основной. дополнительный", например "2,0".</span><span class="sxs-lookup"><span data-stu-id="c8e2d-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8e2d-224">Требования</span><span class="sxs-lookup"><span data-stu-id="c8e2d-224">Requirements</span></span>



| <span data-ttu-id="c8e2d-225">Требование</span><span class="sxs-lookup"><span data-stu-id="c8e2d-225">Requirement</span></span> | <span data-ttu-id="c8e2d-226">Значение</span><span class="sxs-lookup"><span data-stu-id="c8e2d-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e2d-227">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8e2d-227">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e2d-228">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c8e2d-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8e2d-229">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8e2d-229">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e2d-230">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c8e2d-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8e2d-231">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c8e2d-231">Namespace</span></span><br/>                | <span data-ttu-id="c8e2d-232">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c8e2d-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8e2d-233">MOF</span><span class="sxs-lookup"><span data-stu-id="c8e2d-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8e2d-234"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8e2d-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8e2d-235">DLL</span><span class="sxs-lookup"><span data-stu-id="c8e2d-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8e2d-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8e2d-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

