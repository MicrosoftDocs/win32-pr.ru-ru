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
# <a name="named-pipe-client"></a><span data-ttu-id="4da26-103">Клиент именованного канала</span><span class="sxs-lookup"><span data-stu-id="4da26-103">Named Pipe Client</span></span>

<span data-ttu-id="4da26-104">Клиент именованного канала использует функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) для открытия маркера именованного канала.</span><span class="sxs-lookup"><span data-stu-id="4da26-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="4da26-105">Если канал существует, но все его экземпляры заняты, **CreateFile** возвращает **недопустимое \_ \_ значение Handle** , а функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает канал ошибки \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4da26-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="4da26-106">В этом случае клиент именованного канала использует функцию [**ваитнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) для ожидания доступности экземпляра именованного канала.</span><span class="sxs-lookup"><span data-stu-id="4da26-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="4da26-107">Функция [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) завершается ошибкой, если указанный доступ несовместим с указанным доступом (Дуплексный, исходящий или входящий трафик), когда сервер создает канал.</span><span class="sxs-lookup"><span data-stu-id="4da26-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="4da26-108">Для дуплексного канала клиент может указать доступ для чтения, записи или чтения и записи. для исходящего канала (сервер только для записи) клиент должен указать доступ только для чтения. а для входящего канала (сервер только для чтения) клиент должен указать доступ только для записи.</span><span class="sxs-lookup"><span data-stu-id="4da26-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="4da26-109">Для маркера, возвращаемого [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) по умолчанию, используется режим чтения байтов, режим ожидания блокировки, режим перекрывающегося режима и отключенный режим записи.</span><span class="sxs-lookup"><span data-stu-id="4da26-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="4da26-110">Клиент канала может использовать функцию **CreateFile** , чтобы включить режим перекрытия, УКАЗАВ \_ Перекрытие флага файла \_ или включить режим сквозной записи путем указания \_ записи флага файла \_ \_ через.</span><span class="sxs-lookup"><span data-stu-id="4da26-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="4da26-111">Клиент может использовать функцию [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) для включения неблокирующего режима с помощью указания параметра pipe \_ или включения режима чтения сообщений путем указания \_ сообщения READMODE канала \_ .</span><span class="sxs-lookup"><span data-stu-id="4da26-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="4da26-112">В следующем примере показан клиент канала, который открывает именованный канал, устанавливает обработчик канала в режим чтения сообщения, использует функцию [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) для отправки запроса на сервер и использует функцию [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) для чтения ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="4da26-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="4da26-113">Этот клиент канала можно использовать с любыми серверами типов сообщений, которые перечислены в нижней части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="4da26-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="4da26-114">Однако при использовании сервера типа Byte этот клиент канала завершается ошибкой, когда вызывает [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) для переключения в режим чтения сообщения.</span><span class="sxs-lookup"><span data-stu-id="4da26-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="4da26-115">Так как клиент считывает из канала в режиме чтения сообщений, операция **ReadFile** может вернуть ноль после чтения части сообщения.</span><span class="sxs-lookup"><span data-stu-id="4da26-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="4da26-116">Это происходит, когда размер сообщения больше, чем буфер чтения.</span><span class="sxs-lookup"><span data-stu-id="4da26-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="4da26-117">В этом случае [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ больше \_ данных, и клиент может прочитать оставшуюся часть сообщения, используя дополнительные вызовы функции **ReadFile**.</span><span class="sxs-lookup"><span data-stu-id="4da26-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="4da26-118">Этот клиент канала можно использовать с любыми серверами каналов, указанными в разделе см. также.</span><span class="sxs-lookup"><span data-stu-id="4da26-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4da26-119">См. также</span><span class="sxs-lookup"><span data-stu-id="4da26-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da26-120">Многопотоковый сервер каналов</span><span class="sxs-lookup"><span data-stu-id="4da26-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="4da26-121">Сервер именованных каналов, использующий перекрывающиеся операции ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="4da26-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="4da26-122">Сервер именованных каналов, использующий подпрограммы завершения</span><span class="sxs-lookup"><span data-stu-id="4da26-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
