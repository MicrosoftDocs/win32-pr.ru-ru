---
description: Класс Win32 \_ видеоконфигуратион неактивен. Он не будет возвращать экземпляры, так как поставщик не имеет резервной копии.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Класс Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d951a8927458fa12398682ce63963dd71949d70e4db3a426dfc93ad14c78bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922624"
---
# <a name="win32_videoconfiguration-class"></a>\_Класс Win32 видеоконфигуратион

Класс **Win32 \_ видеоконфигуратион** неактивен. Он не будет возвращать экземпляры, так как поставщик не имеет резервной копии.

Класс **Win32 \_ видеоконфигуратион** представляет конфигурацию подсистемы видео. Этот класс является устаревшим в пользу свойств, содержащихся в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)и [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ видеоконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ видеоконфигуратион** имеет следующие свойства.

<dl> <dt>

**актуалколорресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| колоррес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("бит на пиксель")
</dt> </dl>

Указывает текущую глубину цвета для экрана видео.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**адаптерчиптипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| чиптипе")
</dt> </dl>

Содержит имя микросхемы адаптера.

Пример: S3

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**адаптеркомпатибилити**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Указывает имя производителя адаптера. Это имя можно использовать для сравнения совместимости этого устройства с потребностями компьютерной системы.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**адаптердактипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| DACType")
</dt> </dl>

Указывает имя микросхемы с цифровым подключением (DAC), используемой в адаптере.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**адаптердескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Содержит описание или описательное имя видеоадаптера.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**адаптеррам**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| видеомемори"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Указывает объем памяти видеоадаптера.

Пример: 16777216

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| система описания оборудования Win32Registry \\ \\ \\ \\ \\ \\ дисплайконтроллер \\ \\ 0 \\ \\ идентификатор")
</dt> </dl>

Указывает тип видеоадаптера.

Кодировка: буквенно-цифровой

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| битспиксел")
</dt> </dl>

Указывает фактическое число битов на пиксель, представляющих дисплей. Оно может масштабироваться до текущего параметра видео (представленного свойством Актуалколорресолутион) пользователя.

Пример: 8

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**Caption**
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

**колорпланес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| плоскости")
</dt> </dl>

Указывает текущее число цветовых плоскостей, используемых в видеомониторе. Цветовая панель — это еще один способ представления цветов пикселей. Вместо того чтобы назначать одному значению RGB каждому пикселю, цветовые плоскости разделяют изображение на каждый из основных компонентов цвета (красный зеленый цвет) и сохраняют их на собственных плоскостях. Это обеспечивает более высокую глубину цвета в 8 и 16 разрядных видеосистемах. Представленные графические системы имеют битвидс, достаточный для хранения информации о глубине цвета, что делает обязательным только одну цветовую плоскость.

Пример: 1

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**колортаблинтриес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| нумколорс")
</dt> </dl>

Указывает количество цветовых индексов в таблице цветов для экрана видео. Это свойство используется, если цветовая глубина устройства не превышает 8 бит на пиксель. Для устройств с более высокой глубиной цвета возвращается-1.

Пример: 256

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

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

**девицеспеЦификпенс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| нумпенс")
</dt> </dl>

Указывает текущее число перьев конкретного устройства. Значение 0xFFFFFFFF означает, что устройство не поддерживает перья. Перья используются для рисования линий и себордерс объектов многоугольников.

Пример: 3

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**дривердате**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ класса \\ \\ адаптердескриптион \| дривердате")
</dt> </dl>

Указывает дату и время установки текущего видеодрайвера.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| хорзрес")
</dt> </dl>

Указывает текущее количество пикселей в горизонтальном направлении (на оси X) дисплея.

Пример: 1024

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**инффиленаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \| инфпас")
</dt> </dl>

Указывает путь к INF-файлу видеодрайвера.

пример: C: \\ \\ драйверы Windows System32 \\

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**инфсектион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \| инфсектион")
</dt> </dl>

Указывает раздел INF-файла, в котором находится информация о видео Win32.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**инсталледдисплайдриверс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ дефауле \| drv")
</dt> </dl>

Указывает имя установленного видеодрайвера.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**монитормануфактурер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Указывает имя изготовителя устройства дисплея.

Пример: NEC

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**Тип монитора "**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| система описания оборудования Win32Registry \\ \\ \\ \\ \\ \\ мониторпериферал \\ \\ 0 \| идентификатор")
</dt> </dl>

Указывает имя модели устройства вывода.

Пример: NEC 5FGp

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Содержит идентифицирующее имя для класса конфигурации видео.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**пикселсперкслогикалинч**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| логпикселскс")
</dt> </dl>

Указывает число пикселов на логический дюйм по оси X (горизонтальное направление) дисплея.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**пикселсперилогикалинч**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| логпикселси")
</dt> </dl>

Указывает число пикселей на логический дюйм по оси Y (вертикальное направление) дисплея.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**рефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| врефреш")
</dt> </dl>

Указывает частоту обновления конфигурации видео. Значение 0 или 1 указывает, что используется ставка по умолчанию.

Пример: 72

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**сканмоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| дефаултсеттингс. Чересстрочная развертка")
</dt> </dl>

Указывает, является ли устройство вывода чередованием.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Без чередования** ("без чередования")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

С **чередованием** (чередование)


</dt> <dd></dd> </dl>

</dd> <dt>

**скринхеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| вертсизе"), [**единицы измерения**](../wmisdk/standard-qualifiers.md) ("миллиметры")
</dt> </dl>

Задает высоту физического экрана.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**скринвидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| хорзсизе"), [**единицы измерения**](../wmisdk/standard-qualifiers.md) ("миллиметры")
</dt> </dl>

Задает ширину физического экрана.

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

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

**системпалеттинтриес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| сизепалетте")
</dt> </dl>

Реализовано текущее количество записей цветовых индексов, зарезервированных для использования системой. Это значение допустимо только для параметров экрана, использующих индексированную палитру. Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель. Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.

Пример: 20

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| вертрес")
</dt> </dl>

Указывает текущее количество пикселей в вертикальном направлении (ось Y) дисплея.

Пример: 768

Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> </dl>

 

 
