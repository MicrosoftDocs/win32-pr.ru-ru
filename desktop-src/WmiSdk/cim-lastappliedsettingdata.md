---
description: Связь между объектом и другим примененным к нему объектом.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Класс CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 6c1e5174cb9fcaf9279d16eceda547e9e5060c4ca4f7deda09cc170cf3dd7653
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244654"
---
# <a name="cim_lastappliedsettingdata-class"></a>\_Класс CIM ластапплиедсеттингдата

Связь между объектом и другим примененным к нему объектом.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ластапплиедсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ ластапплиедсеттингдата** имеет следующие свойства.

<dl> <dt>

**апплиедобжект**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Объект, примененный к целевому объекту.

</dd> <dt>

**Целевой объект**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Объект, который был целевым объектом приложения объекта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------|
| Пространство имен<br/> | Корневой \\ CIMV2<br/> |



 

 




