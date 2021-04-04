---
title: Класс MDM_DeviceStatus_Firewall01
description: Класс MDM \_ девицестатус \_ Firewall01 используется предприятием для запроса состояния соответствия брандмауэра устройствам с их политиками предприятия.
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- Класс MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803119"
---
# <a name="mdm_devicestatus_firewall01-class"></a>\_Класс MDM девицестатус \_ Firewall01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ девицестатус \_ Firewall01** используется предприятием для запроса состояния соответствия брандмауэра устройствам с их политиками предприятия.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ девицестатус \_ Firewall01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ девицестатус \_ Firewall01** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Узел для запроса брандмауэра.

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

[Состояние](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

