---
description: Представляет параметры миграции для миграции виртуальной системы и хранилища, подключенного к виртуальной системе.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Класс Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896822"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>\_Класс мсвм виртуалсистеммигратионсеттингдата

Представляет параметры миграции для миграции виртуальной системы и хранилища, подключенного к виртуальной системе.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистеммигратионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистеммигратионсеттингдата** имеет следующие свойства.

<dl> <dt>

**аллововервритиксистингфиле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Разрешить операции миграции хранилища перезаписывать существующие VHDX-файлы.

> [!Note]  
> Это свойство было добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**авоидремовингвхдс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не удаляйте виртуальные жесткие диски во время миграции, т. е. виртуальные жесткие диски в источнике на сукцессанд виртуальных жестких дисках в случае сбоя.

> [!Note]  
> Добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**Пропускная способность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает пропускную способность, назначенную или запрошенную для операции миграции виртуальной системы. Единицы пропускной способности задаются свойством **бандвидсунит** . В рамках миграции значение 0 указывает пропускную способность по умолчанию. В противном случае значение 0 указывает, что пропускная способность не поддерживается.

**Пропускную способность** и **приоритет** можно использовать в сочетании. Процессы миграции, имеющие наивысшее значение приоритета, совместно используют доступную пропускную способность в зависимости от запрошенной пропускной способности. Если этот набор процессов потребляет не всю пропускную способность, процессы миграции со следующим меньшим приоритетом совместно используют оставшуюся пропускную способность. Если по-прежнему пропускная способность остается, рассматриваются процессы миграции со следующим меньшим приоритетом и т. д.

Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

</dd> <dt>

**бандвидсунит**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает единицы, используемые свойством **пропускной способности** . Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 DSP0004 V 2.4 или более поздней версии.

Если значение этого свойства равно "Percent", значение свойства **пропускной способности** должно находиться в диапазоне от 0 до 100 с более высокими значениями, указывающими на более высокую пропускную способность. Значение 100 указывает общую доступную пропускную способность для выполнения операций миграции виртуальной системы. Значения от 1 до 100 должны линейно сопоставляться с доступным диапазоном пропускной способности. Например, значение 50 должно запрашивать половину доступной пропускной способности.

Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

</dd> <dt>

**канцелифблаккаутсрешолдексцеедед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Отменяет миграцию, если превышено пороговое значение времени ожидания.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**кпукаппингмагнитуде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("кпукаппингмагнитуде")
</dt> </dl>

Степень выделения ЦП во время миграции.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Обычная** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Низкая** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Высокий** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**дестинатионипаддресслист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Это значение будет **равно NULL** для миграции хранилища. Для миграции виртуальной системы это может содержать список IP-адресов узла назначения.

</dd> <dt>

**дестинатионпланнедвиртуалсистемид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если запланированная виртуальная машина существует в месте назначения миграции, для этого свойства будет задан идентификатор GUID целевой виртуальной машины, на которой требуется выполнить миграцию виртуальной машины. Это полезно в случаях, когда пользователь создал запланированную виртуальную машину в месте назначения, а также настройку ресурсов и хочет, чтобы виртуальная машина из источника была перенесена на эту запланированную виртуальную машину.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, следует ли сжимать трафик динамической миграции. **Значение true** указывает, что необходимо сжать; в противном случае — **false**.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("мигратионтипе")
</dt> </dl>

Указывает тип выполняемой операции миграции. Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**Виртуалсистем** (32768)


</dt> <dd>

Переносит виртуальную систему на целевой узел.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Хранилище** (32769)


</dt> <dd>

Переносит только ресурсы хранилища виртуальной системы.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Промежуточный** (32770)


</dt> <dd>

С помощью конфигурации виртуальной системы создает запланированную виртуальную систему на целевом узле.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**Виртуалсистемандстораже** (32771)


</dt> <dd>

Переносит виртуальную систему и ее хранилище на целевой узел.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**Сторажедипчекк** (32772)


</dt> <dd>

Выполняет проверку возможности миграции ресурсов хранилища виртуальной системы на целевом узле.

</dd> </dl>

</dd> <dt>

**осертранспорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип транспорта, применяемого, если значение **TransportType** равно 1 (другое). Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает важность относительной миграции, которую система миграции может использовать для упорядочения или иным образом предоставлять предпочтение для нескольких ожидающих запросов на миграцию. Чем ниже значение, тем выше приоритет. В рамках миграции значение 0 указывает приоритет по умолчанию. В противном случае значение 0 указывает, что приоритеты не поддерживаются.

Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

</dd> <dt>

**ремовесаурцеунманажедвхдс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Удалите исходные неуправляемые виртуальные жесткие диски.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**ретаинвхдкопиесонсаурце**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Для миграции хранилища указывает, следует ли удалять виртуальные жесткие диски только для чтения на исходном узле после завершения миграции.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")
</dt> </dl>

Указывает тип транспорта, применяемого для операции миграции виртуальной системы. Это свойство наследуется от **CIM \_ виртуалсистеммигратионсеттингдата**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS-точность** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768...)


</dt> <dd></dd> </dl>

Для динамической миграции это свойство указывает тип транспорта, используемый для передачи состояния виртуальной системы на целевой узел. Поддерживаются такие значения:

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Указывает тип транспорта TCP.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Указывает тип транспорта для передачи состояния виртуальной машины — SMB.

</dd> </dl>

</dd> <dt>

**унманажедвхдс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ мовеунманажедвхд")
</dt> </dl>

Массив внедренных экземпляров [**мсвм \_ мовеунманажедвхд**](msvm-moveunmanagedvhd.md) , которые содержат неуправляемые сведения о виртуальных жестких дисках.

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

[**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕТТИНГДАТА CIM**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**мигратевиртуалсистемтохост**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

