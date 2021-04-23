---
description: Представляет внешний порт Fibre Channel.
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Класс Msvm_ExternalFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682867"
---
# <a name="msvm_externalfcport-class"></a><span data-ttu-id="bcdc1-103">\_Класс мсвм екстерналфкпорт</span><span class="sxs-lookup"><span data-stu-id="bcdc1-103">Msvm\_ExternalFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="bcdc1-104">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="bcdc1-105">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="bcdc1-106">Представляет внешний порт Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-106">Represents an external Fibre Channel port.</span></span>

<span data-ttu-id="bcdc1-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcdc1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcdc1-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a><span data-ttu-id="bcdc1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="bcdc1-109">Members</span></span>

<span data-ttu-id="bcdc1-110">Класс **мсвм \_ екстерналфкпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bcdc1-110">The **Msvm\_ExternalFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bcdc1-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bcdc1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bcdc1-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcdc1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bcdc1-113">Методы</span><span class="sxs-lookup"><span data-stu-id="bcdc1-113">Methods</span></span>

<span data-ttu-id="bcdc1-114">Класс **мсвм \_ екстерналфкпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-114">The **Msvm\_ExternalFcPort** class has these methods.</span></span>



| <span data-ttu-id="bcdc1-115">Метод</span><span class="sxs-lookup"><span data-stu-id="bcdc1-115">Method</span></span>                                                               | <span data-ttu-id="bcdc1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bcdc1-116">Description</span></span>                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="bcdc1-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-117">**EnableDevice**</span></span>                                                     | <span data-ttu-id="bcdc1-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bcdc1-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-119">**OnlineDevice**</span></span>                                                     | <span data-ttu-id="bcdc1-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bcdc1-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-121">**QuiesceDevice**</span></span>                                                    | <span data-ttu-id="bcdc1-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="bcdc1-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-123">**RequestStateChange**</span></span>](msvm-externalfcport-requeststatechange.md) | <span data-ttu-id="bcdc1-124">Запрашивает изменение состояния</span><span class="sxs-lookup"><span data-stu-id="bcdc1-124">Requests a state change</span></span><br/>       |
| [<span data-ttu-id="bcdc1-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-125">**Reset**</span></span>](msvm-externalfcport-reset.md)                           | <span data-ttu-id="bcdc1-126">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="bcdc1-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-127">**RestoreProperties**</span></span>                                                | <span data-ttu-id="bcdc1-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bcdc1-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-129">**SaveProperties**</span></span>                                                   | <span data-ttu-id="bcdc1-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bcdc1-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-131">**SetPowerState**</span></span>                                                    | <span data-ttu-id="bcdc1-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bcdc1-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcdc1-133">Properties</span></span>

