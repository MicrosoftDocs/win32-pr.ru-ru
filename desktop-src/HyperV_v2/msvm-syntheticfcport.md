---
description: Представляет порт искусственного Fibre Channel.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Класс Msvm_SyntheticFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143918"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="a0e5d-103">\_Класс мсвм синсетикфкпорт</span><span class="sxs-lookup"><span data-stu-id="a0e5d-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="a0e5d-104">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="a0e5d-105">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="a0e5d-106">Представляет порт искусственного Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="a0e5d-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e5d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e5d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
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
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="a0e5d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a0e5d-109">Members</span></span>

<span data-ttu-id="a0e5d-110">Класс **мсвм \_ синсетикфкпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a0e5d-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a0e5d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a0e5d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0e5d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0e5d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0e5d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a0e5d-113">Methods</span></span>

<span data-ttu-id="a0e5d-114">Класс **мсвм \_ синсетикфкпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="a0e5d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="a0e5d-115">Method</span></span>                                                                | <span data-ttu-id="a0e5d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a0e5d-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a0e5d-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="a0e5d-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a0e5d-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="a0e5d-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a0e5d-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="a0e5d-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a0e5d-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="a0e5d-124">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="a0e5d-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="a0e5d-126">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="a0e5d-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="a0e5d-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a0e5d-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="a0e5d-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a0e5d-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="a0e5d-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0e5d-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0e5d-133">Properties</span></span>

