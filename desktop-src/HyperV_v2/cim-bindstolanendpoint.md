---
description: Представляет ассоциацию, в которой \_ объект CIM сервицеакцесспоинт или CIM \_ протоколендпоинт зависит от базового \_ объекта CIM ланендпоинт в той же системе.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Класс CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664042"
---
# <a name="cim_bindstolanendpoint-class"></a>\_Класс CIM биндстоланендпоинт

Представляет ассоциацию, в которой объект [**CIM \_ Сервицеакцесспоинт**](cim-serviceaccesspoint.md) или [**CIM \_ Протоколендпоинт**](cim-protocolendpoint.md) зависит от базового объекта [**CIM \_ ланендпоинт**](cim-lanendpoint.md) в той же системе.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ биндстоланендпоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ биндстоланендпоинт** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ланендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Базовый объект [**CIM \_ ланендпоинт**](cim-lanendpoint.md) .

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Объект [**CIM \_ Сервицеакцесспоинт**](cim-serviceaccesspoint.md) или [**CIM \_ Протоколендпоинт**](cim-protocolendpoint.md) , который зависит от [**CIM \_ ланендпоинт**](cim-lanendpoint.md).

</dd> <dt>

**фраметипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метод кадрирования для точки доступа к службе верхнего уровня или конечной точки протокола.

> [!Note]  
> Для протокола IPX известно только использование RAW 802.3.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802,2** (2)


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**Привязать** (3)


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**RAW 802.3** (4)


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

[**\_БИНДСТО CIM**](cim-bindsto.md)
</dt> </dl>

 

