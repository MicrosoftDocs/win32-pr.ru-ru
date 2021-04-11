---
description: Приложение получает \_ событие ДБТ девицекуериремове Device, когда компонент в системе решил удалить указанное устройство.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Обработка запроса на удаление устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141506"
---
# <a name="processing-a-request-to-remove-a-device"></a><span data-ttu-id="854ef-103">Обработка запроса на удаление устройства</span><span class="sxs-lookup"><span data-stu-id="854ef-103">Processing a Request to Remove a Device</span></span>

<span data-ttu-id="854ef-104">Приложение получает событие [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) Device, когда компонент в системе решил удалить указанное устройство.</span><span class="sxs-lookup"><span data-stu-id="854ef-104">An application receives a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event when a feature in the system has decided to remove a specified device.</span></span> <span data-ttu-id="854ef-105">Когда приложение получает это событие, оно должно определить, использует ли оно указанное устройство, и либо отменить, либо подготовиться к удалению.</span><span class="sxs-lookup"><span data-stu-id="854ef-105">When the application receives this event, it should determine whether it is using the specified device and either cancel or prepare for the removal.</span></span>

<span data-ttu-id="854ef-106">В следующем примере приложение сохраняет открытый маркер hFile для файла или устройства, представленного именем файла.</span><span class="sxs-lookup"><span data-stu-id="854ef-106">In the following example, an application maintains an open handle, hFile, to the file or device represented by FileName.</span></span> <span data-ttu-id="854ef-107">Приложение регистрирует уведомление о событиях устройства на базовом устройстве, вызывая функцию [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , используя фильтр уведомлений **типа \_ \_ Handle ДБТ Девтип** и указав переменную hFile в элементе **дбч \_ Handle** фильтра.</span><span class="sxs-lookup"><span data-stu-id="854ef-107">The application registers for device event notification on the underlying device by calling the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function, using a **DBT\_DEVTYP\_HANDLE** type notification filter and specifying the hFile variable in the **dbch\_handle** member of the filter.</span></span>

<span data-ttu-id="854ef-108">Приложение обрабатывает событие устройства [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) , закрывая маркер открытого файла для удаляемого устройства.</span><span class="sxs-lookup"><span data-stu-id="854ef-108">The application processes the [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) device event by closing the open file handle to the device that is to be removed.</span></span> <span data-ttu-id="854ef-109">В случае отмены удаления этого устройства приложение обрабатывает событие [ДБТ \_ девицекуериремовефаилед](dbt-devicequeryremovefailed.md) Device, чтобы повторно открыть этот обработчик на устройстве.</span><span class="sxs-lookup"><span data-stu-id="854ef-109">In the event that removal of this device is canceled, the application processes the [DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) device event to reopen the handle to the device.</span></span> <span data-ttu-id="854ef-110">После удаления устройства из системы приложение обрабатывает события устройства [ДБТ \_ Девицеремовекомплете](dbt-deviceremovecomplete.md) и [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) , отменяя регистрацию своего дескриптора уведомления для устройства и закрывая все дескрипторы, которые все еще открыты для устройства.</span><span class="sxs-lookup"><span data-stu-id="854ef-110">After the device has been removed from the system, the application processes the [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) device events by unregistering its notification handle for the device and closing any handles that are still open to the device.</span></span>


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="854ef-111">См. также</span><span class="sxs-lookup"><span data-stu-id="854ef-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="854ef-112">Типы событий устройств</span><span class="sxs-lookup"><span data-stu-id="854ef-112">Device Event Types</span></span>](device-event-types.md)
</dt> </dl>

 

 



