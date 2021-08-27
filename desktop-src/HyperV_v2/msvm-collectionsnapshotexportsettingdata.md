---
description: Экспорт данных параметров, передаваемых в метод Експортснапшот \_ класса мсвм коллектионснапшотсервице.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Класс Msvm_CollectionSnapshotExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd148b7ea73bf7c2eaff7f648c7084c37a8669779515749611c675e7f5564d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130634"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>\_Класс мсвм коллектионснапшотекспортсеттингдата

Экспорт данных параметров, передаваемых в метод Експортснапшот класса [**мсвм \_ коллектионснапшотсервице**](msvm-collectionsnapshotservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионснапшотекспортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ коллектионснапшотекспортсеттингдата** имеет следующие свойства.

<dl> <dt>

**баккупинтент**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает цель использования экспортированных резервных наборов данных:

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Баккупинтентпресервечаин** (1)


</dt> <dd>

Все экспортированные полные и разностные резервные наборы данных будут сохраняться по мере их возникновения.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Баккупинтентмерже** (2)


</dt> <dd>

Экспортированные полные и разностные резервные наборы данных будут объединены для создания полных резервных наборов данных.

</dd> </dl>

</dd> <dt>

**копивмстораже**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, при экспорте виртуальной машины хранилище виртуальной машины будет скопировано. В противном случае — **значение false.**

</dd> <dt>

**дифферентиалбаккупбасе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

База для разностного экспорта. Это путь к экземпляру [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) , который представляет точку ссылки, или путь к экземпляру [**мсвм \_ снапшотколлектион**](msvm-snapshotcollection.md) , который представляет моментальный снимок, который будет использоваться в качестве основы для разностного экспорта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




