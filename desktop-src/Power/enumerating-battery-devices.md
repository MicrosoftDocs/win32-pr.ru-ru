---
description: Чтобы перечислить устройства батареи на локальном компьютере, используйте функцию Сетупдижетклассдевс.
ms.assetid: 17e3c779-91ba-4901-9435-b73dedbf0b89
title: Перечисление устройств с батареей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d610feda8fd312bbefe2742da50d82a664a8ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663124"
---
# <a name="enumerating-battery-devices"></a><span data-ttu-id="5b759-103">Перечисление устройств с батареей</span><span class="sxs-lookup"><span data-stu-id="5b759-103">Enumerating Battery Devices</span></span>

<span data-ttu-id="5b759-104">Чтобы перечислить устройства батареи на локальном компьютере, используйте функцию [сетупдижетклассдевс](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) .</span><span class="sxs-lookup"><span data-stu-id="5b759-104">To enumerate the battery devices on a local computer, use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function.</span></span> <span data-ttu-id="5b759-105">Параметр *классгуид* — это указатель на **GUID \_ девкласс \_ аккумулятора** (определенный в баткласс. h).</span><span class="sxs-lookup"><span data-stu-id="5b759-105">The *ClassGuid* parameter is a pointer to **GUID\_DEVCLASS\_BATTERY** (defined in BatClass.h).</span></span> <span data-ttu-id="5b759-106">Чтобы перечислить все батареи, установите для параметра *перечислителя* **значение NULL** и установите параметр *flags* в **дигкф \_ Present** \| **дигкф \_ интерфацедевице**.</span><span class="sxs-lookup"><span data-stu-id="5b759-106">To enumerate all of the batteries, set the *Enumerator* parameter to **NULL** and set the *Flags* parameter to **DIGCF\_PRESENT** \| **DIGCF\_INTERFACEDEVICE**.</span></span> <span data-ttu-id="5b759-107">Чтобы получить имена устройств с батареей, используйте функции [сетупдиенумдевицеинтерфацес](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces) и [сетупдижетдевицеинтерфацедетаил](https://msdn.microsoft.com/library/ms792901.aspx) для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="5b759-107">To obtain the names of the battery devices, use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces) and [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx) functions on the data returned.</span></span> <span data-ttu-id="5b759-108">Чтобы открыть маркер файла для каждого устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) с этими именами.</span><span class="sxs-lookup"><span data-stu-id="5b759-108">To open a file handle for each of the battery devices, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function with these names.</span></span>

<span data-ttu-id="5b759-109">В следующем примере C++ показано, как перечислить устройства аккумулятора на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5b759-109">The following C++ example shows how to enumerate battery devices on a local computer.</span></span>


```C++
DWORD GetBatteryState()
 {
#define GBS_HASBATTERY 0x1
#define GBS_ONBATTERY  0x2
  // Returned value includes GBS_HASBATTERY if the system has a 
  // non-UPS battery, and GBS_ONBATTERY if the system is running on 
  // a battery.
  //
  // dwResult & GBS_ONBATTERY means we have not yet found AC power.
  // dwResult & GBS_HASBATTERY means we have found a non-UPS battery.

  DWORD dwResult = GBS_ONBATTERY;

  // IOCTL_BATTERY_QUERY_INFORMATION,
  // enumerate the batteries and ask each one for information.

  HDEVINFO hdev =
            SetupDiGetClassDevs(&GUID_DEVCLASS_BATTERY, 
                                0, 
                                0, 
                                DIGCF_PRESENT | DIGCF_DEVICEINTERFACE);
  if (INVALID_HANDLE_VALUE != hdev)
   {
    // Limit search to 100 batteries max
    for (int idev = 0; idev < 100; idev++)
     {
      SP_DEVICE_INTERFACE_DATA did = {0};
      did.cbSize = sizeof(did);

      if (SetupDiEnumDeviceInterfaces(hdev,
                                      0,
                                      &GUID_DEVCLASS_BATTERY,
                                      idev,
                                      &did))
       {
        DWORD cbRequired = 0;

        SetupDiGetDeviceInterfaceDetail(hdev,
                                        &did,
                                        0,
                                        0,
                                        &cbRequired,
                                        0);
        if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
         {
          PSP_DEVICE_INTERFACE_DETAIL_DATA pdidd =
            (PSP_DEVICE_INTERFACE_DETAIL_DATA)LocalAlloc(LPTR,
                                                         cbRequired);
          if (pdidd)
           {
            pdidd->cbSize = sizeof(*pdidd);
            if (SetupDiGetDeviceInterfaceDetail(hdev,
                                                &did,
                                                pdidd,
                                                cbRequired,
                                                &cbRequired,
                                                0))
             {
              // Enumerated a battery.  Ask it for information.
              HANDLE hBattery = 
                      CreateFile(pdidd->DevicePath,
                                 GENERIC_READ | GENERIC_WRITE,
                                 FILE_SHARE_READ | FILE_SHARE_WRITE,
                                 NULL,
                                 OPEN_EXISTING,
                                 FILE_ATTRIBUTE_NORMAL,
                                 NULL);
              if (INVALID_HANDLE_VALUE != hBattery)
               {
                // Ask the battery for its tag.
                BATTERY_QUERY_INFORMATION bqi = {0};

                DWORD dwWait = 0;
                DWORD dwOut;

                if (DeviceIoControl(hBattery,
                                    IOCTL_BATTERY_QUERY_TAG,
                                    &dwWait,
                                    sizeof(dwWait),
                                    &bqi.BatteryTag,
                                    sizeof(bqi.BatteryTag),
                                    &dwOut,
                                    NULL)
                    && bqi.BatteryTag)
                 {
                  // With the tag, you can query the battery info.
                  BATTERY_INFORMATION bi = {0};
                  bqi.InformationLevel = BatteryInformation;

                  if (DeviceIoControl(hBattery,
                                      IOCTL_BATTERY_QUERY_INFORMATION,
                                      &bqi,
                                      sizeof(bqi),
                                      &bi,
                                      sizeof(bi),
                                      &dwOut,
                                      NULL))
                   {
                    // Only non-UPS system batteries count
                    if (bi.Capabilities & BATTERY_SYSTEM_BATTERY)
                     {
                      if (!(bi.Capabilities & BATTERY_IS_SHORT_TERM))
                       {
                        dwResult |= GBS_HASBATTERY;
                       }

                      // Query the battery status.
                      BATTERY_WAIT_STATUS bws = {0};
                      bws.BatteryTag = bqi.BatteryTag;

                      BATTERY_STATUS bs;
                      if (DeviceIoControl(hBattery,
                                          IOCTL_BATTERY_QUERY_STATUS,
                                          &bws,
                                          sizeof(bws),
                                          &bs,
                                          sizeof(bs),
                                          &dwOut,
                                          NULL))
                       {
                        if (bs.PowerState & BATTERY_POWER_ON_LINE)
                         {
                          dwResult &= ~GBS_ONBATTERY;
                         }
                       }
                     }
                   }
                 }
                CloseHandle(hBattery);
               }
             }
            LocalFree(pdidd);
           }
         }
       }
        else  if (ERROR_NO_MORE_ITEMS == GetLastError())
         {
          break;  // Enumeration failed - perhaps we're out of items
         }
     }
    SetupDiDestroyDeviceInfoList(hdev);
   }

  //  Final cleanup:  If we didn't find a battery, then presume that we
  //  are on AC power.

  if (!(dwResult & GBS_HASBATTERY))
    dwResult &= ~GBS_ONBATTERY;

  return dwResult;
 }
```



<span data-ttu-id="5b759-110">Чтобы перечислить устройства, подключенные к удаленному компьютеру, используйте класс WMI [**\_ батареи Win32**](/windows/desktop/CIMWin32Prov/win32-battery) в клиентском скрипте или приложении.</span><span class="sxs-lookup"><span data-stu-id="5b759-110">To enumerate the battery devices connected to a remote computer, use the [**Win32\_Battery**](/windows/desktop/CIMWin32Prov/win32-battery) WMI class in a client script or application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b759-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5b759-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b759-112">сетупдижетклассдевс</span><span class="sxs-lookup"><span data-stu-id="5b759-112">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="5b759-113">сетупдиенумдевицеинтерфацес</span><span class="sxs-lookup"><span data-stu-id="5b759-113">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="5b759-114">сетупдижетдевицеинтерфацедетаил</span><span class="sxs-lookup"><span data-stu-id="5b759-114">SetupDiGetDeviceInterfaceDetail</span></span>](https://msdn.microsoft.com/library/ms792901.aspx)
</dt> <dt>

[<span data-ttu-id="5b759-115">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b759-115">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="5b759-116">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="5b759-116">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="5b759-117">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="5b759-117">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 
