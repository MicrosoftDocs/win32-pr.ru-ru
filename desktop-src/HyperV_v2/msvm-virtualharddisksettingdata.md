---
description: Предоставляет данные настройки для виртуального жесткого диска.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Класс Msvm_VirtualHardDiskSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143891"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>\_Класс мсвм виртуалхарддисксеттингдата

Предоставляет данные настройки для виртуального жесткого диска.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалхарддисксеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалхарддисксеттингдата** имеет следующие свойства.

<dl> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Размер блока, используемого виртуальным жестким диском в байтах.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров виртуального жесткого диска".

</dd> <dt>

**Выравнивание по**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Задает требуемое выравнивание в байтах для полезных данных виртуального диска.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Настройка данных для виртуального жесткого диска".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Формат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Формат виртуального жесткого диска. Это может быть одно из следующих значений.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**Виртуальный жесткий диск** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**Вхдсет** (4)


</dt> <dd>

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**испмемкомпатибле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, можно ли использовать виртуальный диск в качестве резервного хранилища для устройства с энергонезависимой памятью.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**логикалсекторсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Размер логического сектора, используемого виртуальным жестким диском в байтах.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальный размер виртуального жесткого диска, отображаемый виртуальной машиной в байтах. Этот размер будет округляться до следующего большего числа, кратного размеру сектора.

</dd> <dt>

**парентидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID, используемый для уникальной идентификации родителя виртуального жесткого диска. Если виртуальный жесткий диск не имеет родителя, это поле будет пустым.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Родительский элемент виртуального жесткого диска. Если виртуальный жесткий диск не имеет родителя, это свойство будет пустым.

</dd> <dt>

**паренттиместамп**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка времени родителя виртуального жесткого диска. Если виртуальный жесткий диск не имеет родителя, это поле будет пустым.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**Путь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Полный путь к виртуальному жесткому диску.

</dd> <dt>

**фисикалсекторсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Размер физического сектора, используемый виртуальным жестким диском в байтах.

</dd> <dt>

**пмемаддрессабстрактионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Метод абстракции постоянных адресов памяти для использования с этим виртуальным диском.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**БТТ** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Тип виртуального жесткого диска. Это может быть одно из следующих значений.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Исправлено** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dynamic** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Разностное** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор GUID, используемый для уникальной идентификации виртуального диска.

Если метод [**мсвм \_ ). жетвиртуалхарддисксеттингдата**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) возвращает экземпляр **мсвм \_ виртуалхарддисксеттингдата**, клиент может использовать это свойство для получения уникального идентификатора диска VHD.

При обнаружении конфликтов или в противном случае клиент может задать значение **виртуалдискид** для нового идентификатора GUID и передать этот экземпляр **мсвм \_ виртуалхарддисксеттингдата** в метод [**мсвм \_ ). сетвиртуалхарддисксеттингдата**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) , чтобы изменить идентификатор диска VHD. Если виртуальный жесткий диск не является VHD-файлами или подключен к нему, операция завершается ошибкой. Операция также завершается ошибкой, если переданное значение имеет неправильный формат, то есть не GUID или все 0. Операция автоматически завершается успешно, если переданное значение совпадает с ИДЕНТИФИКАТОРом текущего диска.

Ошибки, создаваемые функцией [**сетвиртуалдискинформатион**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) , передаются через это свойство. Клиент также может использовать тот же механизм для предоставления значения **виртуалдискид** при создании виртуального жесткого диска с помощью метода [**Мсвм \_ ). креатевиртуалхарддиск**](createvirtualharddisk-msvm-imagemanagementservice.md) в том же пространстве имен. Это можно использовать для создания виртуальных жестких дисков VHD1 или VHD2.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**жетвиртуалхарддисксеттингдата**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

