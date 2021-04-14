---
description: Демонстрирует процесс добавления обработчика устройства на устройство.
title: Назначение обработчика устройства устройству
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985468"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Назначение обработчика устройства устройству

Демонстрирует процесс добавления обработчика устройства на устройство.

## <a name="instructions"></a>Инструкции


Чтобы назначить обработчик устройства в подразделе **Параметры устройства** экземпляра устройства, добавьте значение типа **reg \_ SZ** с именем **девицехандлерс**. Запись данных для этого значения — это имя обработчика устройства.

Ниже приведен пример записи для вымышленного устройства VID \_ 059&PID \_ 0031.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

Обработчики устройств также могут быть назначены с помощью [группы устройств](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) или параметров [класса устройств](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .

 

 



