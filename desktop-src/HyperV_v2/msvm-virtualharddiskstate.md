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
ms.openlocfilehash: c5896e8b19d2897084997bd01b65bbb0d6e80e0ca15f662fff38871bdc0b6755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426314"
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

### <a name="properties"></a>Элемент Property

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

**FileSize**
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
> добавлено в Windows 10 и Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетвиртуалхарддискстате**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




