---
description: Инструкции по удалению подключенной папки с помощью функции Делетеволумемаунтпоинт.
ms.assetid: 33049110-acf8-4db5-a9c4-bd4a884c8590
title: Удаление подключенной папки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b177aa2010d33b84aa98993d66952c50acb014e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543050"
---
# <a name="deleting-a-mounted-folder"></a><span data-ttu-id="4898d-103">Удаление подключенной папки</span><span class="sxs-lookup"><span data-stu-id="4898d-103">Deleting a Mounted Folder</span></span>

<span data-ttu-id="4898d-104">В примере кода в этом разделе показано, как удалить подключенную папку с помощью функции [**делетеволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="4898d-104">The code example in this topic shows you how to delete a mounted folder by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="4898d-105">Дополнительные сведения см. в разделе [Создание подключенных папок](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="4898d-105">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>


```C++
#define _WIN32_WINNT 0x0501

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void
Syntax (TCHAR *argv)
{
   _tprintf(TEXT("%s unmounts a volume from a volume mount point\n"), 
          argv);
   _tprintf(TEXT("For example: \"%s c:\\mnt\\fdrive\\\"\n"), argv);
}

int _tmain(int argc, TCHAR *argv[])
{
   BOOL bFlag;

   if (argc != 2)
   {
      Syntax (argv[0]);
      return (-1);
   }

// We should do some error checking on the path argument, such as
// ensuring that there is a trailing backslash.

   bFlag = DeleteVolumeMountPoint(
              argv[1] // Path of the volume mount point
           );

   _tprintf(TEXT("\n%s %s in unmounting the volume at %s\n"), argv[0],
           bFlag ? TEXT("succeeded") : TEXT("failed"), argv[1]);

   return (bFlag);
}
```



 

 



