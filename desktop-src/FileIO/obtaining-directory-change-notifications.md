---
description: Приложение может отслеживать содержимое каталога и его подкаталогов с помощью уведомлений об изменениях.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Получение уведомлений об изменениях каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811321"
---
# <a name="obtaining-directory-change-notifications"></a>Получение уведомлений об изменениях каталога

Приложение может отслеживать содержимое каталога и его подкаталогов с помощью уведомлений об изменениях. Ожидание уведомления об изменении похоже на то, что операция чтения находится в состоянии ожидания для каталога и, при необходимости, его подкаталогов. При возникновении каких-либо изменений в отслеживаемом каталоге операция чтения завершается. Например, приложение может использовать эти функции для обновления каталога в списке при изменении имени файла в отслеживаемом каталоге.

Приложение может указать набор условий, которые активируют уведомление об изменении с помощью функции [**финдфирстчанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) . Условия включают изменения в именах файлов, имена каталогов, атрибуты, размер файла, время последней записи и безопасность. Эта функция также возвращает маркер, который можно ожидать с помощью [функций Wait](/windows/desktop/Sync/wait-functions). Если условие ожидания удовлетворено, [**финднекстчанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) можно использовать для предоставления обработчика уведомлений о ожидании последующих изменений. Однако эти функции не указывают на фактическое изменение, которое удовлетворяет условию ожидания.

Чтобы закрыть маркер уведомления, используйте [**финдклосечанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) .

Чтобы получить сведения о конкретном изменении в составе уведомления, используйте функцию [**реаддиректоричанжесв**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) . Эта функция также позволяет предоставить подпрограммы завершения.

Сведения об отслеживании изменений в томе см. в разделе [журналы изменений](change-journals.md).

В следующем примере в дереве каталогов отслеживается изменение имени каталога. Он также отслеживает изменения имен файлов в каталоге. В примере используется функция [**финдфирстчанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) для создания двух дескрипторов уведомлений и функция [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) для ожидания дескрипторов. Каждый раз, когда каталог создается или удаляется в дереве, в примере необходимо обновить все дерево каталогов. Каждый раз, когда файл создается или удаляется в каталоге, в примере следует обновить каталог.

> [!Note]
>
> В этом упрощенном примере используется функция [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) для завершения и очистки, но более сложные приложения всегда должны использовать правильное управление ресурсами, например [**финдклосечанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) , где это необходимо.

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
