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
# <a name="cim_fcport-class"></a>\_Класс CIM фкпорт

> [!NOTE]
> Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его. Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.

Представляет возможности и управление устройством порта Fibre Channel (FC).

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

> [!NOTE]
> Эта статья содержит ссылки на термин slave (ведомый). Корпорация Майкрософт больше не использует его. Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.

Класс **CIM \_ фкпорт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ фкпорт** имеет следующие свойства.

<dl> <dt>

**активекос**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фкпорт**.**Суппортедкос**")
</dt> </dl>

Параметры активного класса службы (COS) для Fibre Channel.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1)


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2)


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3)


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4)


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5)


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6)


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фкпорт**.**SupportedFC4Types**")
</dt> </dl>

Протоколы FC-4, работающие в Fibre Channel.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4)


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

**IP-адрес через FC** (5)


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-ФКП** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**Мастер IPI-3** (17)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**Ведомый IPI-3** (18)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**Пиринг IPI-3** (19)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**Мастер CP-3** (21)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**Ведомость CP-3 Slave** (22)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**Узел CP IPI-3** (23)


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**Канал сбккс** (25)


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**Единица управления сбккс** (26)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**Канал FC-SB-2** (27)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**Управляющая единица FC-SB-2** (28)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34)


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-протокол SNMP** (36)


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**Хиппи-FP** (64)


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**Элемент управления ББЛ** (80)


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**ББЛ FDDI инкапсулированный PDU ЛВС** (81)


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**Ббл 802,3 инкапсулированного распределения ЛВС** (82)


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88)


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96)


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**Уникальный поставщик** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**Порта**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")
</dt> </dl>

Режим включения для порта. Режимы порта определяются стандартом ANSI X3. Если порт вошел в систему, это будет согласованный тип порта, в противном случае будет сообщено о настроенном типе порта.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd>

Связанное свойство **осерпорттипе** содержит строковое описание типа порта.

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span id="N"></span><span id="n"></span>**N** (10)


</dt> <dd>

Порт узла

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span id="NL"></span><span id="nl"></span>**NL** (11)


</dt> <dd>

Порт узла, поддерживающий цикл арбитратед FC

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)


</dt> <dd>

Порт может быть согласован, чтобы стать портом узла (N) или портом узла, поддерживающим цикл FC арбитратед (NL).

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (14)


</dt> <dd>

Порт расширения, соединяющий элементы структуры (например, коммутаторы FC)

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span id="F"></span><span id="f"></span>**F** (15)


</dt> <dd>

Порт Fabric (element)

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span id="FL"></span><span id="fl"></span>**FL** (16)


</dt> <dd>

Порт Fabric (element), поддерживающий цикл FC арбитратед

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (17)


</dt> <dd>

Порт моста

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span id="G"></span><span id="g"></span>**G** (18)


</dt> <dd>

Порт может быть согласован, чтобы стать либо портом расширения (E), либо портом структуры (F).

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (16000.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**суппортедкос**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметры класса службы (COS), поддерживаемые адаптером Fibre Channel.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1)


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2)


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3)


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4)


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5)


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6)


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Протоколы FC-4, поддерживаемые адаптером Fibre Channel.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4)


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

**IP-адрес через FC** (5)


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-ФКП** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**Мастер IPI-3** (17)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**Ведомый IPI-3** (18)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**Пиринг IPI-3** (19)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**Мастер CP-3** (21)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**Ведомость CP-3 Slave** (22)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**Узел CP IPI-3** (23)


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**Канал сбккс** (25)


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**Единица управления сбккс** (26)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**Канал FC-SB-2** (27)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**Управляющая единица FC-SB-2** (28)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34)


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-протокол SNMP** (36)


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**Хиппи-FP** (64)


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**Элемент управления ББЛ** (80)


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**ББЛ FDDI инкапсулированный PDU ЛВС** (81)


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**Ббл 802,3 инкапсулированного распределения ЛВС** (82)


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88)


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96)


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**Уникальный поставщик** (255)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_НЕТВОРКПОРТ CIM**](cim-networkport.md)
</dt> </dl>

 

