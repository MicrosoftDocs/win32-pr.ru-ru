---
description: Предоставляет сведения о состоянии для существующего образа виртуального жесткого диска.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Класс Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497019"
---
# <a name="msvm_virtualharddiskstate-class"></a>\_Класс мсвм виртуалхарддискстате

Предоставляет сведения о состоянии для существующего образа виртуального жесткого диска.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалхарддискстате** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалхарддискстате** имеет следующие свойства.

<dl> <dt>

**Выравнивание**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задает тип выравнивания виртуального жесткого диска. Это может быть одно из следующих значений.



| Значение                                                                        | Значение                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | 512. выравнивание по байтам.<br/> |
| <dl> <dt>1</dt> </dl> | Выравнивание по 4 КБ.<br/>     |



 

</dd> <dt>

**Размер файла**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер файла виртуального жесткого диска (фактического объема хранилища, используемого файлом) в байтах.

</dd> <dt>

**фрагментатионперцентаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приблизительное число блоков виртуальных дисков, фрагментированных в файле виртуального жесткого диска.

</dd> <dt>

**Используемых**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство зарезервировано для дальнейшего использования.

</dd> <dt>

**мининтерналсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный размер, до которого может быть сжат виртуальный жесткий диск, в байтах. Этот размер округляется до следующего большего числа, кратного размеру сектора.

</dd> <dt>

**фисикалсекторсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Физический размер сектора, используемый базовым физическим диском в байтах.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка времени виртуального жесткого диска

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетвиртуалхарддискстате**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




