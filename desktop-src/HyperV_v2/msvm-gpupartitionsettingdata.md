---
description: Представляет настроенное состояние для устройства раздела GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Класс Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39fe0f5a794875c25cf844c39df2217fae04d1b791a5a5174358fa0ea70150ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014532"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>\_Класс мсвм гпупартитионсеттингдата

Представляет настроенное состояние для устройства раздела GPU.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ гпупартитионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ гпупартитионсеттингдата** имеет следующие свойства.

<dl> <dt>

**макспартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальный объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**макспартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**минпартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Минимальное количество ядер, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Минимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Минимальный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**минпартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Минимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионкомпуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Оптимальный объем модулей вычислений, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитиондекоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Оптимальный объем модулей декодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионенкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Оптимальный объем модулей кодирования, которые будут отображаться в разделе GPU.

</dd> <dt>

**оптималпартитионврам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Оптимальный объем видеопамяти, который будет отображаться в разделе GPU.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