<span data-ttu-id="bcdc1-134">Класс **мсвм \_ екстерналфкпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-134">The **Msvm\_ExternalFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-135">**активекос**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-138">Массив целых чисел, указывающий классы активных служб.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="bcdc1-139">Поддерживаемая COS задается свойством **суппортедкос** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="bcdc1-140">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-150">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-152">Массив целых чисел, указывающий Fibre Channel протоколов FC-4, которые в настоящее время выполняются.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="bcdc1-153">Список всех поддерживаемых протоколов задается свойством **SupportedFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="bcdc1-154">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-181">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-184">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="bcdc1-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-185">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="bcdc1-186">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-187">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-188">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-190">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="bcdc1-191">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-192">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-195">Указывает, может ли порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="bcdc1-196">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-197">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-200">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-200">The primary availability and status of the device.</span></span> <span data-ttu-id="bcdc1-201">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-202">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-203">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-205">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="bcdc1-206">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-207">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-210">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-210">A short description of the object.</span></span> <span data-ttu-id="bcdc1-211">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-212">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-215">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bcdc1-216">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bcdc1-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bcdc1-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bcdc1-225">)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-229">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-229">The scoping system's creation class name.</span></span> <span data-ttu-id="bcdc1-230">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-231">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-234">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-234">A description of the object.</span></span> <span data-ttu-id="bcdc1-235">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-239">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bcdc1-240">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bcdc1-241">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bcdc1-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bcdc1-250">)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-254">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="bcdc1-255">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-259">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-259">A display name for the object.</span></span> <span data-ttu-id="bcdc1-260">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-261">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-264">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="bcdc1-265">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-269">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="bcdc1-270">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="bcdc1-271">Значение</span><span class="sxs-lookup"><span data-stu-id="bcdc1-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="bcdc1-272">Значение</span><span class="sxs-lookup"><span data-stu-id="bcdc1-272">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="bcdc1-273"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="bcdc1-274">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="bcdc1-275"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="bcdc1-276"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="bcdc1-277">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-277">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="bcdc1-278"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="bcdc1-279">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-279">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="bcdc1-280"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="bcdc1-281">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="bcdc1-282"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="bcdc1-283">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="bcdc1-284"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="bcdc1-285">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="bcdc1-286"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="bcdc1-287">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-287">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="bcdc1-288"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="bcdc1-289">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="bcdc1-290"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="bcdc1-291">Элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-291">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="bcdc1-292">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="bcdc1-293">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="bcdc1-294"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="bcdc1-295">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="bcdc1-296">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-296">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="bcdc1-297">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-300">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="bcdc1-301">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-305">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="bcdc1-306">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-307">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-310">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="bcdc1-311">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-313">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-315">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-315">The current health of the element.</span></span> <span data-ttu-id="bcdc1-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-318">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-320">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="bcdc1-321">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-323">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-325">The date and time when the object was installed.</span></span> <span data-ttu-id="bcdc1-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="bcdc1-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-331">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-332">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bcdc1-333">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-334">**ишипервкапабле**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-334">**IsHyperVCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-335">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-337">Если это свойство имеет **значение true**, этот Fibre Channel порт может быть подключен к коммутаторам и, таким же, может обеспечить подключение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-337">If this property is **True**, this Fibre Channel port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="bcdc1-338">Если это свойство имеет **значение false**, то этот порт не может использоваться Fibre Channel архитектурой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-338">If this property is **False**, then this port cannot be used by the virtual machine Fibre Channel architecture.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-339">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-340">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-342">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-342">The last error code reported by the logical device.</span></span> <span data-ttu-id="bcdc1-343">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-344">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-344">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-345">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-347">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-347">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="bcdc1-348">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-348">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="bcdc1-349">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-353"><span id="IB"></span><span id="ib"></span>**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="bcdc1-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-362">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-362">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-363">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-365">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-365">This property has been deprecated.</span></span> <span data-ttu-id="bcdc1-366">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-367">**максспид**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-367">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-368">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-370">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="bcdc1-370">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-371">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-371">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bcdc1-372">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-372">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-376">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-376">The label by which the object is known.</span></span> <span data-ttu-id="bcdc1-377">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-378">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-378">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-379">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-381">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-381">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-382">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-382">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="bcdc1-383">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-383">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-384">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-384">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-385">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-387">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-387">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bcdc1-388">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-388">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bcdc1-389">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bcdc1-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bcdc1-409">)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-409">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-410">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-410">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-411">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-413">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-413">The current statuses of the object.</span></span> <span data-ttu-id="bcdc1-414">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-415">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-415">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-416">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-418">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-418">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="bcdc1-419">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-419">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="bcdc1-420">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-420">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-421">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-421">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-422">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-422">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-424">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-424">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="bcdc1-425">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-425">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-426">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-426">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-429">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-429">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="bcdc1-430">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-431">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-431">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-432">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-434">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-434">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="bcdc1-435">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-435">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-436">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-436">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-437">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-439">Описывает тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-439">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="bcdc1-440">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-440">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-441">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-441">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-444">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-444">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-445">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-445">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="bcdc1-446">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-446">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="bcdc1-447">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-447">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="bcdc1-448">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-448">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="bcdc1-449">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-450">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-450">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-451">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-453">номер порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-453">The port number.</span></span> <span data-ttu-id="bcdc1-454">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-454">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-455">**Порта**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-455">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-456">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-458">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-458">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="bcdc1-459">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-459">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="bcdc1-460">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-460">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-483">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-483">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-484">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-484">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-485">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-486">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-486">The power management capabilities of the device.</span></span> <span data-ttu-id="bcdc1-487">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-488">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-488">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-489">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-489">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-491">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-491">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="bcdc1-492">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-493">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-493">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-494">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-494">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-496">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-496">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="bcdc1-497">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-498">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-498">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-499">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-499">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-501">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-501">Provides high level status information.</span></span> <span data-ttu-id="bcdc1-502">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-502">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="bcdc1-503">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-503">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bcdc1-504">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-504">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-506"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="bcdc1-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bcdc1-511">)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-511">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-512">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-512">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-513">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-514">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="bcdc1-514">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-515">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="bcdc1-515">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-516">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-516">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bcdc1-517">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-517">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="bcdc1-518">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-518">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-519">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-519">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-520">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-522">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-522">The last requested or desired state for the element.</span></span> <span data-ttu-id="bcdc1-523">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-523">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-524">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-524">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-525">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-525">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-526">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-526">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-527">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="bcdc1-527">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-528">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-528">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="bcdc1-529">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-529">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-530">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-530">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-531">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-532">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-533">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-533">The current status of the object.</span></span> <span data-ttu-id="bcdc1-534">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-535">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-535">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-536">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-536">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-538">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-538">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="bcdc1-539">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-539">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-540">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-540">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-541">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-541">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-543">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-543">The current state of the logical device.</span></span> <span data-ttu-id="bcdc1-544">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-544">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-545">**суппортедкос**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-545">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-546">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-546">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-547">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-547">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-548">Массив целых чисел, указывающий поддерживаемые Fibre Channel классы службы (COS).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-548">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="bcdc1-549">Активная COS задается свойством **активекос** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-549">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="bcdc1-550">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-550">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-552"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-552"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-553"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-553"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-554"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-554"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-555"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-555"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-556"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-556"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-557"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-557"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-558"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-558"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-559">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-559">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-560">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bcdc1-560">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-561">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-561">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-562">Массив целых чисел, указывающий Поддерживаемые протоколы FC-4 Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-562">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="bcdc1-563">Активные и выполняемые протоколы задаются свойством **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="bcdc1-563">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="bcdc1-564">Это свойство наследуется от **CIM \_ фкпорт**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-564">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-591">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-591">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-592">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-592">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-593">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-594">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="bcdc1-594">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-595">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-595">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="bcdc1-596">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-596">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-597">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-597">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-599">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-600">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-600">The scoping system's creation class name.</span></span> <span data-ttu-id="bcdc1-601">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-602">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-602">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-603">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-604">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-605">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-605">The scoping system's name.</span></span> <span data-ttu-id="bcdc1-606">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-606">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-607">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-607">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-608">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-608">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-609">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-610">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-610">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="bcdc1-611">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-611">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-612">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-612">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-613">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-613">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-614">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-615">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-615">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="bcdc1-616">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-616">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-617">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-617">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-618">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-619">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-620">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-620">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="bcdc1-621">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-621">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-622">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-622">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-623">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-623">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-624">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-624">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-625">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-625">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="bcdc1-626">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-626">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="bcdc1-627">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-627">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="bcdc1-628">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bcdc1-628">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bcdc1-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="bcdc1-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bcdc1-633">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-633">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-635">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-635">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-636">Имя узла в Интернете для этого Fibre Channel порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-636">The world wide node name for this Fibre Channel port.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc1-637">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-637">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcdc1-638">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcdc1-638">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcdc1-639">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcdc1-639">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcdc1-640">WWN имени порта для этого Fibre Channel порта.</span><span class="sxs-lookup"><span data-stu-id="bcdc1-640">The world wide port name for this Fibre Channel port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcdc1-641">Требования</span><span class="sxs-lookup"><span data-stu-id="bcdc1-641">Requirements</span></span>



| <span data-ttu-id="bcdc1-642">Требование</span><span class="sxs-lookup"><span data-stu-id="bcdc1-642">Requirement</span></span> | <span data-ttu-id="bcdc1-643">Значение</span><span class="sxs-lookup"><span data-stu-id="bcdc1-643">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdc1-644">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcdc1-644">Minimum supported client</span></span><br/> | <span data-ttu-id="bcdc1-645">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bcdc1-645">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bcdc1-646">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcdc1-646">Minimum supported server</span></span><br/> | <span data-ttu-id="bcdc1-647">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bcdc1-647">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcdc1-648">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bcdc1-648">Namespace</span></span><br/>                | <span data-ttu-id="bcdc1-649">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bcdc1-649">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bcdc1-650">MOF</span><span class="sxs-lookup"><span data-stu-id="bcdc1-650">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcdc1-651"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-651"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcdc1-652">DLL</span><span class="sxs-lookup"><span data-stu-id="bcdc1-652">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcdc1-653"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc1-653"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

