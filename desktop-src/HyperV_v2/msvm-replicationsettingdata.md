---
description: Представляет параметры репликации для виртуальной машины.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Класс Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265055"
---
# <a name="msvm_replicationsettingdata-class"></a>\_Класс мсвм репликатионсеттингдата

Представляет параметры репликации для виртуальной машины. Клиент передает экземпляр этого класса в [**мсвм \_ Репликатионсервице. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) для создания отношения репликации. Клиент не может напрямую изменять значения любого из свойств этого класса. для изменения значений необходимо вызвать метод [**мсвм \_ Репликатионсервице. модифирепликатионсеттингс.**](modifyreplicationsettings-msvm-replicationservice.md) Каждое отношение репликации имеет единственный экземпляр параметров.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ репликатионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ репликатионсеттингдата** имеет следующие свойства.

<dl> <dt>

**аддитионалсеттингс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные параметры репликации, которые может использовать поставщик конечной точки.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**аппликатионконсистентснапшотинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени между моментальными снимками, согласованными с приложениями, заданными в часах. Допустимые значения: от 1 до 12 часов.

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определите режим проверки подлинности, используемый для подключения к серверу восстановления.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Проверка подлинности Kerberos** (1)


</dt> <dd>

Аутентификация Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата** (2)


</dt> <dd>

Проверка подлинности на основе сертификата.

</dd> </dl>

</dd> <dt>

**аутоматикрековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется.

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**аутоматикшутдовнактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется.

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**аутоматикстартупактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется.

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**аутоматикстартупактионделай**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время задержки перед автоматическим запуском виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**аутоматикстартупактионсекуенценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**ауторесинчронизинаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли автоматически запускаться операции повторной синхронизации при возникновении ошибки репликации из-за сбоев питания и оборудования. Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .

Значение по умолчанию равно **False**.

</dd> <dt>

**ауторесинчронизеинтерваленд**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает время окончания для запуска автоматических операций повторной синхронизации. Это значение указано в местном времени. Значение по умолчанию — 06:00 (6:00 утра).

Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .

Операции повторной синхронизации также можно запланировать, чтобы они запускались в течение следующего интервала.

</dd> <dt>

**ауторесинчронизеинтервалстарт**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает время начала для запуска автоматических операций повторной синхронизации. Это значение указано в местном времени. Значение по умолчанию — 18:30 (6:30 вечера).

Операции повторной синхронизации активируются, только когда происходит сбой между временем, заданным в свойствах **ауторесинчронизеинтервалстарт** и **ауторесинчронизеинтерваленд** .

Операции повторной синхронизации также можно запланировать, чтобы они запускались в течение следующего интервала.

</dd> <dt>

**бипасспроксисервер**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли обходить прокси-сервер при соединении с сервером восстановления.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры репликации".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Отпечаток сертификата, используемый, если свойство **AuthenticationType** использует проверку подлинности на основе сертификата.

</dd> <dt>

**компрессионенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли сжаты данные репликации во время отправки на сервер восстановления.

</dd> <dt>

**конфигуратиондатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется.

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Файл ConfigurationFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины. Этот путь задается относительно свойства **конфигуратиондатарут** . Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания параметров виртуальной машины. Если этот объект представляет текущие параметры виртуальной машины, это значение будет соответствовать времени создания системы. Если этот объект представляет параметры моментального снимка для виртуальной машины, это значение будет соответствовать времени создания моментального снимка. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисистемсеттингс**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров репликации виртуальной машины".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и для него задается отображаемое имя виртуальной машины.

</dd> <dt>

**енаблевритеордерпресерватионакроссдискс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")
</dt> </dl>

Указывает, реплицируются ли все реплицируемые виртуальные жесткие диски виртуальной машины на тот же момент времени. Это гарантирует, что репликация будет учитывать порядок записи приложений на виртуальной машине.

**Windows 8.1:** Начиная с Windows 8.1 и Windows Server 2012 R2 это свойство является устаревшим и всегда имеет значение **true**.

</dd> <dt>

**инклудеддискс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **хипервембеддединстанце** ("CIM \_ сторажеаллокатионсеттингдата"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Список виртуальных жестких дисков (VHD), подключенных к системе, которые будут реплицироваться подсистемой репликации. Это массив строк, каждый из которых содержит **InstanceId** [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) , представляющего виртуальный жесткий диск.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)). Для Windows 8 всегда устанавливается значение «Microsoft:*GUID* \\ HVR». Для Windows 8.1 задано значение "Microsoft:*GUID виртуальной машины* \\ HVR \\<0/1>". В Windows 8.1 значение 0 указывает на первичный, а 1 — на расширенную репликацию. Дополнительные сведения о расширенной репликации см. в разделе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).

</dd> <dt>

**логдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация журнала для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется и не может быть задано.

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**примариконнектионпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя основной точки подключения. В случае с основным кластером это имя прикрепления брокера. В случае автономного сервера-источника это имя системы узла.

</dd> <dt>

**примарихостсистем**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Полное доменное имя основной хост-системы, в которой размещается виртуальная машина.

</dd> <dt>

**рековериконнектионпоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя точки подключения для восстановления. В случае кластера восстановления это имя ограничения брокера. В случае с автономным сервером восстановления это имя системы узла.

</dd> <dt>

**рековерифиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**рековерихистори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число моментальных снимков восстановления, которые будут храниться на сервере восстановления. Допустимые значения: от 0 до 24.

</dd> <dt>

**рековерихостсистем**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Полное доменное имя системы узла восстановления, в которой размещается виртуальная машина.

</dd> <dt>

**рековерисерверпортнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер порта сервера восстановления, используемый при обеспечении безопасного подключения для репликации.

</dd> <dt>

**репликатехостквпитемс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли реплицировать [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md)(только для узла) с основной виртуальной машины на виртуальную машину восстановления.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал репликации отношения репликации в секундах. Допустимые значения:

30

300

900

Значение по умолчанию — 300 секунд.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**репликатионпровидер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экземпляру класса [**мсвм \_ репликатионпровидер**](msvm-replicationprovider.md) , который идентифицирует конечную точку поставщика репликации.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**рутцертификатесумбпринт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Отпечаток корневого сертификата в используемом сертификате, если **AuthenticationType** имеет значение 2 (авторизация на основе сертификата).

</dd> <dt>

**снапшотдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**суспенддатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**свапфиледатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**виртуалсистемидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра. Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**виртуалсистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип виртуальной машины, которую представляют данные параметров. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и всегда имеет значение "Microsoft: Hyper-V: Реплика".

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

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**модифирепликатионсеттингс**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

