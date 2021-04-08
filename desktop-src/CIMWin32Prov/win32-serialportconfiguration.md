---
description: '\_Класс WMI сериалпортконфигуратион для Win32 представляет параметры передачи данных в последовательном порте на основе Windows. К ним относятся конфигурации для установления соединения и проверки ошибок.'
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Класс Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990388"
---
# <a name="win32_serialportconfiguration-class"></a>\_Класс Win32 сериалпортконфигуратион

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ сериалпортконфигуратион для Win32** представляет параметры передачи данных в последовательном порте на основе Windows. К ним относятся конфигурации для установления соединения и проверки ошибок.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сериалпортконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ сериалпортконфигуратион** имеет следующие свойства.

<dl> <dt>

**абортреадвритеонеррор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фабортонеррор")
</dt> </dl>

Если задано **значение true**, операции чтения и записи завершаются при возникновении ошибки. Если **значение — true**, драйвер прерывает все операции чтения и записи с состоянием ошибки в случае возникновения ошибки. Драйвер не будет принимать дальнейшие операции связи, пока приложение не подтвердит ошибку.

</dd> <dt>

**Порта**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| скорость")
</dt> </dl>

Скорость (в битах в секунду), с которой работает коммуникационное устройство.

Пример: 9600

</dd> <dt>

**бинаримодинаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фбинари")
</dt> </dl>

Если задано **значение true**, передача данных в двоичном режиме включается для последовательного порта. Компьютерные системы, работающие под Windows, разрешают только двоичные передачи через последовательные порты, поэтому это значение всегда равно **true**.

</dd> <dt>

**битспербите**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| битесизе")
</dt> </dl>

Количество бит, переданных и полученных для каждого байта данных для последовательного порта Windows. Это число может отличаться в зависимости от разрядов контроля и исправления ошибок, например битов четности.

Пример: 8

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**континуексмитонксофф**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фтксконтинуеонксофф")
</dt> </dl>

Если **значение равно true**, передача данных продолжается, когда входной буфер поступает в пределах **ксоффксмитсрешолд** байт и драйвер передал значение **ксоффчарарктер** для прекращения получения байтов. Если **значение равно false**, передача не продолжается до тех пор, пока входной буфер не будет **ксонксмитсрешолд** байт, а драйвер передал значение **ксончарактер** , чтобы возобновить прием.

</dd> <dt>

**ктсаутфловконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фаутксктсфлов")
</dt> </dl>

Если задано **значение true**, то перед передачей данных проверяется сигнал CTS. CTS сигнализирует, что оба устройства в последовательном подключении готовы к передаче данных. Передача данных приостанавливается до тех пор, пока не будет задан сигнал CTS.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**дискарднуллбитес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| значение fNull")
</dt> </dl>

Если **значение равно true**, **пустые** байты (символы) отбрасываются при получении.

</dd> <dt>

**дсраутфловконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фаутксдсрфлов")
</dt> </dl>

Если **значение — true**, управление потоком данных включено, если имеется условие готовности набора данных (DSR). DSR сигнализирует, что подключение было установлено устройствами через последовательное подключение. Передача данных DSR приостанавливается до тех пор, пока не будет указан сигнал DSR.

</dd> <dt>

**Чувствительность DSR**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фдсрсенситивити")
</dt> </dl>

Если **значение — true**, драйвер связи чувствителен к состоянию сигнала DSR. Драйвер игнорирует все полученные байты, если входная линия коммутатора DSR не является высокой.

</dd> <dt>

**дтрфловконтролтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фдтрконтрол")
</dt> </dl>

Использование управления потоком терминала данных (DTR) после установления соединения.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Enable** ("включить")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Отключить** ("отключить")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Подтверждение** ("подтверждение")


</dt> <dd></dd> </dl>

</dd> <dt>

**Символ конца файла**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| еофчар")
</dt> </dl>

Значение символа, используемого для обозначения конца данных.

Пример: ^ Z

</dd> <dt>

**еррорреплацечарактер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| еррорчар")
</dt> </dl>

Значение символа, используемого для замены полученных байтов с ошибкой четности.

Пример: ^ C

</dd> <dt>

**еррорреплацементенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| феррорчар")
</dt> </dl>

