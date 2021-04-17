---
description: Как получить путь GUID тома для каждого локального тома, связанного с буквой диска, используемой в данный момент на компьютере.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Перечисление путей GUID томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663604"
---
# <a name="enumerating-volume-guid-paths"></a>Перечисление путей GUID томов

В примере кода в этом разделе показано, как получить путь **GUID** тома для каждого локального тома, связанного с буквой диска, используемой в данный момент на компьютере.

В примере кода используется функция [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



Пример, в котором перечисляются все локально подключенные тома и отображается путь к устройству, путь **GUID** тома и подключенные пути (включая буквы дисков), см. в разделе [Отображение путей к томам](displaying-volume-paths.md).

 

 



