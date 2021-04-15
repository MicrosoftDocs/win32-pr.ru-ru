---
description: Используйте элементы программирования питания устройства для управления способом выполнения устройств, когда система находится в спящем режиме.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Использование API питания устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545490"
---
# <a name="using-the-device-power-api"></a><span data-ttu-id="7edaa-103">Использование API питания устройства</span><span class="sxs-lookup"><span data-stu-id="7edaa-103">Using the Device Power API</span></span>

<span data-ttu-id="7edaa-104">Используйте элементы программирования питания устройства для управления способом выполнения устройств, когда система находится в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="7edaa-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="7edaa-105">Открытие и закрытие списка устройств</span><span class="sxs-lookup"><span data-stu-id="7edaa-105">Opening and closing the device list</span></span>

<span data-ttu-id="7edaa-106">Открытие и закрытие списка устройств — это дорогостоящий процесс с точки зрения времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="7edaa-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="7edaa-107">Функции [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) и [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) необходимы, только если приложению требуется несколько раз запрашивать список устройств.</span><span class="sxs-lookup"><span data-stu-id="7edaa-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="7edaa-108">Если вызывается [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) , [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) должен вызываться при завершении запросов в виде списка устройств.</span><span class="sxs-lookup"><span data-stu-id="7edaa-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="7edaa-109">[**Девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) и [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) не закрывают список устройств, если он был явно открыт **девицеповеропен**.</span><span class="sxs-lookup"><span data-stu-id="7edaa-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="7edaa-110">Перечисление устройств</span><span class="sxs-lookup"><span data-stu-id="7edaa-110">Enumerating devices</span></span>

<span data-ttu-id="7edaa-111">Функция [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) определяет, открыт ли список устройств, и, если нет, открывает его.</span><span class="sxs-lookup"><span data-stu-id="7edaa-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="7edaa-112">**Девицеповеренумдевицес** перечисляет устройства на основе указанных условий поиска.</span><span class="sxs-lookup"><span data-stu-id="7edaa-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="7edaa-113">Если список устройств был открыт функцией, он закрывается перед возвратом функции.</span><span class="sxs-lookup"><span data-stu-id="7edaa-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="7edaa-114">Включение и отключение устройства от пробуждения системы</span><span class="sxs-lookup"><span data-stu-id="7edaa-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="7edaa-115">Функция [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , аналогичная [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), определяет, открыт ли список устройств, и, если нет, открывает его.</span><span class="sxs-lookup"><span data-stu-id="7edaa-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="7edaa-116">Затем **девицеповерсетдевицестате** задает указанные критерии для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="7edaa-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="7edaa-117">Если список устройств был открыт функцией, он закрывается перед возвратом функции.</span><span class="sxs-lookup"><span data-stu-id="7edaa-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="7edaa-118">Пример кода</span><span class="sxs-lookup"><span data-stu-id="7edaa-118">Example Code</span></span>

<span data-ttu-id="7edaa-119">В следующем примере демонстрируется использование API питания устройства.</span><span class="sxs-lookup"><span data-stu-id="7edaa-119">The following example demonstrates the use of the Device Power API.</span></span>


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



<span data-ttu-id="7edaa-120">В этом примере список устройств открывается один раз и закрывается один раз.</span><span class="sxs-lookup"><span data-stu-id="7edaa-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="7edaa-121">Если функции [**девицеповеропен**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) и [**девицеповерклосе**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) не были вызваны, список устройств был бы открыт и закрыт каждым вызовом в [**девицеповеренумдевицес**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) и [**девицеповерсетдевицестате**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span><span class="sxs-lookup"><span data-stu-id="7edaa-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="7edaa-122">С помощью **девицеповеропен** и **девицеповерклосе** мы сохранили открытие списка устройств в два ненужных времени.</span><span class="sxs-lookup"><span data-stu-id="7edaa-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