Если **значение равно true**, байты, полученные с ошибками четности, заменяются значением **еррорреплацечарактер** . Символы с ошибками четности заменяются только в том случае, если это свойство имеет **значение true** , а проверка четности включена.

</dd> <dt>

**евентчарактер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| евтчар")
</dt> </dl>

Значение управляющего символа, который используется для сигнализации события, например конца файла.

Пример: ^ e

</dd> <dt>

**IsBusy**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| File functions \| CreateFile")
</dt> </dl>

**Значение true** показывает, что последовательный порт занят.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| оборудование \\ \\ девицемап \\ \\ сериалкомм")
</dt> </dl>

Имя последовательного порта Windows.

Пример: "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| четность")
</dt> </dl>

Метод проверки четности для использования. В качестве метода проверки ошибок используется четность, при котором каждая единица данных включает дополнительный бит четности. Затем получатель может проверить допустимость данных, подчисляя заданные биты.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** ("нет")


</dt> <dd>

Проверка четности не используется.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Нечетная** ("нечетная")


</dt> <dd>

Устанавливает бит четности так, чтобы число установленных битов всегда было нечетным.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Даже** ("даже")


</dt> <dd>

Устанавливает бит четности так, чтобы число установленных битов всегда было четным.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Пометить** ("пометить")


</dt> <dd>

Оставляет бит четности равным 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Пробел** ("пробел")


</dt> <dd>

Оставляет бит четности со значением 0 (ноль).

</dd> </dl>

</dd> <dt>

**паритичеккенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фпарити")
</dt> </dl>

Если **значение равно true**, проверка четности включена.

</dd> <dt>

**ртсфловконтролтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Управление потоком запроса на отправку (RTS). RTS используется для сигнализации того, что данные доступны для передачи.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("включить")


</dt> <dd>

Для сеанса обмена данными остается RTS.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** ("отключить")


</dt> <dd>

RTS игнорируется после получения первого сигнала RTS.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Подтверждение** ("подтверждение")


</dt> <dd>

RTS отключается, если размер буфера передачи превышает три квартала, а RTS включен, если буфер меньше единицы заполнения.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Переключатель** ("переключить")


</dt> <dd>

RTS включается при наличии данных, буферизованных для передачи.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**стопбитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| стопбитс")
</dt> </dl>

Число используемых битов. Останавливаются биты, разделяющие каждую единицу данных на асинхронном последовательном подключении. Они также отправляются постоянно, когда нет доступных данных для передачи.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1,5** ("1,5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**ксоффчарактер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксоффчар")
</dt> </dl>

Значение символа XOFF для передачи и приема. XOFF — это программный элемент управления для отключения передачи данных (в то время как RTS и CTS — аппаратные элементы управления). XON возобновляет передачу.

</dd> <dt>

**ксоффксмитсрешолд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксоффлим")
</dt> </dl>

Максимальное число байтов, разрешенное во входном буфере до отправки символа XOFF.

</dd> <dt>

**ксончарактер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксончар")
</dt> </dl>

Значение символа XON как для передачи, так и для приема. XON — это программный элемент управления для возобновления передачи данных (тогда как RTS и CTS — аппаратные элементы управления). XOFF останавливает передачу.

</dd> <dt>

**ксонксмитсрешолд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксонлим")
</dt> </dl>

Минимальное число байтов, разрешенное во входном буфере до отправки символа XON. Это свойство работает совместно с **ксоффксмитсрешолд** для регулирования скорости передачи данных.

</dd> <dt>

**ксонксоффинфловконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Финкс")
</dt> </dl>

Если задано **значение true**, во время приема используется управление потоком XON/XOFF. Если задано значение **true**, значение **ксоффчарактер** отправляется, когда входной буфер поступает в пределах **Ксоффксмитсрешолд** байт, а значение **ксончарактер** отправляется, когда входной буфер попадает в пределы **ксонксмитсрешолд** байт.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

true

</dd> </dl>

</dd> <dt>

**ксонксоффаутфловконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фауткс")
</dt> </dl>

**Ксонксоффаутфловконтрол** указывает, используется ли управление потоком XON или XOFF во время передачи. Если значение — **true**, передача прекращается при получении значения **ксоффчарактер** и начинается снова при получении значения **ксончарактер** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ сериалпортконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).

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

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
