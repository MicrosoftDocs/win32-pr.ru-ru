---
description: Конечная точка на коммутаторе или конечной станции, назначенная виртуальной ЛС, или принимает трафик от одной или нескольких виртуальных ЛС.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Класс CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143462"
---
# <a name="cim_vlanendpoint-class"></a>\_Класс CIM вланендпоинт

Конечная точка на коммутаторе или конечной станции, назначенная виртуальной ЛС, или принимает трафик от одной или нескольких виртуальных ЛС.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ вланендпоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ вланендпоинт** имеет следующие свойства.

<dl> <dt>

**десиредендпоинтмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**","**CIM \_ вланендпоинт**.**Осерендпоинтмоде**")
</dt> </dl>

Запрошенный режим VLAN для конечной точки.

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

**Туннель Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Зарезервировано поставщиком** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**десиредвлантрункенкапсулатион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ вланендпоинткапабилитиес. суппортстрункенкапсулатионнеготиатион", "**CIM \_ VLANEndpoint**.**Оператионалвлантрункенкапсулатион**","**CIM \_ вланендпоинт**.**Осертрункенкапсулатион**")
</dt> </dl>

Запрошенный тип инкапсуляции виртуальной ЛС.

> [!Note]  
> Это свойство используется только в том случае, если конечная точка VLAN находится в режиме магистрали.

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1 q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco острова** (4)


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

**Согласование** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (6.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768...)


</dt> <dd></dd> </dl>

</dd> <dt>

**гврпстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**, CIM \_ Вланендпоинткапабилитиес. Dot1QTagging ")
</dt> </dl>

Указывает, включен ли протокол регистрации VLAN Гарп (ГВРП) на конечной точке магистрали.

> [!Note]  
> Это свойство используется, только если ГВРП поддерживается конечной точкой, а режим магистрали включен.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**оператионалендпоинтмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ вланендпоинт**.**Осерендпоинтмоде**")
</dt> </dl>

Текущий режим VLAN для конечной точки.

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

**Туннель Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Зарезервировано поставщиком** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**оператионалвлантрункенкапсулатион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Осертрункенкапсулатион**","**CIM \_ вланендпоинт**.**Десиредвлантрункенкапсулатион**")
</dt> </dl>

Текущий тип инкапсуляции виртуальной ЛС.

> [!Note]  
> Это свойство используется только в том случае, если конечная точка VLAN находится в режиме магистрали.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1 q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco острова** (4)


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

**Согласование** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (6.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768...)


</dt> <dd></dd> </dl>

</dd> <dt>

**осерендпоинтмоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**")
</dt> </dl>

Тип модели конечной точки VLAN, поддерживаемой Вланендпоинт, если значение **десиредендпоинтмоде** равно "1" (другое); в противном случае **значение NULL**.

</dd> <dt>

**осертрункенкапсулатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредвлантрункенкапсулатион**","**CIM \_ вланендпоинт**.**Оператионалвлантрункенкапсулатион**")
</dt> </dl>

Тип инкапсуляции виртуальной ЛС, поддерживаемый конечной точкой VLAN, если значение свойства **десиредвлантрункенкапсулатион** равно 1 (другое); в противном случае **значение NULL**.

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

[**\_ПРОТОКОЛЕНДПОИНТ CIM**](cim-protocolendpoint.md)
</dt> </dl>

 

