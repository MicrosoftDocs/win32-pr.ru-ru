---
description: Класс CIM \_ видеоконтроллерресолутион представляет различные видеорежимы, которые может поддерживать контроллер видео.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Класс CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af943df981ca2043e83dfcdd3daade0a1c13b63222a163d7e6ecf1d6110396e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420381"
---
# <a name="cim_videocontrollerresolution-class"></a>\_Класс CIM видеоконтроллерресолутион

Класс **CIM \_ видеоконтроллерресолутион** представляет различные видеорежимы, которые может поддерживать контроллер видео. Видеорежимы определяются с помощью возможных горизонтальных и вертикальных разрешений, частоты обновления, режима сканирования и количества параметров цвета, поддерживаемых контроллером. Фактически используемые разрешения — это значения, указанные в объекте [**CIM \_ Видеоконтроллер**](cim-videocontroller.md) .

оборудование, несовместимое с Windows модели драйвера (WDDM), возвращает неточные значения свойств для экземпляров этого класса.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ видеоконтроллерресолутион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ видеоконтроллерресолутион** имеет следующие свойства.

<dl> <dt>

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

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Курренсоризонталресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")
</dt> </dl>

Разрешение по горизонтали в пикселях.

</dd> <dt>

**максрефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Максрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")
</dt> </dl>

Максимальная частота обновления, если для указанных разрешений поддерживается диапазон частот (в герцах).

</dd> <dt>

**минрефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Минрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")
</dt> </dl>

Минимальная частота обновления, если для указанных разрешений поддерживается диапазон частот (в герцах).

</dd> <dt>

**нумберофколорс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентнумберофколорс**")
</dt> </dl>

Число цветов, поддерживаемое при текущем разрешении.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**рефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")
</dt> </dl>

Частота обновления в герцах. Если поддерживается диапазон ставок, используйте свойства **минрефрешрате** и **максрефрешрате** и присвойте этому свойству значение 0.

</dd> <dt>

**сканмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентсканмоде**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,5 ")
</dt> </dl>

Режим сканирования, в котором работает контроллер.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Операция без чередования** (4)


</dt> <dd>

Нечересстрочнуюющая операция

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Операция чередования** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("свойство settingid"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Идентификатор, который служит частью ключа для текущего экземпляра.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентвертикалресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")
</dt> </dl>

Разрешение контроллера по вертикали (в пикселях).

</dd> </dl>

## <a name="remarks"></a>Remarks

WMI реализует класс **CIM \_ видеоконтроллерресолутион** . Класс **CIM \_ видеоконтроллерресолутион** является динамическим классом.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

Обратите внимание, что этот класс является базовым классом. Если вы пытаетесь получить доступ к видеоконтроллеру с помощью инструментария WMI, вместо этого может потребоваться использовать [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md) .

## <a name="requirements"></a>Requirements (Требования)



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
</dt> </dl>

 

