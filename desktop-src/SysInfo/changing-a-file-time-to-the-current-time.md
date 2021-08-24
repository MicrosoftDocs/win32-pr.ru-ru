---
description: В следующем примере время последней записи для файла устанавливается в текущее системное время с помощью функции Сетфилетиме.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Изменение времени файла на текущее время
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bbc2d9edef02d703542cea8372602724d76857c26099fe67f811d6c3b004e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958647"
---
# <a name="changing-a-file-time-to-the-current-time"></a>Изменение времени файла на текущее время

В следующем примере время последней записи для файла устанавливается в текущее системное время с помощью функции [**сетфилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) .

В файловой системе NTFS значения времени хранятся в формате UTC, поэтому изменения в часовом поясе и летнем времени не затрагиваются. Файловая система FAT хранит значения времени на основе местного времени компьютера.

Файл должен быть открыт с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) с \_ \_ доступом к атрибутам записи файла.


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
