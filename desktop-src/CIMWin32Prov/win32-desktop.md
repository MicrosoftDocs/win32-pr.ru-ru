---
description: Класс Win32 \_ десктопвми представляет общие характеристики рабочего стола пользователя. Свойства этого класса могут быть изменены пользователем для настройки рабочего стола.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Класс Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c59adebd2fdf3c0727016473e6c347be3af139d539bb007c794eb2aafb4c1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002884"
---
# <a name="win32_desktop-class"></a>\_Класс рабочего стола Win32

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) для **\_ настольных компьютеров Win32** представляет общие характеристики рабочего стола пользователя. Свойства этого класса могут быть изменены пользователем для настройки рабочего стола.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Члены

Класс **\_ рабочего стола Win32** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ рабочего стола Win32** имеет следующие свойства.

<dl> <dt>

**BorderWidth**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| BorderWidth ")
</dt> </dl>

Ширина границ вокруг всех окон с изменяемыми границами.

Пример: 3

</dd> <dt>

**Caption**
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

**кулсвитч**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| кулсвитч")
</dt> </dl>

Включено быстрое переключение задач. Быстрое переключение задач позволяет пользователю переключаться между окнами с помощью сочетания клавиш **ALT + TAB** .

</dd> <dt>

**курсорблинкрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| курсорблинкрате"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")
</dt> </dl>

Промежуток времени между мигающими последовательными курсорами.

Пример: 530

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

**драгфуллвиндовс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| драгфуллвиндовс")
</dt> </dl>

Содержимое окна отображается, когда пользователь перемещает окно.

</dd> <dt>

**гридгрануларити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| гридгрануларити"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 пикселей")
</dt> </dl>

Пространство сетки, к которой привязаны окна на рабочем столе. Это упрощает организацию окон. Как правило, отступы достаточно точно, чтобы пользователь не заметит его.

Пример: 1

</dd> <dt>

**иконспаЦинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконспаЦинг "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")
</dt> </dl>

Интервал между значками.

Пример: 75

</dd> <dt>

**иконтитлефаценаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконфонт ")
</dt> </dl>

Шрифт, используемый для имен значков.

Пример: "MS San Serif"

</dd> <dt>

**иконтитлесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**Логфонтв**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| лфхеигхт"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")
</dt> </dl>

Размер шрифта значка.

Пример: 9

</dd> <dt>

**иконтитлеврап**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконтитлеврап ")
</dt> </dl>

Текст заголовка значка переносится на следующую строку.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Имя, идентифицирующее текущий профиль рабочего стола.

Пример: "Маинпроф"

</dd> <dt>

**Шаблон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Шаблон рабочего стола панели управления по умолчанию \\ \\ \| ")
</dt> </dl>

Имя шаблона, используемого в качестве фона для рабочего стола.

</dd> <dt>

**скринсаверактиве**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсавеактиве ")
</dt> </dl>

Экранная заставка активна.

</dd> <dt>

**скринсаверексекутабле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Панель управления \\ \\SCRNSAVE.EXE рабочего стола по умолчанию \| ")
</dt> </dl>

Имя текущего исполняемого файла экранной заставки.

Пример: "LOGON. SCR

</dd> <dt>

**скринсаверсекуре**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсавериссекуре ")
</dt> </dl>

Пароль включен для экранной заставки.

</dd> <dt>

**скринсавертимеаут**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсаветимеаут "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" секунды ")
</dt> </dl>

Период времени, прошедший до запуска заставки экрана.

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

**Фоновый рисунок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Рисунок рабочего стола панели управления по умолчанию \\ \\ \| ")
</dt> </dl>

Имя файла для фона рабочего стола в фоновом режиме.

Пример: "WINNT.BMP"

</dd> <dt>

**валлпаперстретчед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| валлпаперстиле ")
</dt> </dl>

Фоновый рисунок растягивается для заполнения всего экрана. Microsoft Plus! необходимо установить, прежде чем этот параметр станет доступен. Если задано **значение false**, фоновый рисунок оставляет свои исходные размеры на рабочем столе.

</dd> <dt>

**валлпапертилед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| тилеваллпапер ")
</dt> </dl>

Фоновый рисунок накладывается или выравнивается по центру.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ рабочего стола Win32** является производным [**от \_ параметра CIM**](cim-setting.md).

вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ NAME** на компьютере, где размещается реестр. Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию. Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить сведения о рабочем столе.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



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
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

