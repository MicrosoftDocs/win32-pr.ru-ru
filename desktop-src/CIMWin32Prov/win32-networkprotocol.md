---
description: '&Win32 \_ NetworkProtocol \# 8194; Класс WMI представляет протокол и его характеристики сети в компьютерной системе Win32.'
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Класс Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496596"
---
# <a name="win32_networkprotocol-class"></a>\_Класс Win32 NetworkProtocol

Класс **WMI \_ NetworkProtocol** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет протокол и его характеристики сети в компьютерной системе Win32.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ NetworkProtocol** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ NetworkProtocol** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**коннектионлесссервице**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows сокеты структурные \| \_ сведения о протоколе \| двсервицефлагс \| XP1 \_ без подключения")
</dt> </dl>

Протокол поддерживает службу без подключения. Служба без подключения (Datagram) описывает протокол связи или транспорт, в котором пакеты данных направляются независимо друг от друга и могут следовать разным маршрутам и поступать в порядке, отличном от того, в котором они были отправлены. И наоборот, служба, ориентированная на подключение, предоставляет виртуальный канал, через который пакеты данных получаются в том же порядке, в котором они были переданы. Если подключение между компьютерами завершается сбоем, приложение получает уведомления.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**гуарантисделивери**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ — гарантированная \_ Доставка")
</dt> </dl>

Протокол поддерживает доставку пакетов данных. Если этот флаг имеет **значение false**, это не значит, что все отправленные данные будут достигать предполагаемого назначения.

</dd> <dt>

**гуарантиссекуенЦинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows. \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ — гарантированный \_ порядок")
</dt> </dl>

Протокол гарантирует, что данные будут поступать в том порядке, в котором они были отправлены. Имейте в виду, что эта характеристика не гарантирует доставку данных, а только их порядок.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**максимумаддресссизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| имакссоккаддр"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")
</dt> </dl>

Максимальная длина адреса сокета, поддерживаемого протоколом. Адресами сокетов могут быть такие элементы, как URL-адрес ( `www.microsoft.com` ) или IP-адрес ( `130.215.24.1` ).

</dd> <dt>

**максимуммессажесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| двмессажесизе"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")
</dt> </dl>

Максимальный размер сообщения, поддерживаемый протоколом. Это максимальный размер сообщения, которое может быть отправлено или получено узлом. Для протоколов, которые не поддерживают Кадрирование сообщений, фактический максимальный размер сообщения, который может быть отправлен на указанный адрес, может быть меньше этого значения.

</dd> <dt>

**мессажеориентед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP с \_ ориентацией на сообщения \_ ")
</dt> </dl>

Протокол является ориентированным на сообщения. Протокол, ориентированный на сообщения, использует пакеты данных для пересылки информации. И наоборот, протоколы, ориентированные на потоковую передачу данных, передаются в виде непрерывного потока байтов.

</dd> <dt>

**минимумаддресссизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| иминсоккаддр"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")
</dt> </dl>

Минимальная длина адреса сокета, поддерживаемого протоколом.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows сокеты-структура \| сведения о протоколе \_ \| лппротокол")
</dt> </dl>

Имя протокола.

Пример: "TCP/IP"

</dd> <dt>

**псеудостреамориентед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ псевдо \_ -Stream")
</dt> </dl>

Протокол — это протокол, ориентированный на сообщения, который может принимать пакеты данных переменной длины или потоковые данные для всех операций получения. Эта необязательная возможность полезна, когда приложению не требуется, чтобы протокол закадрового сообщения, и требует характеристик, ориентированных на поток. Если **значение равно true**, то протокол является псевдо-ориентированным.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Строка, указывающая текущее состояние объекта. Можно определить операционное и нерабочее состояние. Оперативное состояние может включать "ОК", "деградация" и "пред Fail". "Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).

Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание". "Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**суппортсброадкастинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ поддерживает \_ трансляцию")
</dt> </dl>

Протокол поддерживает механизм вещания сообщений по сети.

</dd> <dt>

**суппортсконнектдата**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ Connect \_ Data")
</dt> </dl>

Протокол позволяет подключать данные по сети.

</dd> <dt>

**суппортсдисконнектдата**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ Disconnect \_ Data")
</dt> </dl>

Протокол позволяет отключать данные по сети.

</dd> <dt>

**суппортсенкриптион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ encrypted")
</dt> </dl>

Протокол поддерживает шифрование данных.

</dd> <dt>

**суппортсекспедитеддата**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе двсервицефлагс, \_ \| \| \_ срочные \_ данные")
</dt> </dl>

Протокол поддерживает срочные данные (также называемые срочными данными) по сети. Срочные данные могут обходить управление потоком и получить приоритет над обычными пакетами данных.

</dd> <dt>

**суппортсфрагментатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ ")
</dt> </dl>

Протокол поддерживает передачу данных во фрагментах. Максимальная физическая сеть (MTU) скрыта от приложений. Для каждого типа носителя не может быть превышен максимальный размер кадра. Слой ссылок обнаруживает MTU и сообщает об используемых протоколах.

</dd> <dt>

**суппортсграцефулклосинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ \_ " — корректное закрытие ")
</dt> </dl>

Протокол поддерживает операции поэтапного закрытия, также называемые «операциями мягкого закрытия». В противном случае протокол поддерживает только операции закрытия с прерываниями.

</dd> <dt>

**суппортсгуарантидбандвидс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе двсервицефлагс, \_ \| \| \_ распределение пропускной способности XP \_ ")
</dt> </dl>

Протокол имеет механизм для установления и поддержания пропускной способности.

</dd> <dt>

**суппортсмултикастинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ поддерживает \_ многоадресную рассылку")
</dt> </dl>

Протокол поддерживает многоадресную рассылку.

</dd> <dt>

**суппортскуалитйофсервице**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows: структуры \| всапротокол \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ ")
</dt> </dl>

Протокол поддерживает качество обслуживания (QoS) в базовом поставщике многоуровневой службы или транспортном перевозчике. Качество обслуживания — это набор компонентов, которые позволяют различать и сохранятся подмножества данных, передаваемых по сети. Качество обслуживания означает, что подмножества данных получают более высокий приоритет или гарантированную службу при прохождении по сети.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ NetworkProtocol** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).

## <a name="examples"></a>Примеры

В следующем примере кода VBScript показано, как получить список выполняющихся служб из экземпляров **Win32 \_ NetworkProtocol**.


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



В следующем образце кода Perl показано, как получить список выполняющихся служб из экземпляров **Win32 \_ NetworkProtocol**.


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
