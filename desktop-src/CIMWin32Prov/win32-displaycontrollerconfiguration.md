---
description: '\_Класс WMI дисплайконтроллерконфигуратион для Win32 представляет сведения о конфигурации видеоадаптера компьютерной системы под Windows.'
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Класс Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142280"
---
# <a name="win32_displaycontrollerconfiguration-class"></a>\_Класс Win32 дисплайконтроллерконфигуратион

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дисплайконтроллерконфигуратион для Win32** представляет сведения о конфигурации видеоадаптера компьютерной системы под Windows.

Этот класс устарел. Вместо этого класса следует использовать свойства в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)и [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ дисплайконтроллерконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ дисплайконтроллерконфигуратион** имеет следующие свойства.

<dl> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| битспиксел")
</dt> </dl>

Число битов, используемых для представления цвета в данной конфигурации, или биты в каждом пикселе.

Пример: 8

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
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

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| плоскости")
</dt> </dl>

Текущее число цветовых плоскостей, используемых в конфигурации экрана. Цветовая плоскость — это еще один способ представления цветов пикселей. Вместо того чтобы назначать одному значению RGB каждому пикселю, цветовые плоскости разделяют изображение на каждый из основных компонентов цвета (красный, зеленый, синий) и сохраняют их на собственных плоскостях. Это обеспечивает более высокую глубину цвета в 8-и 16-разрядных видеосистемах. Представленные графические системы имеют битвидс, достаточный для хранения информации о глубине цвета. Это означает, что требуется только одна цветовая плоскость.

Пример: 1

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

**девицеентриесинаколортабле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумколорс")
</dt> </dl>

Количество цветовых индексов в таблице цветов устройства дисплея (если для устройства задана глубина цвета не более 8 бит на пиксель). Для устройств с более высокой глубиной цвета возвращается-1.

Пример: 256

</dd> <dt>

**девицеспеЦификпенс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумпенс")
</dt> </dl>

Текущее число перьев, зависящих от устройства. Значение 0xFFFFFFFF означает, что устройство не поддерживает перья. Перья — это логические свойства, которые могут быть назначены контроллером экрана для отображения устройств и используются для рисования линий, границ многоугольников и текста.

Пример: 3

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| хорзрес"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей")
</dt> </dl>

Текущее число пикселей в горизонтальном направлении (ось x) дисплея.

Пример: 1024

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Имя адаптера, используемого в этой конфигурации.

</dd> <dt>

**рефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| хорзресврефреш"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц")
</dt> </dl>

Частота обновления видеоадаптера. Значение 0 (ноль) или 1 (одно) указывает, что используется ставка по умолчанию. Значение-1 указывает, что используется оптимальная скорость.

Пример: 72

</dd> <dt>

**ресерведсистемпалеттинтриес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумресервед")
</dt> </dl>

Текущее число записей цветовых индексов, зарезервированных для использования системой. Это значение допустимо только для параметров экрана, использующих индексированную палитру. Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель. Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.

Пример: 20

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
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

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумресервед")
</dt> </dl>

Текущее число записей цветовых индексов, зарезервированных для использования системой. Это значение допустимо только для параметров экрана, использующих индексированную палитру. Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель. Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.

Пример: 20

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| вертрес"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей")
</dt> </dl>

Текущее число пикселей в вертикальном направлении (ось y) дисплея.

Пример: 768

</dd> <dt>

**видеомоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Понятное для пользователя описание текущего разрешения экрана и настройки цвета экрана.

Пример: "1024 768 с 256 Colors"

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ дисплайконтроллерконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).

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

 

