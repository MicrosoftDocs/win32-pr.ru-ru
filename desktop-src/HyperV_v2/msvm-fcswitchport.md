---
description: Представляет порт в виртуальном Fibre Channel коммутаторе.
ms.assetid: 6b4553b7-2717-4285-9e1a-e2ad22a60997
title: Класс Msvm_FcSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcSwitchPort
- Msvm_FcSwitchPort.SetPowerState
- Msvm_FcSwitchPort.EnableDevice
- Msvm_FcSwitchPort.OnlineDevice
- Msvm_FcSwitchPort.QuiesceDevice
- Msvm_FcSwitchPort.SaveProperties
- Msvm_FcSwitchPort.RestoreProperties
- Msvm_FcSwitchPort.InstanceID
- Msvm_FcSwitchPort.Caption
- Msvm_FcSwitchPort.Description
- Msvm_FcSwitchPort.ElementName
- Msvm_FcSwitchPort.InstallDate
- Msvm_FcSwitchPort.Name
- Msvm_FcSwitchPort.OperationalStatus
- Msvm_FcSwitchPort.StatusDescriptions
- Msvm_FcSwitchPort.Status
- Msvm_FcSwitchPort.HealthState
- Msvm_FcSwitchPort.CommunicationStatus
- Msvm_FcSwitchPort.DetailedStatus
- Msvm_FcSwitchPort.OperatingStatus
- Msvm_FcSwitchPort.PrimaryStatus
- Msvm_FcSwitchPort.EnabledState
- Msvm_FcSwitchPort.OtherEnabledState
- Msvm_FcSwitchPort.RequestedState
- Msvm_FcSwitchPort.EnabledDefault
- Msvm_FcSwitchPort.TimeOfLastStateChange
- Msvm_FcSwitchPort.AvailableRequestedStates
- Msvm_FcSwitchPort.TransitioningToState
- Msvm_FcSwitchPort.SystemCreationClassName
- Msvm_FcSwitchPort.SystemName
- Msvm_FcSwitchPort.CreationClassName
- Msvm_FcSwitchPort.DeviceID
- Msvm_FcSwitchPort.PowerManagementSupported
- Msvm_FcSwitchPort.PowerManagementCapabilities
- Msvm_FcSwitchPort.Availability
- Msvm_FcSwitchPort.StatusInfo
- Msvm_FcSwitchPort.LastErrorCode
- Msvm_FcSwitchPort.ErrorDescription
- Msvm_FcSwitchPort.ErrorCleared
- Msvm_FcSwitchPort.OtherIdentifyingInfo
- Msvm_FcSwitchPort.PowerOnHours
- Msvm_FcSwitchPort.TotalPowerOnHours
- Msvm_FcSwitchPort.IdentifyingDescriptions
- Msvm_FcSwitchPort.AdditionalAvailability
- Msvm_FcSwitchPort.MaxQuiesceTime
- Msvm_FcSwitchPort.Speed
- Msvm_FcSwitchPort.MaxSpeed
- Msvm_FcSwitchPort.RequestedSpeed
- Msvm_FcSwitchPort.UsageRestriction
- Msvm_FcSwitchPort.PortType
- Msvm_FcSwitchPort.OtherPortType
- Msvm_FcSwitchPort.OtherNetworkPortType
- Msvm_FcSwitchPort.PortNumber
- Msvm_FcSwitchPort.LinkTechnology
- Msvm_FcSwitchPort.OtherLinkTechnology
- Msvm_FcSwitchPort.PermanentAddress
- Msvm_FcSwitchPort.NetworkAddresses
- Msvm_FcSwitchPort.FullDuplex
- Msvm_FcSwitchPort.AutoSense
- Msvm_FcSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_FcSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_FcSwitchPort.SupportedCOS
- Msvm_FcSwitchPort.ActiveCOS
- Msvm_FcSwitchPort.SupportedFC4Types
- Msvm_FcSwitchPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443ae1065b7c7a6a4bb1523a672e388cacb91667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542479"
---
# <a name="msvm_fcswitchport-class"></a><span data-ttu-id="ee4fd-103">\_Класс мсвм фксвитчпорт</span><span class="sxs-lookup"><span data-stu-id="ee4fd-103">Msvm\_FcSwitchPort class</span></span>

> [!NOTE]
> <span data-ttu-id="ee4fd-104">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="ee4fd-105">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="ee4fd-106">Представляет порт в виртуальном Fibre Channel коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-106">Represents a port on the virtual Fibre Channel switch.</span></span>

<span data-ttu-id="ee4fd-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee4fd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcSwitchPort : CIM_FCPort
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
  uint16   LinkTechnology;
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

## <a name="members"></a><span data-ttu-id="ee4fd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ee4fd-109">Members</span></span>

<span data-ttu-id="ee4fd-110">Класс **мсвм \_ фксвитчпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ee4fd-110">The **Msvm\_FcSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ee4fd-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ee4fd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee4fd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ee4fd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee4fd-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ee4fd-113">Methods</span></span>

