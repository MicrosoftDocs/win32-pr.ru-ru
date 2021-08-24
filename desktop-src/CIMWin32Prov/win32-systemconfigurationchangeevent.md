---
description: '&Win32 \_ системконфигуратиончанжеевент \# 8194; Класс WMI указывает, что список устройств в системе обновлен (устройство было добавлено или удалено, или изменена конфигурация).'
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Класс Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751304"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>\_Класс Win32 системконфигуратиончанжеевент

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ системконфигуратиончанжеевент для Win32** указывает, что список устройств в системе обновлен (устройство было добавлено или удалено, или изменена конфигурация). Возникает событие, и экземпляр этого класса создается при отправке сообщения "Девмгррефрешон<*ComputerName*>". Точное изменение списка устройств не содержится в сообщении, поэтому для получения текущих системных настроек требуется обновление устройства. Примеры изменений конфигурации: параметры IRQ, COM-порты и версии BIOS.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системконфигуратиончанжеевент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ системконфигуратиончанжеевент** имеет следующие свойства.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("сообщения управления Win32APIDevice \| WM \_ девицечанже \| wParam", "Win32APIDevice Управление сообщениями управления \| WM \_ сеттингчанже")
</dt> </dl>

Тип произошедшего уведомления об изменении события.

Это свойство наследуется из [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Конфигурация изменена** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Прибытие устройства** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Удаление устройства** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Закрепление** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**\_дескриптор безопасности**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие. Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md). Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное значение, указывающее время создания события. Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г. Эти сведения находятся в формате всеобщего скоординированного времени (UTC).

Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ системконфигуратиончанжеевент** является производным от [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).

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

[**\_Девицечанжеевент Win32**](win32-devicechangeevent.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
