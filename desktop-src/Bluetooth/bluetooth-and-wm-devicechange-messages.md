---
title: Сообщения Bluetooth и WM_DEVICECHANGE
description: Bluetooth включает определенные \_ сообщения WM девицечанже, которые позволяют разработчикам получать сообщения при изменении состояния устройства Bluetooth.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987597"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Сообщения Bluetooth и WM \_ девицечанже

Bluetooth включает определенные сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , которые позволяют разработчикам получать сообщения при изменении состояния устройства Bluetooth. В этом разделе описывается, как получить специальные сообщения **WM \_ Девицечанже** для Bluetooth и список сообщений, связанных с Bluetooth.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Получение сообщений девицечанже WM, относящихся к Bluetooth \_

Чтобы получать сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , необходимо сначала открыть обработчик для локального радио. Для этого используйте один из следующих методов:

-   Используйте функцию [сетупдижетклассдевс](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) со следующими параметрами: (GUID \_ бспорт \_ \_ интерфейс устройства,..., дигкф \_ Present \| дигкф \_ девицеинтерфаце), а затем используйте функции [сетупдиенумдевицеинтерфацес](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)и [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .
-   Используйте функции [**блуетусфиндфирстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**блуетусфинднекстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)и [**блуетусфиндрадиоклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

При открытии обработчика радиосигнала Bluetooth вызовите функцию [**регистердевиценотификатион**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) и зарегистрируйте для получения уведомлений об этом маркере с помощью **ДБТ \_ девтип \_ Handle** в качестве типа устройства. При регистрации отправляются следующие идентификаторы GUID, и элемент **\_ данных** [**dev \_ Broadcast \_ Handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: дбч является связанным буфером.

## <a name="bluetooth-specific-messages"></a>Сообщения, относящиеся к Bluetooth

В следующей таблице перечислены сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , относящиеся к Bluetooth.

| Код GUID                                   | BUFFER                                                  | Описание                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ Bluetooth \_ хЦи, \_ событие            | [**\_ \_ сведения о событии БС хЦи \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Это сообщение отправляется при подключении или отключении удаленного устройства Bluetooth на уровне ACL.                                                                                                                                                                                                                                                                    |
| GUID \_ Bluetooth \_ L2CAP, \_ событие          | [**\_ \_ Сведения о событии БС L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Это сообщение отправляется при установке или завершении канала L2CAP между локальным радио и удаленным устройством Bluetooth. Для каналов L2CAP, которые являются мультиплексорами, например RFCOMM, это сообщение отправляется только при установке базового канала, а не при установке или завершении каждого мультиплексированного канала, такого как канал RFCOMM. |
| GUID \_ \_ запрос ПИН-кода Bluetooth \_          | Не применяется                                         | Это сообщение должно игнорироваться приложением. Если приложение должно получать запросы на получение ПИН-кода, следует использовать функцию [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                                                                                                                   |
| GUID \_ \_ радиомодуля Bluetooth \_ в \_ диапазоне      | [**\_радио БС \_ в \_ диапазоне**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Это сообщение отправляется при изменении любого из следующих атрибутов удаленного устройства Bluetooth: обнаружено устройство, класс устройства, имя, состояние подключения или сохраненное состояние устройства. Это сообщение также отправляется, если эти атрибуты заданы или сняты.                                                                                  |
| GUID \_ \_ радиомодуля \_ Bluetooth \_ вне \_ допустимого диапазона | [**\_адрес Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Это сообщение отправляется, когда ранее обнаруженное устройство не было найдено после завершения последнего запроса. Это сообщение не будет отправлено для сохраненных устройств. Структура **\_ адреса БС** — это адрес устройства, которое не было найдено.                                                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**блуетусфиндфирстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**блуетусфинднекстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**блуетусфиндрадиоклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**регистердевиценотификатион**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[сетупдидестройдевицеинфолист](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[сетупдиенумдевицеинтерфацес](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[сетупдижетклассдевс](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**\_адрес Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**\_ \_ сведения о событии БС хЦи \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**\_ \_ Сведения о событии БС L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**\_радио БС \_ в \_ диапазоне**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**\_обработчик вещания для разработчиков \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 