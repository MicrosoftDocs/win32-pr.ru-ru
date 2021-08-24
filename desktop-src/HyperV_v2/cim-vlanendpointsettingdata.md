---
description: Представляет данные конфигурации для конечной точки виртуальной ЛС.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Класс CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443d7b50ae8fe727a95464ec4e7fa589d7a08db770ce4c5090f37e5c988bfa4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682614"
---
# <a name="cim_vlanendpointsettingdata-class"></a>\_Класс CIM вланендпоинтсеттингдата

Представляет данные конфигурации для конечной точки виртуальной ЛС.

## <a name="syntax"></a>Синтаксис

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ вланендпоинтсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ вланендпоинтсеттингдата** имеет следующие свойства.

<dl> <dt>

**акцессвлан**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")
</dt> </dl>

VLAN для доступа к конечной точке.

</dd> <dt>

**дефаултвлан**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")
</dt> </dl>

Значение по умолчанию для собственной виртуальной ЛС в конечной точке магистрали.

> [!Note]  
> Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .

 

</dd> <dt>

**нативевлан**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")
</dt> </dl>

ИДЕНТИФИКАТОР виртуальной ЛС, который используется для обозначения трафика без тегов, полученного в конечной точке магистрали.

> [!Note]  
> Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **свитчендпоинтмоде** .

 

</dd> <dt>

**прунилигиблевланлист**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")
</dt> </dl>

Массив, содержащий идентификаторы виртуальных ЛС, которые система может удалить из конечной точки магистрали.

> [!Note]  
> Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .

 

</dd> <dt>

**трункедвланлист**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")
</dt> </dl>

Массив, содержащий идентификаторы конечных точек VLAN с включенной магистральной службой.

> [!Note]  
> Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

