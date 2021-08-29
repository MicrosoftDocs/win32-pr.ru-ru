---
title: Bluetooth Обратные вызовы
description: функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять Bluetooth устройствами и службами.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588364"
---
# <a name="bluetooth-callbacks"></a>Bluetooth Обратные вызовы

функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять Bluetooth устройствами и службами.

Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows. дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [поддержка Windows сокетов для Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                      | Содержимое                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_обратный вызов проверки подлинности PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Используется в сочетании с функцией [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_обратный вызов проверки подлинности pfn, \_ \_ ex**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Используется в сочетании с функцией [**блуетусрегистерфораусентикатионекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**\_ \_ \_ обратный вызов атрибутов перечисления PFN Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Вызывается один раз для каждого атрибута, найденного в параметре *псдпстреам* , который передается в вызов функции [**блуетуссдпенуматтрибутес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**\_ \_ обратный вызов устройства PFN**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | используется в связи с выбором устройств Bluetooth.                                                                                                                    |



 

 

 




