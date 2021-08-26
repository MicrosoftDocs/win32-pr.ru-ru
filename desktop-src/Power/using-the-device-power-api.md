---
description: Используйте элементы программирования питания устройства для управления способом выполнения устройств, когда система находится в спящем режиме.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Использование API питания устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aff8239c1cd0ffc8d5e8abaf0133a9ca42bb3a01a5b6fc2acef7850929a8484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032774"
---
# <a name="using-the-device-power-api"></a>Использование API питания устройства

Используйте элементы программирования питания устройства для управления способом выполнения устройств, когда система находится в спящем режиме.

## <a name="opening-and-closing-the-device-list"></a>Открытие и закрытие списка устройств

Открытие и закрытие списка устройств — это дорогостоящий процесс с точки зрения времени ЦП. Функции [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) и [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) необходимы, только если приложению требуется несколько раз запрашивать список устройств.

Если вызывается [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) , [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) должен вызываться при завершении запросов в виде списка устройств. [**Девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) и [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) не закрывают список устройств, если он был явно открыт **девицеповеропен**.

## <a name="enumerating-devices"></a>Перечисление устройств

Функция [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) определяет, открыт ли список устройств, и, если нет, открывает его. **Девицеповеренумдевицес** перечисляет устройства на основе указанных условий поиска. Если список устройств был открыт функцией, он закрывается перед возвратом функции.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Включение и отключение устройства от пробуждения системы

Функция [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , аналогичная [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), определяет, открыт ли список устройств, и, если нет, открывает его. Затем **девицеповерсетдевицестате** задает указанные критерии для указанного устройства. Если список устройств был открыт функцией, он закрывается перед возвратом функции.

## <a name="example-code"></a>Пример кода

В следующем примере демонстрируется использование API питания устройства.


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



В этом примере список устройств открывается один раз и закрывается один раз. Если функции [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) и [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) не были вызваны, список устройств был бы открыт и закрыт каждым вызовом в [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) и [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate). С помощью **девицеповеропен** и **девицеповерклосе** мы сохранили открытие списка устройств в два ненужных времени.

 

 



