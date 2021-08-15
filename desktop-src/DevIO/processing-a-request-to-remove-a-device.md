---
description: Приложение получает \_ событие ДБТ девицекуериремове Device, когда компонент в системе решил удалить указанное устройство.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Обработка запроса на удаление устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6432ba2709dd05589acd5f8e0a2d1de6547216c9d24d4c9d742b9ad6dcc838e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956783"
---
# <a name="processing-a-request-to-remove-a-device"></a>Обработка запроса на удаление устройства

Приложение получает событие [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) Device, когда компонент в системе решил удалить указанное устройство. Когда приложение получает это событие, оно должно определить, использует ли оно указанное устройство, и либо отменить, либо подготовиться к удалению.

В следующем примере приложение сохраняет открытый маркер hFile для файла или устройства, представленного именем файла. Приложение регистрирует уведомление о событиях устройства на базовом устройстве, вызывая функцию [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , используя фильтр уведомлений **типа \_ \_ Handle ДБТ Девтип** и указав переменную hFile в элементе **дбч \_ Handle** фильтра.

Приложение обрабатывает событие устройства [ДБТ \_ девицекуериремове](dbt-devicequeryremove.md) , закрывая маркер открытого файла для удаляемого устройства. В случае отмены удаления этого устройства приложение обрабатывает событие [ДБТ \_ девицекуериремовефаилед](dbt-devicequeryremovefailed.md) Device, чтобы повторно открыть этот обработчик на устройстве. После удаления устройства из системы приложение обрабатывает события устройства [ДБТ \_ Девицеремовекомплете](dbt-deviceremovecomplete.md) и [ДБТ \_ девицеремовепендинг](dbt-deviceremovepending.md) , отменяя регистрацию своего дескриптора уведомления для устройства и закрывая все дескрипторы, которые все еще открыты для устройства.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы событий устройств](device-event-types.md)
</dt> </dl>

 

 



