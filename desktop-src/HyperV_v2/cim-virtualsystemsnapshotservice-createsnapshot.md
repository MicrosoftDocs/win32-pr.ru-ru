---
description: Создает моментальный снимок виртуальной системы.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Метод CreateSnapshot класса CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663993"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Метод CreateSnapshot \_ класса CIM виртуалсистемснапшотсервице

Создает моментальный снимок виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедсистем* \[ окне\]
</dt> <dd>

Ссылка [**CIM \_ ComputerSystem**](cim-computersystem.md) на затронутую виртуальную систему.

</dd> <dt>

*Снапшотсеттингс* \[ окне\]
</dt> <dd>

Параметры параметров.

</dd> <dt>

*Снапшоттипе* \[ окне\]
</dt> <dd>

Запрошенный тип моментального снимка:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Полный моментальный снимок** (2)


</dt> <dd>

Завершите создание моментального снимка виртуальной системы.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Моментальный снимок диска** (3)


</dt> <dd>

Моментальный снимок дисков виртуальной системы.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl> </dd> <dt>

*Ресултингснапшот* \[ в, out\]
</dt> <dd>

Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на полученный моментальный снимок виртуальной системы.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, при необходимости может быть возвращено задание. В этом случае экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новый моментальный снимок виртуальной системы, представлен с помощью связи [**CIM \_ аффектеджобелемент**](cim-affectedjobelement.md) со значением свойства **аффектеделемент** , ссылающегося на новый экземпляр класса **CIM \_ виртуалсистемсеттингдата** , представляющего моментальный снимок виртуальной системы, а значение **ElementEffects** установлено в 5 (Create).

> [!Note]  
> Этот параметр был доступен для чтения и записи в Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0; в противном случае возвращает ошибку.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Недопустимый тип** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕМСНАПШОТСЕРВИЦЕ CIM**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




