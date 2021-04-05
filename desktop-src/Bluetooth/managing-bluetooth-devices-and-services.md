---
title: Управление устройствами и службами Bluetooth
description: Два основных подхода к программированию Bluetooth для программирования Windows с помощью интерфейса сокетов Windows и управления устройствами напрямую с интерфейсами Bluetooth, не поддерживающими сокеты.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Управление устройствами и службами Bluetooth
- Устройства и службы Bluetooth, управление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133931"
---
# <a name="managing-bluetooth-devices-and-services"></a>Управление устройствами и службами Bluetooth

В этом разделе описывается, как использовать API Bluetooth для непосредственного управления устройствами и службами Bluetooth.

Сведения об использовании интерфейса сокетов Windows для программирования Bluetooth в Windows см. в разделе [Поддержка Bluetooth в Windows Sockets](windows-sockets-support-for-bluetooth.md).

> [!Note]  
> Bluetooth не мешает функциям управления питанием прерывать передачу данных Bluetooth. Приложения с поддержкой Bluetooth могут отслеживать сообщения о питании, чтобы предотвратить такое прерывание. Дополнительные сведения см. [в разделе Использование функции управления питанием](/windows/desktop/Power/using-power-management).

 

Этот раздел содержит следующие подразделы.

| Section                                                                               | Содержимое                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Выбор устройства Bluetooth](selecting-a-bluetooth-device.md)                      | Описывает, как выбрать устройство Bluetooth.                                   |
| [Сообщения Bluetooth и WM \_ девицечанже](bluetooth-and-wm-devicechange-messages.md) | Объясняет взаимодействие между сообщениями Bluetooth и **WM \_ девицечанже** . |



 

 

 