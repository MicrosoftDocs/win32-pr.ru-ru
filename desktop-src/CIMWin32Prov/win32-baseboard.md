---
description: Представляет основную плату, которая также называется материнской платой или системной платой.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Класс Win32_BaseBoard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac22dc01864d74902c666529bd40344f65eacfb1ad2515552e1cd46fbf65b9e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546523"
---
# <a name="win32_baseboard-class"></a>\_Класс основной платы Win32

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ основной платы Win32** представляет основную плату, которая также называется материнской платой или системной платой.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Члены

Класс **\_ основной платы Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ основной платы Win32** содержит следующие методы.



| Метод           | Описание                 |
|:-----------------|:----------------------------|
| **Является совместимым** | Не реализован.<br/> |



 

### <a name="properties"></a>Свойства

Класс **\_ основной платы Win32** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**конфигоптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 12 \| строки параметров конфигурации")
</dt> </dl>

Массив, представляющий конфигурацию переключателей и коммутаторов, расположенных на основной плате.

Пример: "JP2: размер кэша 1-2 — 256 КБ, размер кэша 2-3 — 512 КБ, SW1-1: закрыть для отключения на платном видео"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Depth**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Глубина физического пакета в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Высота физического пакета в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**хостингбоард**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, плата является материнской платой или основной платой в корпусе.

Это свойство наследуется [**от \_ карты CIM**](cim-card.md).

</dd> <dt>

**хотсваппабле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано **значение true**, пакет может быть горячим заменой. Физический пакет может быть горячим заменой, если можно заменить элемент физически отличающимся, но эквивалентным элементом, пока содержащий его пакет применяет к нему питание, когда он включен. Например, пакет диска, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой. Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя Организации, ответственной за создание физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Модель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Имя, по которому известен физический элемент.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Захватывает дополнительные данные, помимо сведений о тегах актива, которые можно использовать для обнаружения физического элемента. Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива. Обратите внимание, что если только данные штрих-кода доступны и уникальны или могут использоваться в качестве ключа элемента, значение свойства будет **равно NULL** , а данные штрих-кода будут использоваться в качестве ключа класса в свойстве Tag.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**партнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**повередон**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** показывает, что физический элемент включен.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Продукт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 2 \| продукта")
</dt> </dl>

Номер части основной платы, определяемый производителем.

</dd> <dt>

**Службе**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если пакет является съемным. Физический пакет является съемным, если он предназначен для извлечения и выхода из физического контейнера, в котором он обычно обнаруживается без нарушения функций общей упаковки. Пакет по-прежнему может быть съемным, если необходимо отключить питание для выполнения удаления. Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой. Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей SCA. Однако последняя может также быть горячей заменой. Дисплей ноутбука не является съемным или не является избыточным источником питания. Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**Заменяемый**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если пакет является заменяемым. Физический пакет может быть заменяемым, если можно заменить (FRU или обновить) элемент физически другой. Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок. В этом случае процессор считается заменяемым. Еще один пример — это пакет источника питания, подключенный к скользящим шинам. Все съемные пакеты по сути являются заменяемыми.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**рекуирементсдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ карта CIM**](cim-card.md)".**СпеЦиалрекуирементс**")
</dt> </dl>

Произвольная строка, которая описывает способ физического уникальности этой карточки с других карточек. Свойство имеет значение только в том случае, если соответствующее свойство логического свойства **спеЦиалрекуирементс** имеет значение **true**.

Это свойство наследуется [**от \_ карты CIM**](cim-card.md).

</dd> <dt>

**рекуиресдаугхтербоард**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано **значение true**, для правильной работы требуется по крайней мере одна даугхтербоард или вспомогательная карта.

Это свойство наследуется [**от \_ карты CIM**](cim-card.md).

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Номер, выделенный изготовителем, используемый для распознавания физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Номер единицы хранения для физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**слотлайаут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, описывающая расположение слота, типичное использование, ограничения, отдельные интервалы между гнездами и другие сведения, относящиеся к слотам на карте.

Это свойство наследуется [**от \_ карты CIM**](cim-card.md).

</dd> <dt>

**спеЦиалрекуирементс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ карта CIM**](cim-card.md)".**Рекуирементсдескриптион**")
</dt> </dl>

Если **значение — true**, эта карта физически уникальна по отношению к другим картам того же типа, поэтому для нее требуется специальный слот. Например, для двойной широкой карты требуется два слота. Другим примером является то, что определенная карта может использоваться для одной и той же общей функции с другими картами, но для нее требуется специальный слот (например, очень длинный), тогда как другие карты можно разместить в любом доступном слоте. Если задано значение **true**, то соответствующее свойство, **рекуирементсдескриптион**, должно задавать природу уникальности или назначения карты.

Это свойство наследуется [**от \_ карты CIM**](cim-card.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

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

**Тег**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("тег"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Уникальный идентификатор основной платы системы.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

Пример: "Основная плата"

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Версия физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")
</dt> </dl>

Вес физического пакета в фунтах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Ширина физического пакета в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ основной платы Win32** является производным [**от \_ карты CIM**](cim-card.md) , которая является производной от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).

## <a name="examples"></a>Примеры

Образец [свойства основной платы компьютера](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) на Perl возвращает сведения о компьютерной плате.

Пример " [свойства платы компьютера](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) " в примере PowerShell возвращает сведения о компьютерной плате.

Следующий пример VBScript также возвращает сведения о компьютерной плате.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Карта CIM**](cim-card.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

