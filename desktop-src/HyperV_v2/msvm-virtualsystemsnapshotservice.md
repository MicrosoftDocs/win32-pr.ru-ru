---
description: Служба для создания, применения и уничтожения моментальных снимков виртуальных машин.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Класс Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896818"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="63e5e-103">\_Класс мсвм виртуалсистемснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="63e5e-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="63e5e-104">Служба для создания, применения и уничтожения моментальных снимков виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="63e5e-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="63e5e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="63e5e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e5e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63e5e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="63e5e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="63e5e-107">Members</span></span>

<span data-ttu-id="63e5e-108">Класс **мсвм \_ виртуалсистемснапшотсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="63e5e-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="63e5e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="63e5e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="63e5e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="63e5e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63e5e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="63e5e-111">Methods</span></span>

<span data-ttu-id="63e5e-112">Класс **мсвм \_ виртуалсистемснапшотсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="63e5e-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="63e5e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="63e5e-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="63e5e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="63e5e-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="63e5e-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>апплиснапшот</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-116">Применяет моментальный снимок виртуальной машины к виртуальной машине, из которой он был создан.</span><span class="sxs-lookup"><span data-stu-id="63e5e-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="63e5e-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>клеарснапшотстате</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-118">Очищает сохраненное состояние из существующего моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="63e5e-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="63e5e-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>конверттореференцепоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-120">Преобразование существующего моментального снимка виртуальной системы в точку ссылки.</span><span class="sxs-lookup"><span data-stu-id="63e5e-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="63e5e-121">Моментальный снимок удаляется как побочный результат.</span><span class="sxs-lookup"><span data-stu-id="63e5e-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="63e5e-122">В контрольные точки можно преобразовать только моментальные снимки восстановления.</span><span class="sxs-lookup"><span data-stu-id="63e5e-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="63e5e-123">Поддержка этого метода была добавлена в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63e5e-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="63e5e-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-125">Создает моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63e5e-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="63e5e-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>дестройснапшот</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-127">Уничтожает существующий моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63e5e-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="63e5e-128">Этот метод может в качестве побочного результата уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="63e5e-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="63e5e-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>дестройснапшоттри</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-130">Удаляет существующий моментальный снимок и все его дочерние элементы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63e5e-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="63e5e-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>Равен</strong></a></span><span class="sxs-lookup"><span data-stu-id="63e5e-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-132">Запрашивает изменение состояния для элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="63e5e-133">Поддержка этого метода была добавлена в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63e5e-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="63e5e-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="63e5e-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-135">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63e5e-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="63e5e-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="63e5e-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="63e5e-137">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="63e5e-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="63e5e-138">Свойства</span><span class="sxs-lookup"><span data-stu-id="63e5e-138">Properties</span></span>

