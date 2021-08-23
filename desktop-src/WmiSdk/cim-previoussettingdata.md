---
description: Связь между виртуальной системой и данными параметров моментального снимка, который является родительским для виртуальной системы.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Класс CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 85f08f22409df8a17bdae33ae81c06cb8167996ecb477f6a2d207d9e0ce2acca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131766"
---
# <a name="cim_previoussettingdata-class"></a>\_Класс CIM превиауссеттингдата

Связь между виртуальной системой и данными параметров моментального снимка, который является родительским для виртуальной системы.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ превиауссеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ превиауссеттингдата** имеет следующие свойства.

<dl> <dt>

**превиаусобжект**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Данные параметра моментального снимка, являющиеся родительскими для данной компьютерной системы.

</dd> <dt>

**Целевой объект**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Компьютерная система, которая была целью приложения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------|
| Пространство имен<br/> | Корневой \\ CIMV2<br/> |



 

 