<span data-ttu-id="a0e5d-134">Класс **мсвм \_ синсетикфкпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-135">**активекос**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-138">Массив целых чисел, указывающий классы активных служб.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="a0e5d-139">Поддерживаемая COS задается свойством **суппортедкос** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="a0e5d-140">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-150">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-152">Массив целых чисел, указывающий Fibre Channel протоколов FC-4, которые в настоящее время выполняются.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="a0e5d-153">Список всех поддерживаемых протоколов задается свойством **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="a0e5d-154">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-181">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-184">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="a0e5d-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-185">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="a0e5d-186">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-187">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-188">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-190">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="a0e5d-191">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-192">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-195">Указывает, может ли порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="a0e5d-196">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-197">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-200">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-200">The primary availability and status of the device.</span></span> <span data-ttu-id="a0e5d-201">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-202">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-203">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-205">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a0e5d-206">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-207">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-210">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-210">A short description of the object.</span></span> <span data-ttu-id="a0e5d-211">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-212">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-215">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a0e5d-216">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0e5d-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0e5d-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0e5d-225">)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-229">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-229">The scoping system's creation class name.</span></span> <span data-ttu-id="a0e5d-230">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-231">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-234">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-234">A description of the object.</span></span> <span data-ttu-id="a0e5d-235">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-239">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a0e5d-240">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0e5d-241">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0e5d-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0e5d-250">)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-254">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="a0e5d-255">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-259">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-259">A display name for the object.</span></span> <span data-ttu-id="a0e5d-260">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-261">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-264">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="a0e5d-265">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-269">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a0e5d-270">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="a0e5d-271">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e5d-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a0e5d-272">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e5d-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a0e5d-273"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="a0e5d-274">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a0e5d-275"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="a0e5d-276"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="a0e5d-277">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a0e5d-278"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a0e5d-279">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="a0e5d-280"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="a0e5d-281">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="a0e5d-282"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="a0e5d-283">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a0e5d-284"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a0e5d-285">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="a0e5d-286"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="a0e5d-287">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="a0e5d-288"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="a0e5d-289">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="a0e5d-290"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="a0e5d-291">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="a0e5d-292">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="a0e5d-293">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="a0e5d-294"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="a0e5d-295">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="a0e5d-296">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="a0e5d-297">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-300">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="a0e5d-301">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-305">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="a0e5d-306">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-307">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-310">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="a0e5d-311">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-313">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-315">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-315">The current health of the element.</span></span> <span data-ttu-id="a0e5d-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-318">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-320">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="a0e5d-321">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-323">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-325">The date and time when the object was installed.</span></span> <span data-ttu-id="a0e5d-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="a0e5d-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-331">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-332">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a0e5d-333">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-334">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-337">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="a0e5d-338">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-339">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-340">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-342">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="a0e5d-343">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="a0e5d-344">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="a0e5d-345">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e5d-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="a0e5d-346">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e5d-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="a0e5d-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a0e5d-348">Fibre Channel</span><span class="sxs-lookup"><span data-stu-id="a0e5d-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0e5d-349">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-350">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-352">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-352">This property has been deprecated.</span></span> <span data-ttu-id="a0e5d-353">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-354">**максспид**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-355">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-357">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="a0e5d-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-358">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a0e5d-359">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-363">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-363">The label by which the object is known.</span></span> <span data-ttu-id="a0e5d-364">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-366">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-368">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-369">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="a0e5d-370">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-371">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-372">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-374">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a0e5d-375">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0e5d-376">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0e5d-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0e5d-396">)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-398">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-400">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-400">The current statuses of the object.</span></span> <span data-ttu-id="a0e5d-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-402">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-405">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a0e5d-406">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="a0e5d-407">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-409">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-411">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a0e5d-412">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-413">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-414">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-416">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="a0e5d-417">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-418">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-419">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-421">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="a0e5d-422">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-423">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-426">Описывает тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="a0e5d-427">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-428">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-429">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-431">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-432">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="a0e5d-433">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="a0e5d-434">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="a0e5d-435">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="a0e5d-436">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-437">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-438">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-440">номер порта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-440">The port number.</span></span> <span data-ttu-id="a0e5d-441">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-442">**Порта**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-443">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-445">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="a0e5d-446">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="a0e5d-447">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-470">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-471">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-473">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-473">The power management capabilities of the device.</span></span> <span data-ttu-id="a0e5d-474">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-475">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-476">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-478">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a0e5d-479">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-480">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-481">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-483">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a0e5d-484">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-485">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-486">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-488">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-488">Provides high level status information.</span></span> <span data-ttu-id="a0e5d-489">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a0e5d-490">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0e5d-491">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-493"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0e5d-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0e5d-498">)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-499">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-500">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-501">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="a0e5d-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-502">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="a0e5d-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-503">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a0e5d-504">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="a0e5d-505">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-507">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-508">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-509">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="a0e5d-510">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-511">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-512">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-514">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="a0e5d-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-515">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="a0e5d-516">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-517">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-518">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-520">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-520">The current status of the object.</span></span> <span data-ttu-id="a0e5d-521">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-522">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-523">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-525">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a0e5d-526">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-528">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-529">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-530">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-530">The current state of the logical device.</span></span> <span data-ttu-id="a0e5d-531">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-532">**суппортедкос**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-533">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-535">Массив целых чисел, указывающий поддерживаемые Fibre Channel классы службы (COS).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="a0e5d-536">Активная COS задается свойством **активекос** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="a0e5d-537">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-547">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0e5d-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-549">Массив целых чисел, указывающий Поддерживаемые протоколы FC-4 Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="a0e5d-550">Активные и выполняемые протоколы задаются свойством **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="a0e5d-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="a0e5d-551">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0e5d-578">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-579">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-580">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-581">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="a0e5d-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-582">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="a0e5d-583">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-584">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-585">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-586">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-587">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-587">The scoping system's creation class name.</span></span> <span data-ttu-id="a0e5d-588">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-590">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-591">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-592">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-592">The scoping system's name.</span></span> <span data-ttu-id="a0e5d-593">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-594">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-595">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-596">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-597">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a0e5d-598">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-599">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-600">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-601">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-602">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a0e5d-603">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-604">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-605">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-606">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-607">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a0e5d-608">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e5d-609">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0e5d-610">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0e5d-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-611">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0e5d-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0e5d-612">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="a0e5d-613">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="a0e5d-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="a0e5d-614">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="a0e5d-615">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0e5d-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a0e5d-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0e5d-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="a0e5d-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0e5d-620">Требования</span><span class="sxs-lookup"><span data-stu-id="a0e5d-620">Requirements</span></span>



| <span data-ttu-id="a0e5d-621">Требование</span><span class="sxs-lookup"><span data-stu-id="a0e5d-621">Requirement</span></span> | <span data-ttu-id="a0e5d-622">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e5d-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e5d-623">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0e5d-623">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e5d-624">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a0e5d-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0e5d-625">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0e5d-625">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e5d-626">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a0e5d-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0e5d-627">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a0e5d-627">Namespace</span></span><br/>                | <span data-ttu-id="a0e5d-628">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a0e5d-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0e5d-629">MOF</span><span class="sxs-lookup"><span data-stu-id="a0e5d-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0e5d-630"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0e5d-631">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e5d-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e5d-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0e5d-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

