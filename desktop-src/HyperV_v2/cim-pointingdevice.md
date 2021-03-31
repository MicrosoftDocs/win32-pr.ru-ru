---
description: Представляет устройство, используемое для указания областей экрана.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Класс CIM_PointingDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156947"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a>Класс CIM_PointingDevice (Управление Hyper-V)

Представляет устройство, используемое для указания областей экрана.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ поинтингдевице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ поинтингдевице** имеет следующие свойства.

<dl> <dt>

**Правой или левой**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли указывающее устройство для работы с правой или левой рукой.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (1)


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

**Правая операция** (2)


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

**Левая операция** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**нумберофбуттонс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Указывающее устройство в DMTF \| 003,4 ")
</dt> </dl>

Число кнопок на устройстве. Если указывающее устройство не имеет кнопок, для этого параметра должно быть задано значение "0".

</dd> <dt>

**поинтингтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Указывающее устройство в DMTF \| 003,1 ")
</dt> </dl>

Тип указывающего устройства.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

**Мышь** (3)


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

**Отслеживание шарика** (4)


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

**Точка трассировки** (5)


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

**Точка глиде** (6)


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

**Сенсорная панель** (7)


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

**Сенсорный экран** (8)


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

**Оптический датчик мыши** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Решение**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("число счетчиков на дюйм"), **Пунит** ("Счетчик/дюйм")
</dt> </dl>

Разрешение отслежения указывающего устройства в счетчиках на дюйм.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_УСЕРДЕВИЦЕ CIM**](cim-userdevice.md)
</dt> </dl>

 

