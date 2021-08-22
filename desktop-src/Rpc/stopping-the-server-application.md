---
title: Остановка серверного приложения
description: Серверное приложение может прекратить прослушивание клиентов, вызвав Рпкмгмтстопсерверлистенинг и Рпксерверунрегистериф или просто выходя из процесса узла.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Удаленный вызов процедур RPC, задачи, остановка серверного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83f0a96732b1c862cf3e00d25cc2d2d9caf27ae5d764a9edab00c78aaf18682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925144"
---
# <a name="stopping-the-server-application"></a>Остановка серверного приложения

Серверное приложение может прекратить прослушивание клиентов, вызвав [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) и [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)или просто выходя из процесса узла. Оба метода приемлемы. Если сервер соответствует первому подходу, он должен реализовать следующие шаги:

Функция сервера [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) не возвращает вызывающей программе, пока не произойдет исключение или пока не будет вызван вызов [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) . По умолчанию для остановки сервера RPC с помощью **рпкмгмтстопсерверлистенинг** можно использовать только другой поток сервера. Клиенты, пытающиеся приостановить работу сервера, получат сообщение об ошибке \_ \_ отказа в доступе RPC S \_ . Однако можно настроить RPC, чтобы разрешить некоторым или всем клиентам прекращать работу сервера. Дополнительные сведения см. в разделе **рпкмгмтстопсерверлистенинг** .

Кроме того, клиентское приложение может выполнить удаленный вызов процедур в подпрограммы завершения работы на сервере. Подпрограммы завершения работы вызывают [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) и [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). В этом примере программное приложение использует этот подход, добавляя новую удаленную функцию **Shutdown** в файл хеллоп. c.

В функции **Shutdown** один параметр NULL для [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) указывает, что локальное приложение должно прекращать прослушивание удаленных вызовов процедур. Два параметра NULL для [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) — это подстановочные знаки, указывающие, что все интерфейсы должны быть отменены. Параметр **false** указывает, что интерфейс должен быть немедленно удален из реестра, а не ожидать завершения отложенных вызовов.


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




