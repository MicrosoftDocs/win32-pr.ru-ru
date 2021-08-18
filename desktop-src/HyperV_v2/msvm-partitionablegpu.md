---
description: Представляет секционированный GPU. Каждый GPU может быть разбит на несколько разделов GPU, которые могут быть назначены виртуальной машине в виде виртуального видеонабора.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Класс Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15ce369a0186ae6309f90a5b37a77a35cce90ae6997e3c8cbc7e968a0a0d0de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148297"
---
# <a name="msvm_partitionablegpu-class"></a>\_Класс мсвм партитионаблегпу

Представляет секционированный GPU. Каждый GPU может быть разбит на несколько разделов GPU, которые могут быть назначены виртуальной машине в виде виртуального видеонабора.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ партитионаблегпу** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ партитионаблегпу** имеет следующие свойства.

<dl> <dt>

**аваилаблекомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступный объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**аваилабледекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**аваилаблинкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступный объем модулей кодирования, который будет отображаться в разделе GPU.

</dd> <dt>

**аваилаблеврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**макспартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**минпартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальное количество ядер, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальноеный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оптимальный объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оптимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оптимальный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оптимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Объем разделов GPU, на которые разбит физический GPU.

</dd> <dt>

**тоталкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**тоталдекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**тоталенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**тоталврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**валидпартитионкаунтс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив допустимых параметров раздела GPU, в который может быть разбит физический GPU.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> </dl>

 

 




