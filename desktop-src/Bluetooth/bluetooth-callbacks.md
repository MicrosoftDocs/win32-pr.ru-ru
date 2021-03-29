---
title: Обратные вызовы Bluetooth
description: Функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять устройствами и службами Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773649"
---
# <a name="bluetooth-callbacks"></a>Обратные вызовы Bluetooth

Функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять устройствами и службами Bluetooth.

Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows. Дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [Поддержка сокетов Windows для Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                      | Содержимое                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_обратный вызов проверки подлинности PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Используется в сочетании с функцией [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_обратный вызов проверки подлинности pfn, \_ \_ ex**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Используется в сочетании с функцией [**блуетусрегистерфораусентикатионекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**\_ \_ \_ обратный вызов атрибутов перечисления PFN Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Вызывается один раз для каждого атрибута, найденного в параметре *псдпстреам* , который передается в вызов функции [**блуетуссдпенуматтрибутес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**\_ \_ обратный вызов устройства PFN**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Используется в связи с выбором устройств Bluetooth.                                                                                                                    |



 

 

 