<span data-ttu-id="63e5e-139">Класс **мсвм \_ виртуалсистемснапшотсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="63e5e-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-140">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="63e5e-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="63e5e-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-143">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="63e5e-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="63e5e-144">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="63e5e-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="63e5e-145">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="63e5e-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="63e5e-146">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="63e5e-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="63e5e-147">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63e5e-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="63e5e-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="63e5e-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="63e5e-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="63e5e-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="63e5e-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="63e5e-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="63e5e-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="63e5e-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="63e5e-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="63e5e-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="63e5e-158">)</span><span class="sxs-lookup"><span data-stu-id="63e5e-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e5e-159">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="63e5e-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-162">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="63e5e-162">A short description of the object.</span></span> <span data-ttu-id="63e5e-163">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба моментальных снимков виртуальных систем Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="63e5e-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-164">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="63e5e-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-167">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="63e5e-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="63e5e-168">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="63e5e-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="63e5e-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="63e5e-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="63e5e-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="63e5e-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="63e5e-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="63e5e-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="63e5e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="63e5e-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="63e5e-177">)</span><span class="sxs-lookup"><span data-stu-id="63e5e-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e5e-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63e5e-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-181">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="63e5e-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-182">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="63e5e-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="63e5e-183">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ виртуалсистемснапшотсервице".</span><span class="sxs-lookup"><span data-stu-id="63e5e-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-184">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63e5e-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-187">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="63e5e-187">A description of the object.</span></span> <span data-ttu-id="63e5e-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба для создания, уничтожения и применения моментальных снимков виртуальных машин".</span><span class="sxs-lookup"><span data-stu-id="63e5e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="63e5e-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-192">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="63e5e-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="63e5e-193">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="63e5e-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="63e5e-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="63e5e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="63e5e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="63e5e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="63e5e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="63e5e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="63e5e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="63e5e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="63e5e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="63e5e-203">)</span><span class="sxs-lookup"><span data-stu-id="63e5e-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e5e-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="63e5e-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-207">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="63e5e-207">A display name for the object.</span></span> <span data-ttu-id="63e5e-208">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-209">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="63e5e-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-210">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-212">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="63e5e-213">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="63e5e-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="63e5e-214">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-214">Value</span></span>                                                                        | <span data-ttu-id="63e5e-215">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="63e5e-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="63e5e-217">Активировано</span><span class="sxs-lookup"><span data-stu-id="63e5e-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63e5e-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="63e5e-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-221">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="63e5e-222">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="63e5e-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="63e5e-223">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="63e5e-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="63e5e-224">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-224">Value</span></span>                                                                        | <span data-ttu-id="63e5e-225">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="63e5e-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="63e5e-227">Активировано</span><span class="sxs-lookup"><span data-stu-id="63e5e-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63e5e-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="63e5e-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-229">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-231">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-231">The current health of the element.</span></span> <span data-ttu-id="63e5e-232">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="63e5e-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="63e5e-233">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="63e5e-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="63e5e-234">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="63e5e-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="63e5e-235">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-235">Value</span></span>                                                                        | <span data-ttu-id="63e5e-236">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="63e5e-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="63e5e-238">Состояние работоспособности — нормальное.</span><span class="sxs-lookup"><span data-stu-id="63e5e-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63e5e-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63e5e-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-240">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63e5e-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-242">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63e5e-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="63e5e-243">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63e5e-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-247">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="63e5e-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-248">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="63e5e-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="63e5e-249">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-250">**Name**</span><span class="sxs-lookup"><span data-stu-id="63e5e-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-253">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="63e5e-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-254">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="63e5e-254">The label by which the object is known.</span></span> <span data-ttu-id="63e5e-255">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "всснапсвк".</span><span class="sxs-lookup"><span data-stu-id="63e5e-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-256">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="63e5e-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-259">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="63e5e-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="63e5e-260">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="63e5e-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="63e5e-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="63e5e-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="63e5e-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="63e5e-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="63e5e-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="63e5e-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="63e5e-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="63e5e-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="63e5e-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="63e5e-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="63e5e-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="63e5e-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="63e5e-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="63e5e-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="63e5e-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="63e5e-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="63e5e-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="63e5e-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="63e5e-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="63e5e-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="63e5e-281">)</span><span class="sxs-lookup"><span data-stu-id="63e5e-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e5e-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="63e5e-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-283">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="63e5e-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-285">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="63e5e-285">The current statuses of the object.</span></span> <span data-ttu-id="63e5e-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="63e5e-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-287">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="63e5e-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-290">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="63e5e-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="63e5e-291">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="63e5e-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="63e5e-292">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-293">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="63e5e-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-296">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="63e5e-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-297">Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="63e5e-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="63e5e-298">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-299">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="63e5e-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-302">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="63e5e-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-303">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="63e5e-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="63e5e-304">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="63e5e-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="63e5e-305">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-306">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="63e5e-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-307">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-309">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="63e5e-309">Provides high level status information.</span></span> <span data-ttu-id="63e5e-310">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="63e5e-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="63e5e-311">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="63e5e-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="63e5e-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63e5e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="63e5e-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="63e5e-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-314"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="63e5e-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="63e5e-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="63e5e-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="63e5e-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="63e5e-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="63e5e-319">)</span><span class="sxs-lookup"><span data-stu-id="63e5e-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63e5e-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="63e5e-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-321">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-323">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="63e5e-324">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="63e5e-325">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="63e5e-326">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="63e5e-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="63e5e-327">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="63e5e-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="63e5e-328">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="63e5e-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="63e5e-329">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-329">Value</span></span>                                                                         | <span data-ttu-id="63e5e-330">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="63e5e-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="63e5e-332">Не применяется</span><span class="sxs-lookup"><span data-stu-id="63e5e-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="63e5e-333">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="63e5e-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-334">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="63e5e-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-336">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="63e5e-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="63e5e-337">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="63e5e-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-341">Квалификаторы: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="63e5e-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-342">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="63e5e-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="63e5e-343">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="63e5e-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-344">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="63e5e-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="63e5e-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-348">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="63e5e-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-349">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="63e5e-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-351">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="63e5e-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="63e5e-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "служба работает нормально".</span><span class="sxs-lookup"><span data-stu-id="63e5e-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-353">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="63e5e-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-356">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="63e5e-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-357">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="63e5e-357">The scoping system's creation class name.</span></span> <span data-ttu-id="63e5e-358">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="63e5e-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="63e5e-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="63e5e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-362">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="63e5e-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-363">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="63e5e-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="63e5e-364">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63e5e-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-365">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="63e5e-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-366">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63e5e-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-368">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="63e5e-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="63e5e-369">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63e5e-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="63e5e-370">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="63e5e-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63e5e-371">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63e5e-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63e5e-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="63e5e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63e5e-373">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="63e5e-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="63e5e-374">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63e5e-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="63e5e-375">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="63e5e-376">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="63e5e-377"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="63e5e-378"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="63e5e-379"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="63e5e-380"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="63e5e-381"><dt>**Нет изменений**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="63e5e-382">Переход не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63e5e-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="63e5e-383"><dt>**Автономный режим**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="63e5e-384"><dt>**Тест**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="63e5e-385"><dt>**Отложить**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="63e5e-386"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="63e5e-387"><dt>**Перезагрузка**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="63e5e-388"><dt>**Сброс**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="63e5e-389"><dt>**Не применимо**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="63e5e-390">Реализация не поддерживает представление текущих переходов.</span><span class="sxs-lookup"><span data-stu-id="63e5e-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="63e5e-391"><dt> **Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63e5e-392">Требования</span><span class="sxs-lookup"><span data-stu-id="63e5e-392">Requirements</span></span>



| <span data-ttu-id="63e5e-393">Требование</span><span class="sxs-lookup"><span data-stu-id="63e5e-393">Requirement</span></span> | <span data-ttu-id="63e5e-394">Значение</span><span class="sxs-lookup"><span data-stu-id="63e5e-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e5e-395">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63e5e-395">Minimum supported client</span></span><br/> | <span data-ttu-id="63e5e-396">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="63e5e-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="63e5e-397">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63e5e-397">Minimum supported server</span></span><br/> | <span data-ttu-id="63e5e-398">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="63e5e-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63e5e-399">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63e5e-399">Namespace</span></span><br/>                | <span data-ttu-id="63e5e-400">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="63e5e-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="63e5e-401">MOF</span><span class="sxs-lookup"><span data-stu-id="63e5e-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63e5e-402"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63e5e-403">DLL</span><span class="sxs-lookup"><span data-stu-id="63e5e-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e5e-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63e5e-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

