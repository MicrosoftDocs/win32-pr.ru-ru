---
title: Класс MDM_DeviceStatus_NetworkIdentifiers01_01
description: Класс MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01 позволяет запрашивать свойства сети на устройстве.
ms.assetid: 2439010e-62fa-4482-b280-b9f98d1fbb7b
keywords:
- Класс MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_NetworkIdentifiers01_01
- MDM_DeviceStatus_NetworkIdentifiers01_01.InstanceID
- MDM_DeviceStatus_NetworkIdentifiers01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034b3b24c6b81bc5afc4ebf9b8fee28b9fccccfbe96e55d29f6f4123882762c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088164"
---
# <a name="mdm_devicestatus_networkidentifiers01_01-class"></a>\_Класс MDM девицестатус \_ NetworkIdentifiers01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** позволяет запрашивать свойства сети на устройстве.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_NetworkIdentifiers01_01
{
  string  InstanceID;
  string  ParentID;
  string  IPAddressV4;
  string  IPAddressV6;
  boolean IsConnected;
  sint32  Type;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ девицестатус \_ NetworkIdentifiers01 \_ 01** имеет эти свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Узел для запросов к свойствам сети и устройства.

</dd> <dt>

[IPAddressV4](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv4)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[IPAddressV6](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-ipaddressv6)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Подсоединено](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-isconnected)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/девицестатус"

</dd> <dt>

[Тип](/windows/client-management/mdm/devicestatus-csp#devicestatus-networkidentifiers-macaddress-type)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

