---
title: Bluetooth Сотрудник
description: в этом разделе приводятся определения структур, используемых для управления Bluetooth устройствами и службами.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, ссылки, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588284"
---
# <a name="bluetooth-structures"></a>Bluetooth Сотрудник

в этом разделе приводятся определения структур, используемых для управления Bluetooth устройствами и службами.

Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows. дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [поддержка Windows сокетов для Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                       | Содержимое                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_адрес Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | содержит адрес устройства Bluetooth.                                                                                      |
| [**\_ \_ Параметры обратного вызова проверки подлинности Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | содержит конкретные сведения о конфигурации устройства Bluetooth, отвечающего на запрос проверки подлинности.                  |
| [**\_ответ проверки подлинности Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Содержит сведения, передаваемые в ответ на \_ событие БС Remote \_ Authenticate \_ request.                                           |
| [**\_пары платежей \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | обеспечивает спецификацию и получение сведений о Bluetooth класса данных устройства (наложенного на устройство).                                         |
| [**\_ \_ сведения об устройстве Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | предоставляет сведения об устройстве Bluetooth.                                                                                   |
| [**\_ \_ Параметры поиска устройств \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | задает условия поиска для Bluetooth поиска устройств.                                                                         |
| [**\_ \_ Параметры Радио поиска по Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | упрощает перечисление установленных Bluetooth радио.                                                                       |
| [**\_ \_ сведения о локальной службе Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | содержит сведения о локальной службе для Bluetooth радио.                                                                        |
| [**\_ \_ сведения о числовом СРАВНЕНии Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Содержит числовое значение, используемое для проверки подлинности с помощью числового сравнения.                                                       |
| [**\_ \_ сведения о данных OOB по Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Содержит данные, используемые для проверки подлинности перед установкой связывания устройств по внешнему каналу.                                          |
| [**\_сведения о ключе доступа Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Содержит ключ доступа, используемый для проверки подлинности через ключ доступа.                                                                        |
| [**\_сведения о ПИН-коде Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Содержит сведения, используемые для проверки подлинности с помощью ПИН-кода.                                                                            |
| [**\_сведения о радиомодуле Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | содержит сведения о Bluetooth радио.                                                                                    |
| [**\_Выбор \_ параметров устройства \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | облегчает и управляет видимостью, проверкой подлинности и выбором Bluetooth устройств и служб.                         |
| [**\_ \_ сведения об устройстве БС**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | хранит сведения об устройстве Bluetooth.                                                                                     |
| [**\_ \_ сведения о событии БС хЦи \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Используется в связи с получением \_ сообщений WM девицечанже для Bluetooth.                                                       |
| [**\_ \_ Сведения о событии БС L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Содержит данные о событиях, связанных с каналом L2CAP.                                                        |
| [**БС \_ запрос \_ устройства**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | используется при запросе на присутствие устройства Bluetooth.                                                                       |
| [**\_служба запросов \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | используется для запроса службы Bluetooth.                                                                                               |
| [**\_радио БС \_ в \_ диапазоне**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | хранит данные об устройствах Bluetooth, находящихся в пределах диапазона обмена данными.                                                     |
| [**\_Служба настройки \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | предоставляет сведения о службе для указанной службы Bluetooth.                                                                |
| [**\_данные элемента \_ SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Сохраняет данные элемента SDP.                                                                                                         |
| [**\_ \_ данные типа строки \_ SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Хранит сведения о типах строк SDP.                                                                                       |
| [**сдпаттрибутеранже**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | используется в Bluetooth запросе для ограничения набора атрибутов, возвращаемых в запросе.                                             |
| [**сдпкуерюуид**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Облегчает поиск UUID.                                                                                                 |
| [**сдпкуерюуидунион**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Содержит идентификатор UUID, на котором выполняется запрос SDP. Используется в сочетании со структурой [**сдпкуерюуид**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) . |
| [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | используется в сочетании с операциями сокета Bluetooth в соответствии с определением \_ семейства адресов AF бс.                                   |



 

 

 




