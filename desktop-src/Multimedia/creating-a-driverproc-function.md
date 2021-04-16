---
title: Создание функции Дриверпрок
description: Создание функции Дриверпрок
ms.assetid: 8182d115-ba0b-43f4-a6b9-9f6a19493247
keywords:
- устанавливаемые драйверы, создание
- Создание функции Дриверпрок
- Функция Дриверпрок
- устанавливаемые драйверы, функция Дриверпрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6865d5e13425fe873e74ac77af5ae66401280e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672273"
---
# <a name="creating-a-driverproc-function"></a>Создание функции Дриверпрок

Создание функции [дриверпрок](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) во многом аналогично созданию процедуры окна. Функция состоит из оператора **switch** , и каждый вариант обрабатывает данное сообщение драйвера, возвращая значение, указывающее на успешное выполнение или сбой. Функция **дриверпрок** имеет следующую форму:


```C++
LONG DriverProc(DWORD dwDriverId, HDRVR hdrvr, UINT msg, 
    LONG lParam1, LONG lParam2)
{
    DWORD dwRes = 0L;

    switch (msg) {
    case DRV_LOAD:
    // Sent when the driver is loaded. This is always   
    // the first message received by a driver. 
        dwRes = 1L;  // returns 0L to fail
        break;

    case DRV_FREE:
    // Sent when the driver is about to be discarded.
    // This is the last message a driver receives
    // before it is freed.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_OPEN:
    // Sent when the driver is opened.
        dwRes = 1L;  // returns 0L to fail
        break;       // value subsequently used
                     // for dwDriverId.

    case DRV_CLOSE:
    // Sent when the driver is closed. Drivers are
    // unloaded when the open count reaches zero.
        dwRes = 1L;  // returns 0L to fail
        break;

    case DRV_ENABLE:
    // Sent when the driver is loaded or reloaded and
    // when Windows is enabled. Install interrupt
    // handlers and initialize hardware. Expect the
    // driver to be in memory only between the enable
    // and disable messages.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_DISABLE:
    // Sent before the driver is freed or when Windows
    // is disabled. Remove interrupt handlers and place
    // hardware in an inactive state.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_INSTALL:
    // Sent when the driver is installed.
        dwRes = DRVCNF_OK;  // Can also return 
        break;              // DRVCNF_CANCEL
                            // and DRV_RESTART

    case DRV_REMOVE:
    // Sent when the driver is removed.
        dwRes = 1L;  // return value ignored
        break;

    case DRV_QUERYCONFIGURE:
    // Sent to determine if the driver can be
    // configured.
        dwRes = 0L;  // Zero indicates configuration
        break;       // NOT supported

    case DRV_CONFIGURE:
    // Sent to display the configuration
    // dialog box for the driver.
        dwRes = DRVCNF_OK;  // Can also return
        break;              // DRVCNF_CANCEL
                            // and DRVCNF_RESTART

    default:
    // Process any other messages.
        return DefDriverProc (dwDriverId, hdrvr, 
            msg, lParam1, lParam2);

    }
    return dwRes;
}
 
```



 

 