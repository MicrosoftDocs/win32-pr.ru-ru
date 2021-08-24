---
description: Представляет параметры для выделения порта Ethernet в дополнение к параметрам, предоставленным \_ классом ЕСЕРНЕТПОРТ CIM. Эти параметры используются для предоставления сведений, относящихся к самому ресурсу.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Класс CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7546af167a6e13712119a081e7dbfaee118dc0c8a4912b8411d898a4ad90bc7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695804"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a>\_Класс CIM есернетпорталлокатионсеттингдата

Представляет параметры для выделения порта Ethernet в дополнение к параметрам, предоставленным классом [**\_ есернетпорт CIM**](cim-ethernetport.md) . Эти параметры используются для предоставления сведений, относящихся к самому ресурсу.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ есернетпорталлокатионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ есернетпорталлокатионсеттингдата** имеет следующие свойства.

<dl> <dt>

**десиредвланендпоинтмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**","**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ есернетпорталлокатионсеттингдата**.**Осерендпоинтмоде**")
</dt> </dl>

Запрошенный режим VLAN. Это свойство используется для задания значения начального свойства **оператионалендпоинтмоде** в экземпляре **CIM \_ вланендпоинт** , связанного с портом Ethernet.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Доступ** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Динамическое автоматическое** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Желательно динамически** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Магистраль** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Tunnel Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (0x8000.. 0XFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**осерендпоинтмоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорталлокатионсеттингдата**.**Десиредвланендпоинтмоде**")
</dt> </dl>

Тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN, если для свойства Mode задано значение 1 (другое). Этому свойству следует присвоить значение **null** , если свойство Mode имеет любое значение, отличное от "1".

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