<span data-ttu-id="ee4fd-114">Класс **мсвм \_ фксвитчпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-114">The **Msvm\_FcSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="ee4fd-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ee4fd-115">Method</span></span>                                                             | <span data-ttu-id="ee4fd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4fd-116">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ee4fd-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-117">**EnableDevice**</span></span>                                                   | <span data-ttu-id="ee4fd-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ee4fd-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-119">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="ee4fd-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ee4fd-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-121">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="ee4fd-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ee4fd-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-123">**RequestStateChange**</span></span>](msvm-fcswitchport-requeststatechange.md) | <span data-ttu-id="ee4fd-124">запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-124">requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ee4fd-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-125">**Reset**</span></span>](msvm-fcswitchport-reset.md)                           | <span data-ttu-id="ee4fd-126">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="ee4fd-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-127">**RestoreProperties**</span></span>                                              | <span data-ttu-id="ee4fd-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ee4fd-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-129">**SaveProperties**</span></span>                                                 | <span data-ttu-id="ee4fd-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ee4fd-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-131">**SetPowerState**</span></span>                                                  | <span data-ttu-id="ee4fd-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ee4fd-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="ee4fd-133">Properties</span></span>

<span data-ttu-id="ee4fd-134">Класс **мсвм \_ фксвитчпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-134">The **Msvm\_FcSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-135">**активекос**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-138">Массив целых чисел, указывающий классы активных служб.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="ee4fd-139">Поддерживаемая COS задается свойством **суппортедкос** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="ee4fd-140">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-150">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-152">Массив целых чисел, указывающий Fibre Channel протоколов FC-4, которые в настоящее время выполняются.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="ee4fd-153">Список всех поддерживаемых протоколов задается свойством **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="ee4fd-154">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-181">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-184">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="ee4fd-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-185">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="ee4fd-186">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-187">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-188">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-190">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="ee4fd-191">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-192">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-195">Указывает, может ли порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="ee4fd-196">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-197">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-200">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-200">The primary availability and status of the device.</span></span> <span data-ttu-id="ee4fd-201">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-202">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-203">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-205">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ee4fd-206">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-207">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-210">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-210">A short description of the object.</span></span> <span data-ttu-id="ee4fd-211">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-212">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-215">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ee4fd-216">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee4fd-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ee4fd-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee4fd-225">)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-229">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-229">The scoping system's creation class name.</span></span> <span data-ttu-id="ee4fd-230">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-231">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-234">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-234">A description of the object.</span></span> <span data-ttu-id="ee4fd-235">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-239">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ee4fd-240">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee4fd-241">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ee4fd-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee4fd-250">)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-254">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="ee4fd-255">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-259">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-259">A display name for the object.</span></span> <span data-ttu-id="ee4fd-260">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-261">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-264">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="ee4fd-265">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-269">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ee4fd-270">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="ee4fd-271">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4fd-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ee4fd-272">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4fd-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ee4fd-273"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="ee4fd-274">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ee4fd-275"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="ee4fd-276"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="ee4fd-277">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="ee4fd-278"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ee4fd-279">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="ee4fd-280"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="ee4fd-281">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ee4fd-282"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="ee4fd-283">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="ee4fd-284"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ee4fd-285">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="ee4fd-286"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="ee4fd-287">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="ee4fd-288"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="ee4fd-289">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="ee4fd-290"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="ee4fd-291">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="ee4fd-292">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="ee4fd-293">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="ee4fd-294"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ee4fd-295">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="ee4fd-296">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="ee4fd-297">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-300">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="ee4fd-301">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-305">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="ee4fd-306">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-307">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-310">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="ee4fd-311">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-313">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-315">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-315">The current health of the element.</span></span> <span data-ttu-id="ee4fd-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-318">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-320">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ee4fd-321">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-323">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-325">The date and time when the object was installed.</span></span> <span data-ttu-id="ee4fd-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="ee4fd-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-331">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-332">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ee4fd-333">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-334">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-337">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="ee4fd-338">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-339">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-340">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-342">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="ee4fd-343">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="ee4fd-344">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-348"><span id="IB"></span><span id="ib"></span>**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="ee4fd-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-357">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-357">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-358">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-360">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-360">This property has been deprecated.</span></span> <span data-ttu-id="ee4fd-361">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-362">**максспид**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-362">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-363">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-365">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="ee4fd-365">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-366">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-366">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ee4fd-367">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-367">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-368">**Name**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-371">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-371">The label by which the object is known.</span></span> <span data-ttu-id="ee4fd-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-373">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-373">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-374">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-374">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-376">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-376">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-377">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-377">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="ee4fd-378">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-378">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-379">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-379">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-380">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-382">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-382">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ee4fd-383">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee4fd-384">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ee4fd-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee4fd-404">)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-404">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-405">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-405">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-406">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-408">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-408">The current statuses of the object.</span></span> <span data-ttu-id="ee4fd-409">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-410">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-410">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-411">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-413">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-413">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ee4fd-414">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-414">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="ee4fd-415">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-416">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-416">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-417">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-417">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-419">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-419">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ee4fd-420">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-421">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-421">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-422">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-424">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-424">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="ee4fd-425">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-425">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-426">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-426">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-429">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-429">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="ee4fd-430">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-431">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-431">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-432">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-434">Описывает тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-434">Describes the type of module when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="ee4fd-435">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-436">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-436">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-437">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-439">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-439">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-440">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-440">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="ee4fd-441">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-441">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="ee4fd-442">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-442">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="ee4fd-443">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-443">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="ee4fd-444">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-444">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-445">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-445">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-446">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-448">номер порта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-448">The port number.</span></span> <span data-ttu-id="ee4fd-449">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-450">**Порта**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-450">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-451">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-453">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-453">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="ee4fd-454">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-454">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="ee4fd-455">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-455">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-478">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-478">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-479">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-479">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-481">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-481">The power management capabilities of the device.</span></span> <span data-ttu-id="ee4fd-482">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-482">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-483">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-483">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-484">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-484">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-485">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-486">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-486">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ee4fd-487">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-488">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-488">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-489">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-489">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-491">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-491">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ee4fd-492">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-493">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-493">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-494">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-496">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-496">Provides high level status information.</span></span> <span data-ttu-id="ee4fd-497">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-497">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ee4fd-498">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-498">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee4fd-499">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-499">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-501"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ee4fd-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee4fd-506">)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-506">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-507">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-507">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-508">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-509">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="ee4fd-509">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-510">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="ee4fd-510">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-511">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-511">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ee4fd-512">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-512">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="ee4fd-513">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-513">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-514">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-514">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-515">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-517">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-517">The last requested or desired state for the element.</span></span> <span data-ttu-id="ee4fd-518">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-518">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-519">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-519">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-520">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-520">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-522">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="ee4fd-522">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-523">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-523">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ee4fd-524">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-524">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-525">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-525">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-527">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-528">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-528">The current status of the object.</span></span> <span data-ttu-id="ee4fd-529">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-530">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-531">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-532">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-533">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ee4fd-534">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-535">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-535">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-536">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-538">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-538">The current state of the logical device.</span></span> <span data-ttu-id="ee4fd-539">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-539">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-540">**суппортедкос**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-540">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-541">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-543">Массив целых чисел, указывающий поддерживаемые Fibre Channel классы службы (COS).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-543">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="ee4fd-544">Активная COS задается свойством **активекос** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-544">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="ee4fd-545">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-545">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-547"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-547"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-548"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-548"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-549"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-549"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-550"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-550"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-551"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-551"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-552"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-552"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-553"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-553"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-554">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-554">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-555">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ee4fd-555">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-556">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-557">Массив целых чисел, указывающий Поддерживаемые протоколы FC-4 Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-557">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="ee4fd-558">Активные и выполняемые протоколы задаются свойством **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="ee4fd-558">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="ee4fd-559">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-559">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee4fd-586">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-586">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-587">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-587">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-588">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-589">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="ee4fd-589">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-590">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-590">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="ee4fd-591">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-591">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-592">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-592">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-593">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-593">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-594">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-594">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-595">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-595">The scoping system's creation class name.</span></span> <span data-ttu-id="ee4fd-596">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-596">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-597">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-597">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-599">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-600">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-600">The scoping system's name.</span></span> <span data-ttu-id="ee4fd-601">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-602">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-602">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-603">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-603">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-604">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-605">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-605">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ee4fd-606">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-606">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-607">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-607">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-608">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-608">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-609">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-610">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-610">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ee4fd-611">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-611">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-612">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-612">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-613">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-614">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-615">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-615">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ee4fd-616">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-616">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee4fd-617">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-617">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee4fd-618">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee4fd-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-619">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ee4fd-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee4fd-620">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-620">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="ee4fd-621">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="ee4fd-621">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="ee4fd-622">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-622">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="ee4fd-623">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee4fd-623">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ee4fd-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee4fd-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="ee4fd-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee4fd-628">Требования</span><span class="sxs-lookup"><span data-stu-id="ee4fd-628">Requirements</span></span>



| <span data-ttu-id="ee4fd-629">Требование</span><span class="sxs-lookup"><span data-stu-id="ee4fd-629">Requirement</span></span> | <span data-ttu-id="ee4fd-630">Значение</span><span class="sxs-lookup"><span data-stu-id="ee4fd-630">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4fd-631">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee4fd-631">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4fd-632">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ee4fd-632">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee4fd-633">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee4fd-633">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4fd-634">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ee4fd-634">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee4fd-635">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ee4fd-635">Namespace</span></span><br/>                | <span data-ttu-id="ee4fd-636">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ee4fd-636">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee4fd-637">MOF</span><span class="sxs-lookup"><span data-stu-id="ee4fd-637">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee4fd-638"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-638"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee4fd-639">DLL</span><span class="sxs-lookup"><span data-stu-id="ee4fd-639">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee4fd-640"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee4fd-640"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

