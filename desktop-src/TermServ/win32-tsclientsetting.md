---
title: Класс Win32_TSClientSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, связанного с политикой подключения.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSClientSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSClientSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff3e4eb9d99288914fb6d4e9a6e2d22aa38689cdc6b60f227e7e5ba2e0c5323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349368"
---
# <a name="win32_tsclientsetting-class"></a>\_Класс Win32 тсклиентсеттинг

Класс **WMI \_ Тсклиентсеттинг для Win32** определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , связанного с политикой подключения.

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсклиентсеттинг** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсклиентсеттинг** содержит следующие методы.



| Метод                                                                   | Описание                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionSettings**](win32-tsclientsetting-connectionsettings.md)   | Задает свойства **коннектклиентдривесатлогон**, **коннектпринтератлогон** и **дефаулттоклиентпринтер** этого класса.<br/>                      |
| [**сеталловдвм**](setallowdwm-win32-tsclientsetting.md)                 | Не поддерживается.<br/> **Windows 7 и Windows Server 2008 R2:** Задает свойство **алловдвм** .<br/>                                               |
| [**сетклиентпроперти**](win32-tsclientsetting-setclientproperty.md)     | Задает свойство **лптпортмаппинг**, **компортмаппинг**, **аудиомаппинг**, **клипбоардмаппинг**, **дривемаппинг** или **виндовспринтермаппинг** .<br/> |
| [**сетколордепс**](win32-tsclientsetting-setcolordepth.md)             | Задает свойство **clientareawidth** .<br/>                                                                                                                 |
| [**сетколордепсполици**](win32-tsclientsetting-setcolordepthpolicy.md) | Задает свойство **колордепсполици** .<br/>                                                                                                           |
| [**сетмаксмониторс**](setmaxmonitors-win32-tsclientsetting.md)           | Задает свойство **максмониторс** .<br/>                                                                                                                |
| [**сетмаксксресолутион**](setmaxxresolution-win32-tsclientsetting.md)     | Задает свойство **максксресолутион** .<br/>                                                                                                             |
| [**сетмаксиресолутион**](setmaxyresolution-win32-tsclientsetting.md)     | Задает свойство **максиресолутион** .<br/>                                                                                                             |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсклиентсеттинг** имеет следующие свойства.

<dl> <dt>

**адванцедремотеаппграфикс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

указывает, следует ли включить расширенную графику RemoteFX для RemoteApp.

**Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2012 R2 и Windows 8.1.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Дополнительные графические объекты отключены.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Расширенная графика включена.

</dd> </dl>

</dd> <dt>

**алловдвм**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство недоступно.

* * Windows 7 и Windows Server 2008 R2: * *

Указывает, следует ли включить или отключить композицию удаленного рабочего стола. Ноль отключит композицию удаленного рабочего стола, а ненулевое значение включит его.

Чтобы изменить это свойство, используйте метод [**сеталловдвм**](setallowdwm-win32-tsclientsetting.md) .

</dd> <dt>

**аудиокаптурередир**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли перенаправление захвата звука.

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**аудиомаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включено или отключено сопоставление звука.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление звука включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление звука отключено.

</dd> </dl>

</dd> <dt>

**AVC444ModePreferred**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, является ли режим AVC444 предпочтительным.

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** это свойство недоступно до Windows 10 или Windows Server 2016.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое описание (однострочная строка) объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**клипбоардмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, отключено или включено сопоставление буфера обмена.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление буфера обмена включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление буфера обмена отключено.

</dd> </dl>

</dd> <dt>

**Clientareawidth**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задает глубину цвета. Возможные значения см. в описании метода [**сетколордепс**](win32-tsclientsetting-setcolordepth.md) .

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span id="8_bit"></span><span id="8_BIT"></span>**8 бит** (1)


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span id="15_bit"></span><span id="15_BIT"></span>**15 бит** (2)


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span id="16_bit"></span><span id="16_BIT"></span>**16-разрядная** (3)


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span id="24_bit"></span><span id="24_BIT"></span>**24 бита** (4)


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span id="32_bit"></span><span id="32_BIT"></span>**32 бит** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**колордепсполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли переопределить параметр максимального цвета пользователя.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Не переопределяйте политику пользователя.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Переопределите политику пользователя.

</dd> </dl>

</dd> <dt>

**компортмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включено или отключено сопоставление COM-портов.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление COM-портов включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление COM-портов отключено.

</dd> </dl>

</dd> <dt>

**коннектклиентдривесатлогон**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли диски клиента автоматически подключены в процессе входа в систему.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Диски не будут автоматически подключены.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Диски будут автоматически подключены.

</dd> </dl>

</dd> <dt>

**ConnectionPolicy**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Политика, используемая сервером для получения параметров подключения пользователя.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)


</dt> <dd>

Параметры подключения пользователя вступают в действие.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)


</dt> <dd>

Параметры подключения пользователя переопределяются сервером.

</dd> </dl>

</dd> <dt>

**коннектпринтератлогон**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли все сопоставленные локальные принтеры клиента автоматически подключаться в процессе входа в систему.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Локальные принтеры не будут автоматически подключены.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Локальные принтеры будут автоматически подключены.

</dd> </dl>

</dd> <dt>

**дефаулттоклиентпринтер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли автоматически отправляться задания печати на локальный принтер клиента.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Задания печати не должны автоматически отправляться на локальный принтер клиента.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Задания печати должны автоматически отправляться на локальный принтер клиента.

</dd> </dl>

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**дривемаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включено или отключено сопоставление дисков.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление дисков включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление дисков отключено.

</dd> </dl>

</dd> <dt>

**енкодеимажекуалити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает качество образа для взаимодействия с RDP.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

