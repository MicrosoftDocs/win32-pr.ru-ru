---
title: Имсрдпклиентнонскриптабле Нотифиредиректдевицечанже, метод
description: сообщает модулю перенаправления устройств элемента управления удаленный рабочий стол ActiveX, что в системе произошло изменение устройства. Этот метод передает в \_ элемент управления уведомления WM девицечанже.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, метод Нотифиредиректдевицечанже
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130081"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>Метод Имсрдпклиентнонскриптабле:: Нотифиредиректдевицечанже

сообщает модулю перенаправления устройств элемента управления удаленный рабочий стол ActiveX, что в системе произошло изменение устройства. Этот метод передает в элемент управления уведомления [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Указывает событие устройства. Этот параметр может принимать одно из указанных ниже значений.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**ДБТ \_ конфигчанжеканцелед**


</dt> <dd>

Запрос на изменение текущей конфигурации (закрепления или отстыковки) отменен.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**ДБТ \_ конфигчанжед**


</dt> <dd>

Текущая конфигурация изменилась из-за закрепления или открепления.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**ДБТ \_ CUSTOMEVENT**


</dt> <dd>

Произошло пользовательское событие.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**ДБТ \_ девицеарривал**


</dt> <dd>

Устройство было вставлено и теперь доступно.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**ДБТ \_ девицекуериремове**


</dt> <dd>

Запрошено разрешение на удаление устройства. Любое приложение может отклонить этот запрос и отменить удаление.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**ДБТ \_ девицекуериремовефаилед**


</dt> <dd>

Запрос на удаление устройства отменен.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**ДБТ \_ девицеремовекомплете**


</dt> <dd>

Устройство удалено.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**ДБТ \_ девицеремовепендинг**


</dt> <dd>

Устройство будет удалено. Удаление не может быть запрещено.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**ДБТ \_ девицетипеспеЦифик**


</dt> <dd>

Произошло событие для конкретного устройства.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**ДБТ \_ девнодес \_ изменен**


</dt> <dd>

Устройство было добавлено в систему или удалено из нее.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**ДБТ \_ куеричанжеконфиг**


</dt> <dd>

Запрошено разрешение на изменение текущей конфигурации (закрепление или Отстыковка).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**ДБТ \_ пользователяопределенные**


</dt> <dd>

Значение этого сообщения определяется пользователем.

</dd> </dl> </dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на структуру, содержащую данные, относящиеся к конкретному событию. Его формат зависит от значения параметра *wParam* . Дополнительные сведения см. в документации по каждому событию. Дополнительные сведения см. в разделе [типы событий устройства](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Приложение-контейнер, которое разрешает динамическое добавление или удаление устройств, должно обрабатывать сообщение [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) в своем окне верхнего уровня и пересылать сообщение в элемент управления с помощью метода **нотифиредиректдевицечанже** . Примером динамического изменения устройства является то, что во время работы системы добавляется или удаляется перенаправленный диск.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                               |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ имсрдпклиентнонскриптабле определен как 2f079c4c-87B2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

