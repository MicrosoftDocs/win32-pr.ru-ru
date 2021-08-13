---
description: Представляет возможности и управление ленточным накопителем.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Класс CIM_TapeDrive (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b4c12dce8e67a2f46d9c7e7a1ab4ae0772b9e20517da6ab58c00c45a9ea8c71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646712"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a>Класс CIM_TapeDrive (Управление Hyper-V)

Представляет возможности и управление ленточным накопителем.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ TapeDrive** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ TapeDrive** имеет следующие свойства.

<dl> <dt>

**еотварнингзонесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Размер (в байтах) области, обозначенной как "конец ленты". Доступ в этой области приводит к возникновению предупреждения "конец ленты".

</dd> <dt>

**MaxPartitionCount**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число разделов для ленточного накопителя.

</dd> <dt>

**максревиндтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")
</dt> </dl>

Время (в миллисекундах) перехода с наиболее физической точки на ленте к началу.

</dd> <dt>

**Заполнение**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Число байтов, вставленных между блоками на ленточном носителе.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МЕДИААКЦЕССДЕВИЦЕ CIM**](cim-mediaaccessdevice.md)
</dt> </dl>

 

