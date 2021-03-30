---
description: В примере кода показан клиент канала, который открывает именованный канал, устанавливает обработчик канала в режим чтения сообщения, использует функцию WriteFile для отправки запроса на сервер и использует функцию ReadFile для чтения ответа сервера.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Клиент именованного канала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896690"
---
# <a name="named-pipe-client"></a>Клиент именованного канала

Клиент именованного канала использует функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия маркера именованного канала. Если канал существует, но все его экземпляры заняты, **CreateFile** возвращает **недопустимое \_ \_ значение Handle** , а функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает канал ошибки \_ \_ . В этом случае клиент именованного канала использует функцию [**ваитнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) для ожидания доступности экземпляра именованного канала.

Функция [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) завершается ошибкой, если указанный доступ несовместим с указанным доступом (Дуплексный, исходящий или входящий трафик), когда сервер создает канал. Для дуплексного канала клиент может указать доступ для чтения, записи или чтения и записи. для исходящего канала (сервер только для записи) клиент должен указать доступ только для чтения. а для входящего канала (сервер только для чтения) клиент должен указать доступ только для записи.

Для маркера, возвращаемого [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) по умолчанию, используется режим чтения байтов, режим ожидания блокировки, режим перекрывающегося режима и отключенный режим записи. Клиент канала может использовать функцию **CreateFile** , чтобы включить режим перекрытия, УКАЗАВ \_ Перекрытие флага файла \_ или включить режим сквозной записи путем указания \_ записи флага файла \_ \_ через. Клиент может использовать функцию [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) для включения неблокирующего режима с помощью указания параметра pipe \_ или включения режима чтения сообщений путем указания \_ сообщения READMODE канала \_ .

В следующем примере показан клиент канала, который открывает именованный канал, устанавливает обработчик канала в режим чтения сообщения, использует функцию [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) для отправки запроса на сервер и использует функцию [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) для чтения ответа сервера. Этот клиент канала можно использовать с любыми серверами типов сообщений, которые перечислены в нижней части этого раздела. Однако при использовании сервера типа Byte этот клиент канала завершается ошибкой, когда вызывает [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) для переключения в режим чтения сообщения. Так как клиент считывает из канала в режиме чтения сообщений, операция **ReadFile** может вернуть ноль после чтения части сообщения. Это происходит, когда размер сообщения больше, чем буфер чтения. В этом случае [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ больше \_ данных, и клиент может прочитать оставшуюся часть сообщения, используя дополнительные вызовы функции **ReadFile**.

Этот клиент канала можно использовать с любыми серверами каналов, указанными в разделе см. также.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
// Try to open a named pipe; wait for it, if necessary. 
 
   while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
   // Break if the pipe handle is valid. 
 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Многопотоковый сервер каналов](multithreaded-pipe-server.md)
</dt> <dt>

[Сервер именованных каналов, использующий перекрывающиеся операции ввода-вывода](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Сервер именованных каналов, использующий подпрограммы завершения](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
