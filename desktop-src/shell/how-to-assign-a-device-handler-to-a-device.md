---
description: Демонстрирует процесс добавления обработчика устройства на устройство.
title: Назначение обработчика устройства устройству
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092978"
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

 

 



