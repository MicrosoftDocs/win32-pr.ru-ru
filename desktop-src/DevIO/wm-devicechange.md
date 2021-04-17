---
description: Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Сообщение WM_DEVICECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423297"
---
# <a name="wm_devicechange-message"></a>\_Сообщение ДЕВИЦЕЧАНЖЕ WM

Уведомляет приложение об изменении конфигурации оборудования устройства или компьютера.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Идентификатор **WM \_ девицечанже** .

</dd> <dt>

*wParam* 
</dt> <dd>

Произошедшее событие. Этот параметр может принимать одно из следующих значений из файла заголовка ДБТ. h.



| Значение                                                                                                                                                                                                                                                                                                  | Значение                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[ДБТ \_ КОНФИГЧАНЖЕКАНЦЕЛЕД](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | Запрос на изменение текущей конфигурации (закрепления или отстыковки) отменен.<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[ДБТ \_ КОНФИГЧАНЖЕД](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | Текущая конфигурация изменилась из-за закрепления или открепления.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[ДБТ \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | Произошло пользовательское событие.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕАРРИВАЛ](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> </dl>                                         | Устройство или носитель вставлены и теперь доступны.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕКУЕРИРЕМОВЕ](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | Запрошено разрешение на удаление устройства или фрагмента носителя. Любое приложение может отклонить этот запрос и отменить удаление.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕКУЕРИРЕМОВЕФАИЛЕД](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | Запрос на удаление устройства или носителя был отменен.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕРЕМОВЕКОМПЛЕТЕ](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | Устройство или носитель с носителем были удалены.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕРЕМОВЕПЕНДИНГ](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | Устройство или носитель будет удален. Нельзя запретить.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[ДБТ \_ ДЕВИЦЕТИПЕСПЕЦИФИК](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | Произошло событие для конкретного устройства.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[ДБТ \_ ДЕВНОДЕС \_ изменил](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Устройство было добавлено в систему или удалено из нее.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[ДБТ \_ КУЕРИЧАНЖЕКОНФИГ](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | Запрошено разрешение на изменение текущей конфигурации (закрепление или Отстыковка).<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[ДБТ \_ ПОЛЬЗОВАТЕЛЯОПРЕДЕЛЕННЫЕ](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> </dl>                                                 | Значение этого сообщения определяется пользователем.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, содержащую данные, относящиеся к конкретному событию. Его формат зависит от значения параметра *wParam* . Дополнительные сведения см. в документации по каждому событию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы предоставить запрос.

Верните **широковещательный \_ запрос \_ Deny** , чтобы отклонить запрос.

## <a name="remarks"></a>Комментарии

Для устройств, которые предлагают функции, управляемые программным обеспечением, такие как извлечение и блокировка, система обычно отправляет сообщение [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) , чтобы позволить приложениям и драйверам устройств правильно использовать устройство. Если система принудительно удаляет устройство, оно может не отправить сообщение [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) перед этим.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                                                    |
| Header<br/>                   | <dl> <dt>Winuser. h (включая Windows. h или ДБТ. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ДБТ \_ конфигчанжеканцелед](dbt-configchangecanceled.md)
</dt> <dt>

[ДБТ \_ конфигчанжед](dbt-configchanged.md)
</dt> <dt>

[ДБТ \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[ДБТ \_ девицеарривал](dbt-devicearrival.md)
</dt> <dt>

[ДБТ \_ девицекуериремове](dbt-devicequeryremove.md)
</dt> <dt>

[ДБТ \_ девицекуериремовефаилед](dbt-devicequeryremovefailed.md)
</dt> <dt>

[ДБТ \_ девицеремовекомплете](dbt-deviceremovecomplete.md)
</dt> <dt>

[ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md)
</dt> <dt>

[ДБТ \_ девицетипеспеЦифик](dbt-devicetypespecific.md)
</dt> <dt>

[ДБТ \_ девнодес \_ изменен](dbt-devnodes-changed.md)
</dt> <dt>

[ДБТ \_ куеричанжеконфиг](dbt-querychangeconfig.md)
</dt> <dt>

[ДБТ \_ пользователяопределенные](dbt-userdefined.md)
</dt> </dl>

 