**без потерь** (1)


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

**высокий** (2)


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

**средний** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**хардвареграфиксадаптер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, использует ли сервер узла сеансов удаленных рабочих столов аппаратный модуль визуализации графики в качестве адаптера по умолчанию.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF
</dt> </dl>

Дата установки объекта. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**лптпортмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, отключено или включено сопоставление LPT-портов.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление LPT-портов включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление LPT-портов отключено.

</dd> </dl>

</dd> <dt>

**максмониторс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число мониторов, поддерживаемое сервером. Чтобы изменить это свойство, используйте метод [**сетмаксмониторс**](setmaxmonitors-win32-tsclientsetting.md) .

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

</dd> <dt>

**максксресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное разрешение по оси X, поддерживаемое сервером. Чтобы изменить это свойство, используйте метод [**сетмаксксресолутион**](setmaxxresolution-win32-tsclientsetting.md) .

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

</dd> <dt>

**максиресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное разрешение по оси Y, поддерживаемое сервером. Чтобы изменить это свойство, используйте метод [**сетмаксиресолутион**](setmaxyresolution-win32-tsclientsetting.md) .

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**пнпредиректион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли перенаправление самонастраивающийся.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Разрешить перенаправление самонастраивающийся.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Не разрешать перенаправление самонастраивающийся.

</dd> </dl>

</dd> <dt>

**полициадванцедремотеаппграфикс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **адванцедремотеаппграфикс** сервером или групповой политикой.

**Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2012 R2 и Windows 8.1.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеалловдвм**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство недоступно.

* * Windows 7 и Windows Server 2008 R2: * *

Указывает, настроено ли свойство **алловдвм** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеаудиокаптурередир**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **аудиокаптурередир** сервером или групповой политикой.

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеаудиомаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **аудиомаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**PolicySourceAvc444ModePreferred**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настроено свойство **AVC444ModePreferredis** .

**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** это свойство недоступно до Windows 10 или Windows Server 2016.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеклипбоардмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **клипбоардмаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцеколордепс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **clientareawidth** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцеколордепсполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **колордепсполици** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцекомпортмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **компортмаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцедефаулттоклиентпринтер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **дефаулттоклиентпринтер** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцедривемаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **дривемаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцеенкодеимажекуалити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настраивается **енкодеимажекуалити** .

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцехардвареграфиксадаптер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настраивается **хардвареграфиксадаптер** .

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцелптпортмаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **лптпортмаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцемаксмониторс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **максмониторс** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

</dd> <dt>

**полицисаурцемаксресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроены ли свойства **максксресолутион** и **максиресолутион** сервером, групповой политикой или по умолчанию.

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцепнпредиректион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **пнпредиректион** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеремотесессионпрофиле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настраивается **ремотесессионпрофиле** .

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеселектнетворкдетект**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настроено свойство **селектнетворкдетект** .

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеселекттранспорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как настроено свойство **селекттранспорт** .

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцевидеоплайбаккредир**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **видеоплайбаккредир** сервером или групповой политикой.

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцевиндовспринтермаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **виндовспринтермаппинг** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**ремотесессионпрофиле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает профиль для взаимодействия с RDP.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

<span id="scale"></span><span id="SCALE"></span>

**масштаб** (1)


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

**опыт** (2)


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

**пропускная способность** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**селектнетворкдетект**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, используется ли обнаружение сети.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

используется во время подключения и в стабильном состоянии.

</dd> <dt>

1
</dt> <dd>

отключено во время подключения

</dd> <dt>

2
</dt> <dd>

отключено в стабильном состоянии

</dd> <dt>

3
</dt> <dd>

отключено во время подключения и в стабильном состоянии.

</dd> </dl>

</dd> <dt>

**селекттранспорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, какие транспортные протоколы можно использовать для доступа к серверу по протоколу RDP.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** это свойство недоступно до Windows 8 или Windows Server 2012.

<dt>

0
</dt> <dd>

Используйте как UDP, так и TCP.

</dd> <dt>

1
</dt> <dd>

Используйте только TCP.

</dd> <dt>

2
</dt> <dd>

Используйте либо UDP, либо TCP.

</dd> </dl>

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

<dt>



 ("ОК")


</dt> <dd></dd> <dt>



 ("Ошибка")


</dt> <dd></dd> <dt>



 ("Пониженное состояние")


</dt> <dd></dd> <dt>



 ("Неизвестно")


</dt> <dd></dd> <dt>



 ("Пред Fail")


</dt> <dd></dd> <dt>



 ("Запуск")


</dt> <dd></dd> <dt>



 ("Остановка")


</dt> <dd></dd> <dt>



 ("Служба")


</dt> <dd></dd> </dl>

</dd> <dt>

**терминалнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя терминала.

Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).

</dd> <dt>

**видеоплайбаккредир**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли перенаправление воспроизведения видео.

**Windows Server 2008 и Windows Vista:** это свойство недоступно до Windows Server 2008 R2 и Windows 7.

<dt>

<span id="FALSE"></span><span id="false"></span>

**False** (0)


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

**True** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**виндовспринтермаппинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включено ли сопоставление принтеров для окна клиента.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Сопоставление принтеров включено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Сопоставление принтеров отключено.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Имейте в виду, что станция окна, связанная с сеансом консоли, не может получить доступ к методам и свойствам этого класса. Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства **терминалнаме** , методы этого объекта будут возвращать **WBEM \_ E \_ не \_ поддерживаются**. Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.

Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.

в следующем примере Visual Basic scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминал Win32**](win32-terminal.md)
</dt> <dt>

[**\_Терминалсеттинг Win32**](win32-terminalsetting.md)
</dt> <dt>

[**\_Параметр CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

