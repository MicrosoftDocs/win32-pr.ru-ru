---
title: Класс MDM_DeviceManageability_Provider01_01
description: Класс MDM \_ девицеманажеабилити \_ Provider01 \_ 01 используется для получения общих сведений о возможностях конфигурации MDM на устройстве.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- Класс MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45fa96c71902bae9f6c7a98be8004b6f632fa0dad04952720f9a9c598879a03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825744"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a>\_Класс MDM девицеманажеабилити \_ Provider01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс MDM \_ девицеманажеабилити \_ Provider01 \_ 01 используется для получения общих сведений о возможностях конфигурации MDM на устройстве.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ девицеманажеабилити \_ Provider01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ девицеманажеабилити \_ Provider01 \_ 01** имеет эти свойства.

<dl> <dt>

[конфигинфо](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Необходимо задать значение для WMI \_ Bridge \_ Server. Вызывающий объект не может динамически задавать идентификатор поставщика.

</dd> <dt>

[енроллментинфо](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
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

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

