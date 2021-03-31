---
title: Класс SystemRestore
description: Предоставляет методы для отключения и включения мониторинга, перечисления доступных точек восстановления и инициации восстановления в локальной системе.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Восстановление системы класса SystemRestore
- Восстановление системы класса SystemRestore, описание
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071747"
---
# <a name="systemrestore-class"></a>Класс SystemRestore

Предоставляет методы для отключения и включения мониторинга, перечисления доступных точек восстановления и инициации восстановления в локальной системе.

## <a name="syntax"></a>Синтаксис

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Члены

Класс **SystemRestore** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **SystemRestore** содержит следующие методы.



| Метод                                                             | Описание                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**креатересторепоинт**](createrestorepoint-systemrestore.md)     | Создает точку восстановления.<br/>                         |
| [**Отключить**](disable-systemrestore.md)                           | Отключает мониторинг на определенном диске.<br/>       |
| [**Включить**](enable-systemrestore.md)                             | Включает наблюдение на определенном диске.<br/>        |
| [**жетластресторестатус**](getlastrestorestatus-systemrestore.md) | Возвращает состояние последнего восстановления системы.<br/> |
| [**Восстановлен**](restore-systemrestore.md)                           | Инициирует восстановление системы.<br/>                      |



 

### <a name="properties"></a>Свойства

Класс **SystemRestore** имеет следующие свойства.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Время, когда произошло изменение состояния.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Отображаемое описание, чтобы пользователь мог легко найти точку восстановления. Максимальная длина строки ANSI — MAX \_ DESC. Максимальная длина строки Юникода — MAX \_ DESC \_ W. Дополнительные сведения см. в разделе [текст описания точки восстановления](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Тип события. Этот элемент может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Начало \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>102</dt> </dl> | Начато изменение системы. Последующий вложенный вызов не создает новую точку восстановления. <br/> Последующие вызовы должны использовать КОНЕЧные \_ вложенные \_ \_ изменения системы, а не конечные \_ \_ изменения системы.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Начало \_ \_Изменение системы**</dt> <dt>100</dt> </dl>                       | Начато изменение системы.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Конец \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>103</dt> </dl>       | Изменение системы завершено.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Конец \_ \_Изменение системы**</dt> <dt>101</dt> </dl>                             | Изменение системы завершено.<br/>                                                                                                                                                           |



 

</dd> <dt>

**ресторепоинттипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Тип точки восстановления. Этот элемент может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                          | Значение                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Приложение \_ УСТАНОВИТЬ**</dt> <dt>0</dt> </dl>         | Приложение установлено.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Приложение \_ Удаление**</dt> <dt>1</dt> </dl>   | Удалено приложение.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Отменено \_ Операция**</dt> <dt>13</dt> </dl>        | Приложению необходимо удалить созданную точку восстановления. Например, приложение будет использовать этот флаг, когда пользователь отменит установку. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Устройство \_ \_Установка драйвера**</dt> <dt>10</dt> </dl> | Установлен драйвер устройства.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Изменение \_ Параметры**</dt> <dt>12</dt> </dl>                    | В приложении были добавлены или удалены компоненты.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Порядковый номер точки восстановления.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Список точек восстановления можно получить с помощью метода [**SwbemServices. инстанцесоф**](/windows/desktop/WmiSdk/swbemservices-instancesof) , чтобы получить коллекцию объектов **SystemRestore** . Для указания точки восстановления можно использовать свойства класса.

## <a name="examples"></a>Примеры

Следующий пример скрипта перечисляет текущие точки восстановления.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                         |
| Пространство имен<br/>                | Корневой каталог \\ по умолчанию<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Инструментарий управления Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

