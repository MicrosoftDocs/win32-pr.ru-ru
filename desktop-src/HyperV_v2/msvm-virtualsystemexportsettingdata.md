---
description: Предоставляет дополнительные сведения для использования с методом Експортсистемдефинитион \_ класса Виртуалсистемманажементсервице мсвм.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Класс Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682504"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>\_Класс мсвм виртуалсистемекспортсеттингдата

Предоставляет дополнительные сведения для использования с методом [**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемекспортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемекспортсеттингдата** имеет следующие свойства.

<dl> <dt>

**баккупинтент**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает цель использования экспортированных резервных наборов данных.

> [!Note]  
> Это свойство было добавлено в Windows 10 и Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Баккупинтентпресервечаин** (0)


</dt> <dd>

Все экспортированные полные и разностные резервные наборы данных будут сохраняться по мере их возникновения.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Баккупинтентмерже** (1)


</dt> <dd>

Экспортированные полные и разностные резервные наборы данных будут объединены для создания полных резервных наборов данных.

</dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**каптуреливестате**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, какое состояние следует записать, если целевой объект экспорта является работающей виртуальной машиной.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**Каптурекрашконсистентстате** (0)


</dt> <dd>

Файлы сохраненного состояния не будут экспортированы для работающей виртуальной машины, поместив ее в состояние сбоя.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**Каптуресаведстате** (1)


</dt> <dd>

Файлы сохраненного состояния для работающей виртуальной машины будут экспортированы вместе с конфигурацией виртуальной машины.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**Каптуреаппконсистентстате** (2)


</dt> <dd>

Будет экспортировано состояние работающей виртуальной машины в режиме совместимости приложений.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**кописнапшотконфигуратион**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, какие моментальные снимки должны быть экспортированы с помощью виртуальной машины.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**Експорталлснапшотс** (0)


</dt> <dd>

Все моментальные снимки будут экспортированы с помощью виртуальной машины.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**Експортноснапшотс** (1)


</dt> <dd>

Моментальные снимки не будут экспортированы с виртуальной машиной.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**Експортонеснапшот** (2)


</dt> <dd>

Моментальные снимки, определяемые свойством **снапшотвиртуалсистем** , будут экспортированы вместе с виртуальной машиной. Свойства **копивмстораже** и **копивмрунтимеинформатион** не учитываются, сведения о хранилище и времени выполнения экспортируются вместе с виртуальной машиной, а все разностные диски VHD будут ОБЪЕДИНЕНЫ в новый виртуальный жесткий диск.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**Експортонеснапшотфорбаккуп** (3)


</dt> <dd>

Моментальный снимок, определяемый свойством **снапшотвиртуалсистем** , будет экспортирован в целях резервного копирования виртуальной машины. Экспортированная конфигурация будет использовать идентификатор виртуальной машины.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**копивмрунтимеинформатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, будут ли копироваться сведения о времени выполнения виртуальной машины при экспорте виртуальной машины.



| Значение                                                                                | Значение                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Сведения о времени выполнения виртуальной машины будут скопированы.<br/>     |
| <dl> <dt>**Неверно**</dt> </dl> | Сведения о времени выполнения виртуальной машины не будут скопированы.<br/> |



 

</dd> <dt>

**копивмстораже**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, будет ли копироваться хранилище виртуальной машины при экспорте виртуальной машины.



| Значение                                                                                | Значение                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Будет скопировано хранилище виртуальной машины.<br/>     |
| <dl> <dt>**Неверно**</dt> </dl> | Хранилище виртуальной машины не будет скопировано.<br/> |



 

</dd> <dt>

**креатевмекспортсубдиректори**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, будет ли создаваться подкаталог с именем виртуальной машины при экспорте виртуальной машины.



| Значение                                                                                | Значение                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Будет создан подкаталог.<br/>     |
| <dl> <dt>**Неверно**</dt> </dl> | Подкаталог не будет создан.<br/> |



 

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**дифферентиалбаккупбасе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

База для разностного экспорта. Это путь к экземпляру [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , который представляет точку ссылки или путь к экземпляру [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который представляет моментальный снимок, используемый в качестве основы для разностного экспорта. Если свойство **кописнапшотконфигуратион** не имеет значение 3 (**експортонеснапшотфорбаккуп**), это свойство игнорируется.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**дисабледифферентиалофигноредстораже**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, будут ли создаваться разностные диски или нет для хранилища, пропущенного во время экспорта. По умолчанию установлено значение false, что означает, что разностные диски создаются для хранилища, которое не будет скопировано в назначение экспорта.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя для этого экземпляра. Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**ексклудедвиртуалхарддискс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив идентификаторов экземпляров [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) (расд), которые представляют виртуальные жесткие диски, запрашиваемые для исключения из операции экспорта. Если хотя бы один из предоставленных идентификаторов не является допустимым подключенным виртуальным жестким диском, операция завершится ошибкой.

Виртуальные жесткие диски, на которые ссылается это свойство, могут быть из виртуальной машины и (или) из моментальных снимков. Исключение виртуальных жестких дисков не поддерживается, если свойство **кописнапшотконфигуратион** имеет значение 0 (експорталлснапшотс).

Обратите внимание, что идентификатор экземпляра РАСД для виртуальных жестких дисков представляет расположение, к которому они присоединены, и исключение через этот идентификатор исключает все виртуальные жесткие диски, подключенные в этом расположении в дереве моментальных снимков виртуальной машины, независимо от того, действительно ли они являются действительной цепочкой виртуальных жестких дисков.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**експортфорливемигратион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, должна ли экспортированная виртуальная машина использоваться в динамической миграции.

> [!Note]  
> Добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

В области создания экземпляра пространства имен непрозрачно и уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**снапшотвиртуалсистем**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Путь к экземпляру [**\_ виртуалсистемсеттингдата мсвм**](msvm-virtualsystemsettingdata.md) , который представляет моментальный снимок, экспортируемый с виртуальной машиной. Если свойство **кописнапшотконфигуратион** не имеет значение 2 (експортонеснапшот), это свойство игнорируется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуалсистемекспортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> <dt>

[**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

