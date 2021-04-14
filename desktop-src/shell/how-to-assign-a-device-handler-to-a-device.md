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
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="e9dbd-103">Назначение обработчика устройства устройству</span><span class="sxs-lookup"><span data-stu-id="e9dbd-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="e9dbd-104">Демонстрирует процесс добавления обработчика устройства на устройство.</span><span class="sxs-lookup"><span data-stu-id="e9dbd-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="e9dbd-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e9dbd-105">Instructions</span></span>


<span data-ttu-id="e9dbd-106">Чтобы назначить обработчик устройства в подразделе **Параметры устройства** экземпляра устройства, добавьте значение типа **reg \_ SZ** с именем **девицехандлерс**.</span><span class="sxs-lookup"><span data-stu-id="e9dbd-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="e9dbd-107">Запись данных для этого значения — это имя обработчика устройства.</span><span class="sxs-lookup"><span data-stu-id="e9dbd-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="e9dbd-108">Ниже приведен пример записи для вымышленного устройства VID \_ 059&PID \_ 0031.</span><span class="sxs-lookup"><span data-stu-id="e9dbd-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

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

<span data-ttu-id="e9dbd-109">Обработчики устройств также могут быть назначены с помощью [группы устройств](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) или параметров [класса устройств](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e9dbd-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



