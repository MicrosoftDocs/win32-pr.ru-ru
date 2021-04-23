---
description: Представляет возможности и управление устройством порта Fibre Channel (FC).
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: Класс CIM_FCPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682421"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="480b0-103">\_Класс CIM фкпорт</span><span class="sxs-lookup"><span data-stu-id="480b0-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="480b0-104">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="480b0-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="480b0-105">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="480b0-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="480b0-106">Представляет возможности и управление устройством порта Fibre Channel (FC).</span><span class="sxs-lookup"><span data-stu-id="480b0-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="480b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="480b0-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="480b0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="480b0-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="480b0-109">Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его.</span><span class="sxs-lookup"><span data-stu-id="480b0-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="480b0-110">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="480b0-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="480b0-111">Класс **CIM \_ фкпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="480b0-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="480b0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="480b0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="480b0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="480b0-113">Properties</span></span>

<span data-ttu-id="480b0-114">Класс **CIM \_ фкпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="480b0-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="480b0-115">**активекос**</span><span class="sxs-lookup"><span data-stu-id="480b0-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="480b0-116">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="480b0-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="480b0-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="480b0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="480b0-118">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фкпорт**.**Суппортедкос**")</span><span class="sxs-lookup"><span data-stu-id="480b0-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="480b0-119">Параметры активного класса службы (COS) для Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="480b0-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="480b0-120">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="480b0-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="480b0-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="480b0-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="480b0-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="480b0-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="480b0-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="480b0-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="480b0-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="480b0-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="480b0-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="480b0-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="480b0-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="480b0-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="480b0-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="480b0-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="480b0-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="480b0-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="480b0-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="480b0-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="480b0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="480b0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="480b0-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фкпорт**.**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="480b0-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="480b0-132">Протоколы FC-4, работающие в Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="480b0-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="480b0-133">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="480b0-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="480b0-134">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="480b0-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="480b0-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="480b0-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="480b0-136">**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="480b0-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="480b0-137">**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="480b0-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="480b0-138">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="480b0-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="480b0-139">**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="480b0-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="480b0-140">**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="480b0-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="480b0-141">**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="480b0-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="480b0-142">**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="480b0-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="480b0-143">**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="480b0-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="480b0-144">**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="480b0-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="480b0-145">**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="480b0-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="480b0-146">**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="480b0-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="480b0-147">**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="480b0-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="480b0-148">**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="480b0-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="480b0-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="480b0-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="480b0-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="480b0-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="480b0-151">**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="480b0-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="480b0-152">**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="480b0-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="480b0-153">**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="480b0-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="480b0-154">**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="480b0-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="480b0-155">**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="480b0-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="480b0-156">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="480b0-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="480b0-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="480b0-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="480b0-158">**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="480b0-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="480b0-159">**Порта**</span><span class="sxs-lookup"><span data-stu-id="480b0-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="480b0-160">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="480b0-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="480b0-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="480b0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="480b0-162">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="480b0-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="480b0-163">Режим включения для порта.</span><span class="sxs-lookup"><span data-stu-id="480b0-163">The enabled mode for the port.</span></span> <span data-ttu-id="480b0-164">Режимы порта определяются стандартом ANSI X3.</span><span class="sxs-lookup"><span data-stu-id="480b0-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="480b0-165">Если порт вошел в систему, это будет согласованный тип порта, в противном случае будет сообщено о настроенном типе порта.</span><span class="sxs-lookup"><span data-stu-id="480b0-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="480b0-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="480b0-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="480b0-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="480b0-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-168">Связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="480b0-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="480b0-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="480b0-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-170">Порт узла</span><span class="sxs-lookup"><span data-stu-id="480b0-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="480b0-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span><span class="sxs-lookup"><span data-stu-id="480b0-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-172">Порт узла, поддерживающий цикл арбитратед FC</span><span class="sxs-lookup"><span data-stu-id="480b0-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="480b0-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span><span class="sxs-lookup"><span data-stu-id="480b0-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="480b0-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="480b0-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-175">Порт может быть согласован, чтобы стать портом узла (N) или портом узла, поддерживающим цикл FC арбитратед (NL).</span><span class="sxs-lookup"><span data-stu-id="480b0-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="480b0-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="480b0-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-177">Порт расширения, соединяющий элементы структуры (например, коммутаторы FC)</span><span class="sxs-lookup"><span data-stu-id="480b0-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="480b0-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="480b0-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-179">Порт Fabric (element)</span><span class="sxs-lookup"><span data-stu-id="480b0-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="480b0-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span><span class="sxs-lookup"><span data-stu-id="480b0-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-181">Порт Fabric (element), поддерживающий цикл FC арбитратед</span><span class="sxs-lookup"><span data-stu-id="480b0-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="480b0-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="480b0-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-183">Порт моста</span><span class="sxs-lookup"><span data-stu-id="480b0-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="480b0-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="480b0-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="480b0-185">Порт может быть согласован, чтобы стать либо портом расширения (E), либо портом структуры (F).</span><span class="sxs-lookup"><span data-stu-id="480b0-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="480b0-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="480b0-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="480b0-187">**суппортедкос**</span><span class="sxs-lookup"><span data-stu-id="480b0-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="480b0-188">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="480b0-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="480b0-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="480b0-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="480b0-190">Параметры класса службы (COS), поддерживаемые адаптером Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="480b0-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="480b0-191">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="480b0-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="480b0-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="480b0-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="480b0-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="480b0-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="480b0-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="480b0-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="480b0-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="480b0-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="480b0-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="480b0-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="480b0-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="480b0-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="480b0-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="480b0-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="480b0-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="480b0-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="480b0-200">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="480b0-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="480b0-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="480b0-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="480b0-202">Протоколы FC-4, поддерживаемые адаптером Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="480b0-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="480b0-203">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="480b0-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="480b0-204">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="480b0-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="480b0-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="480b0-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="480b0-206">**IP-адрес через FC** (5)</span><span class="sxs-lookup"><span data-stu-id="480b0-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="480b0-207">**SCSI-ФКП** (8)</span><span class="sxs-lookup"><span data-stu-id="480b0-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="480b0-208">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="480b0-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="480b0-209">**Мастер IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="480b0-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="480b0-210">**Ведомый IPI-3** (18)</span><span class="sxs-lookup"><span data-stu-id="480b0-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="480b0-211">**Пиринг IPI-3** (19)</span><span class="sxs-lookup"><span data-stu-id="480b0-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="480b0-212">**Мастер CP-3** (21)</span><span class="sxs-lookup"><span data-stu-id="480b0-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="480b0-213">**Ведомость CP-3 Slave** (22)</span><span class="sxs-lookup"><span data-stu-id="480b0-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="480b0-214">**Узел CP IPI-3** (23)</span><span class="sxs-lookup"><span data-stu-id="480b0-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="480b0-215">**Канал сбккс** (25)</span><span class="sxs-lookup"><span data-stu-id="480b0-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="480b0-216">**Единица управления сбккс** (26)</span><span class="sxs-lookup"><span data-stu-id="480b0-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="480b0-217">**Канал FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="480b0-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="480b0-218">**Управляющая единица FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="480b0-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="480b0-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="480b0-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="480b0-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="480b0-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="480b0-221">**FC-протокол SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="480b0-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="480b0-222">**Хиппи-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="480b0-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="480b0-223">**Элемент управления ББЛ** (80)</span><span class="sxs-lookup"><span data-stu-id="480b0-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="480b0-224">**ББЛ FDDI инкапсулированный PDU ЛВС** (81)</span><span class="sxs-lookup"><span data-stu-id="480b0-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="480b0-225">**Ббл 802,3 инкапсулированного распределения ЛВС** (82)</span><span class="sxs-lookup"><span data-stu-id="480b0-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="480b0-226">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="480b0-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="480b0-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="480b0-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="480b0-228">**Уникальный поставщик** (255)</span><span class="sxs-lookup"><span data-stu-id="480b0-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="480b0-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="480b0-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="480b0-230">Требования</span><span class="sxs-lookup"><span data-stu-id="480b0-230">Requirements</span></span>



| <span data-ttu-id="480b0-231">Требование</span><span class="sxs-lookup"><span data-stu-id="480b0-231">Requirement</span></span> | <span data-ttu-id="480b0-232">Значение</span><span class="sxs-lookup"><span data-stu-id="480b0-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480b0-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="480b0-233">Minimum supported client</span></span><br/> | <span data-ttu-id="480b0-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="480b0-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="480b0-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="480b0-235">Minimum supported server</span></span><br/> | <span data-ttu-id="480b0-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="480b0-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="480b0-237">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="480b0-237">Namespace</span></span><br/>                | <span data-ttu-id="480b0-238">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="480b0-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="480b0-239">MOF</span><span class="sxs-lookup"><span data-stu-id="480b0-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="480b0-240"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="480b0-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="480b0-241">DLL</span><span class="sxs-lookup"><span data-stu-id="480b0-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="480b0-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="480b0-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="480b0-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="480b0-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480b0-244">**\_НЕТВОРКПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="480b0-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

