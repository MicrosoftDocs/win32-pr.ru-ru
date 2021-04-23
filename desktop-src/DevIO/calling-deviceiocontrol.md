---
description: Вызов DeviceIoControl
ms.assetid: b4dbda89-effb-43f7-b3cc-774db57862a9
title: Вызов DeviceIoControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf032182b4c461f13ebc046d30bc445abbfc9a1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538897"
---
# <a name="calling-deviceiocontrol"></a><span data-ttu-id="83ef2-103">Вызов DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="83ef2-103">Calling DeviceIoControl</span></span>

<span data-ttu-id="83ef2-104">Приложение может использовать функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) для выполнения прямых операций ввода-вывода для или получения сведений о дисководе гибких дисков, жестком диске, ленточном накопителе или дисководе компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="83ef2-104">An application can use the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to perform direct input and output operations on, or retrieve information about, a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span> <span data-ttu-id="83ef2-105">Список стандартных кодов управления, входящих в документацию по пакету SDK, см. в разделе "Примечания" для **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="83ef2-105">For a list of standard control codes included in the SDK documentation, see the Remarks section of **DeviceIoControl**.</span></span>

<span data-ttu-id="83ef2-106">В следующем примере показано, как получить сведения о первом физическом диске в системе.</span><span class="sxs-lookup"><span data-stu-id="83ef2-106">The following example demonstrates how to retrieve information about the first physical drive in the system.</span></span> <span data-ttu-id="83ef2-107">Она использует функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для получения маркера устройства к первому физическому диску, а затем использует [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) с параметром [ioctl \_ диска \_ Get \_ Drive \_](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) управляющий код для [**заполнения \_ геометрической структуры диска**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) информацией о диске.</span><span class="sxs-lookup"><span data-stu-id="83ef2-107">It uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to retrieve the device handle to the first physical drive, and then uses [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) with the [IOCTL\_DISK\_GET\_DRIVE\_GEOMETRY](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) control code to fill a [**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) structure with information about the drive.</span></span>


```C++
#define UNICODE 1
#define _UNICODE 1

/* The code of interest is in the subroutine GetDriveGeometry. The 
   code in main shows how to interpret the results of the call. */

#include <windows.h>
#include <winioctl.h>
#include <stdio.h>

#define wszDrive L"\\\\.\\PhysicalDrive0"

BOOL GetDriveGeometry(LPWSTR wszPath, DISK_GEOMETRY *pdg)
{
  HANDLE hDevice = INVALID_HANDLE_VALUE;  // handle to the drive to be examined 
  BOOL bResult   = FALSE;                 // results flag
  DWORD junk     = 0;                     // discard results

  hDevice = CreateFileW(wszPath,          // drive to open
                        0,                // no access to the drive
                        FILE_SHARE_READ | // share mode
                        FILE_SHARE_WRITE, 
                        NULL,             // default security attributes
                        OPEN_EXISTING,    // disposition
                        0,                // file attributes
                        NULL);            // do not copy file attributes

  if (hDevice == INVALID_HANDLE_VALUE)    // cannot open the drive
  {
    return (FALSE);
  }

  bResult = DeviceIoControl(hDevice,                       // device to be queried
                            IOCTL_DISK_GET_DRIVE_GEOMETRY, // operation to perform
                            NULL, 0,                       // no input buffer
                            pdg, sizeof(*pdg),            // output buffer
                            &junk,                         // # bytes returned
                            (LPOVERLAPPED) NULL);          // synchronous I/O

  CloseHandle(hDevice);

  return (bResult);
}

int wmain(int argc, wchar_t *argv[])
{
  DISK_GEOMETRY pdg = { 0 }; // disk drive geometry structure
  BOOL bResult = FALSE;      // generic results flag
  ULONGLONG DiskSize = 0;    // size of the drive, in bytes

  bResult = GetDriveGeometry (wszDrive, &pdg);

  if (bResult) 
  {
    wprintf(L"Drive path      = %ws\n",   wszDrive);
    wprintf(L"Cylinders       = %I64d\n", pdg.Cylinders);
    wprintf(L"Tracks/cylinder = %ld\n",   (ULONG) pdg.TracksPerCylinder);
    wprintf(L"Sectors/track   = %ld\n",   (ULONG) pdg.SectorsPerTrack);
    wprintf(L"Bytes/sector    = %ld\n",   (ULONG) pdg.BytesPerSector);

    DiskSize = pdg.Cylinders.QuadPart * (ULONG)pdg.TracksPerCylinder *
               (ULONG)pdg.SectorsPerTrack * (ULONG)pdg.BytesPerSector;
    wprintf(L"Disk size       = %I64d (Bytes)\n"
            L"                = %.2f (Gb)\n", 
            DiskSize, (double) DiskSize / (1024 * 1024 * 1024));
  } 
  else 
  {
    wprintf (L"GetDriveGeometry failed. Error %ld.\n", GetLastError ());
  }

  return ((int)bResult);
}
```



 

 
