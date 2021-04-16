---
description: Транзакция именованного канала — это обмен данными между клиентом и сервером, объединяющий операцию записи и операцию чтения в одну сетевую операцию. Транзакции повышают производительность сетевого взаимодействия между клиентом и удаленным сервером.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Транзакции по именованным каналам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489039b92b65f57cefc71c5d78a01b1824b1418a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546839"
---
# <a name="transactions-on-named-pipes"></a><span data-ttu-id="07ed2-104">Транзакции по именованным каналам</span><span class="sxs-lookup"><span data-stu-id="07ed2-104">Transactions on Named Pipes</span></span>

<span data-ttu-id="07ed2-105">Транзакция именованного канала — это обмен данными между клиентом и сервером, объединяющий операцию записи и операцию чтения в одну сетевую операцию.</span><span class="sxs-lookup"><span data-stu-id="07ed2-105">A named pipe transaction is a client/server communication that combines a write operation and a read operation into a single network operation.</span></span> <span data-ttu-id="07ed2-106">Транзакция может использоваться только с дуплексным каналом типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="07ed2-106">A transaction can be used only on a duplex, message-type pipe.</span></span> <span data-ttu-id="07ed2-107">Транзакции повышают производительность сетевого взаимодействия между клиентом и удаленным сервером.</span><span class="sxs-lookup"><span data-stu-id="07ed2-107">Transactions improve the performance of network communications between a client and a remote server.</span></span> <span data-ttu-id="07ed2-108">Процессы могут использовать функции [**трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) и [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) для выполнения именованных транзакций каналов.</span><span class="sxs-lookup"><span data-stu-id="07ed2-108">Processes can use the [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) and [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) functions to perform named pipe transactions.</span></span>

<span data-ttu-id="07ed2-109">Функция [**трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) чаще всего используется клиентом канала для записи сообщения запроса на сервер именованных каналов и считывания ответного сообщения сервера.</span><span class="sxs-lookup"><span data-stu-id="07ed2-109">The [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) function is most commonly used by a pipe client to write a request message to the named pipe server and read the server's response message.</span></span> <span data-ttu-id="07ed2-110">Клиент канала должен указать универсальный \_ доступ на запись для чтения \| \_ при открытии его обработчика канала, вызвав функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="07ed2-110">The pipe client must specify GENERIC\_READ \| GENERIC\_WRITE access when it opens its pipe handle by calling the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="07ed2-111">Затем клиент канала устанавливает обработчик канала в режим чтения сообщения, вызывая функцию [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .</span><span class="sxs-lookup"><span data-stu-id="07ed2-111">Then, the pipe client sets the pipe handle to message-read mode by calling the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function.</span></span> <span data-ttu-id="07ed2-112">Если буфер чтения, указанный в вызове **трансактнамедпипе** , недостаточно велик для хранения всего сообщения, записанного сервером, функция возвращает ноль, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ больше \_ данных.</span><span class="sxs-lookup"><span data-stu-id="07ed2-112">If the read buffer specified in the call to **TransactNamedPipe** is not large enough to hold the entire message written by the server, the function returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="07ed2-113">Клиент может прочитать оставшуюся часть сообщения, вызвав либо функцию [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**Реадфиликс**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), либо [**пикнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) .</span><span class="sxs-lookup"><span data-stu-id="07ed2-113">The client can read the remainder of the message by calling either the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), or [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) function.</span></span>

<span data-ttu-id="07ed2-114">[**Трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) обычно вызывается клиентами канала, но может также использоваться сервером канала.</span><span class="sxs-lookup"><span data-stu-id="07ed2-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) is typically called by pipe clients, but can also be used by a pipe server.</span></span>

<span data-ttu-id="07ed2-115">В следующем примере показан клиент канала, использующий [**трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="07ed2-115">The following example shows a pipe client using [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span></span> <span data-ttu-id="07ed2-116">Этот клиент канала можно использовать с любыми серверами каналов, указанными в разделе см. также.</span><span class="sxs-lookup"><span data-stu-id="07ed2-116">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
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
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



<span data-ttu-id="07ed2-117">Клиент канала использует [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) для объединения вызовов функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**ваитнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (при необходимости), [**трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)и [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) в один вызов.</span><span class="sxs-lookup"><span data-stu-id="07ed2-117">A pipe client uses [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) to combine the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (if necessary), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function calls into a single call.</span></span> <span data-ttu-id="07ed2-118">Поскольку обработчик канала закрывается до возвращения функции, все дополнительные байты в сообщении теряются, если размер сообщения превышает указанный для буфера чтения.</span><span class="sxs-lookup"><span data-stu-id="07ed2-118">Because the pipe handle is closed before the function returns, any additional bytes in the message are lost if the message is larger than the specified size of the read buffer.</span></span> <span data-ttu-id="07ed2-119">В следующем примере приведен предыдущий пример, написанный для использования **каллнамедпипе**.</span><span class="sxs-lookup"><span data-stu-id="07ed2-119">The following example is the previous example rewritten to use **CallNamedPipe**.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="07ed2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="07ed2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ed2-121">Многопотоковый сервер каналов</span><span class="sxs-lookup"><span data-stu-id="07ed2-121">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="07ed2-122">Сервер именованных каналов, использующий перекрывающиеся операции ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="07ed2-122">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="07ed2-123">Сервер именованных каналов, использующий подпрограммы завершения</span><span class="sxs-lookup"><span data-stu-id="07ed2-123">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
