---
title: Остановка серверного приложения
description: Серверное приложение может прекратить прослушивание клиентов, вызвав Рпкмгмтстопсерверлистенинг и Рпксерверунрегистериф или просто выходя из процесса узла.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Удаленный вызов процедур RPC, задачи, остановка серверного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779217"
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



 

 




