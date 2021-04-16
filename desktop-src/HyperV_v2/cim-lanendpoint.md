---
description: Конечная точка связи, которая может подключаться к локальной сети для отправки и получения кадров данных. К конечным точкам локальной сети относятся интерфейсы Ethernet, Token Ring и FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Класс CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664778"
---
# <a name="cim_lanendpoint-class"></a>\_Класс CIM ланендпоинт

Конечная точка связи, которая может подключаться к локальной сети для отправки и получения кадров данных. К конечным точкам локальной сети относятся интерфейсы Ethernet, Token Ring и FDDI.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ланендпоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ ланендпоинт** имеет следующие свойства.

<dl> <dt>

**алиасаддрессес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий другие адреса одноадресной рассылки, которые могут использоваться для связи с конечной точкой локальной сети.

</dd> <dt>

**граупаддрессес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий адреса многоадресной рассылки, на которые прослушивается конечная точка локальной сети.

</dd> <dt>

**ланид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ланконнективитисегмент. ланид, CIM \_ лансегмент. ланид")
</dt> </dl>

Метка или идентификатор сегмента локальной сети, к которой подключена конечная точка. Если конечная точка в настоящее время не подключена или если эта информация неизвестна, **ланид** имеет значение null.

</dd> <dt>

**лантипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ протоколендпоинт**](cim-protocolendpoint.md).**ProtocolType**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ ЛАНКОННЕКТИВИТИСЕГМЕНТ. ConnectivityType, CIM \_ лансегмент. лантипе ")
</dt> </dl>

> [!Note]  
> Нерекомендуемое описание: тип технологии, используемой в локальной сети.

 

Это свойство использовать не рекомендуется. Вместо этого рекомендуется использовать свойство **ProtocolType** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**Токенринг** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Основной адрес одноадресной рассылки, используемый конечной точкой локальной сети.

MAC-адрес должен быть отформатирован со следующими характеристиками:

-   Адрес состоит из двенадцати шестнадцатеричных цифр.
-   Каждая пара цифр представляет один из шести октетов MAC-адреса.
-   Каждая пара цифр должна быть в каноническом порядке в соответствии с RFC 2469.

</dd> <dt>

**максдатасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")
</dt> </dl>

Максимальный размер (в байтах) полей данных, отправленных или полученных конечной точкой локальной сети.

</dd> <dt>

**осерлантипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ протоколендпоинт**](cim-protocolendpoint.md).**Осертипедескриптион**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ ланконнективитисегмент. Осертипедескриптион ","**CIM \_ LANEndpoint**.**Лантипе**")
</dt> </dl>

> [!Note]  
> Нерекомендуемое описание: тип технологии, используемой в локальной сети, если свойство **лантипе** имеет значение "1" (другое).

 

Это свойство использовать не рекомендуется. Вместо этого рекомендуется использовать свойство **осертипедескриптион** .

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

 

