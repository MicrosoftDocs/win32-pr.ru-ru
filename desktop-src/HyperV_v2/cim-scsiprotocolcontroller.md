---
description: Представляет контроллер протокола, управляющий интерфейсом SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Класс CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682809"
---
# <a name="cim_scsiprotocolcontroller-class"></a>\_Класс CIM сксипротоколконтроллер

Представляет контроллер протокола, управляющий интерфейсом SCSI.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сксипротоколконтроллер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сксипротоколконтроллер** имеет следующие свойства.

<dl> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сксипротоколконтроллер**.**Name**","**CIM \_ сксипротоколконтроллер**.**Осернамеформат**")
</dt> </dl>

Формат свойства **Name** объекта **CIM \_ сксипротоколконтроллер**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

**WWN порта FC** (2)


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

**имя iSCSI** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**осернамеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сксипротоколконтроллер**.**Name**","**CIM \_ сксипротоколконтроллер**.**Намеформат**")
</dt> </dl>

Описание свойства **намеформат** , когда параметру **намеформат** присвоено значение 1 (другое).

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

[**\_ПРОТОКОЛКОНТРОЛЛЕР CIM**](cim-protocolcontroller.md)
</dt> </dl>

 

