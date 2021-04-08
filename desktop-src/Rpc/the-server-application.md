---
title: Серверное приложение
description: Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK).
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888432"
---
# <a name="the-server-application"></a>Серверное приложение

Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK). Серверная часть распределенного приложения информирует систему о доступности служб. Затем он ожидает клиентские запросы. Компилятор MIDL должен использоваться с примером ниже.

В зависимости от размера приложения и настроек кода можно реализовать удаленные процедуры в одном или нескольких отдельных файлах. В этой программе учебника исходный файл Hello. c содержит основную подпрограмму сервера. Файл Хеллоп. c содержит удаленную процедуру.

Преимущество организации удаленных процедур в отдельных файлах заключается в том, что процедуры можно связать с автономной программой для отладки кода перед его преобразованием в распределенное приложение. После того как процедуры будут работать в автономной программе, можно скомпилировать и связать исходные файлы, содержащие удаленные процедуры, с серверным приложением. Как и в случае с исходным файлом клиентского приложения, исходный файл серверного приложения должен включать файл заголовка Hello. h.

Сервер вызывает функции времени выполнения RPC [**рпксерверусепротсекеп**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) и [**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , чтобы сделать сведения о привязке доступными для клиента. Этот пример программы передает имя обработчика интерфейса в **рпксерверрегистериф**. Другие параметры имеют значение **null**. Затем сервер вызывает функцию [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) , чтобы указать, что она ожидает клиентские запросы.

Серверное приложение также должно включать две функции управления памятью, которые вызываются заглушкой сервера: MIDL, пользовательское [**\_ \_ выделение**](the-midl-user-allocate-function.md) и [**MIDL \_ \_**](the-midl-user-free-function.md). Эти функции выделяют и освобождают память на сервере, когда удаленная процедура передает параметры на сервер. В этом примере программы MIDL для пользовательского **\_ \_ выделения** и **MIDL \_ является \_** просто оболочками для функций C-Library [**malloc**](pointers-and-memory-allocation.md) и **Free**. (Обратите внимание, что в объявлениях, созданных компилятором MIDL, "MIDL" является прописной буквой. В файле заголовка Рпкндр. h определено пользовательское \_ \_ бесплатное значение MIDL, а \_ пользователь MIDL \_ выделит пользователя MIDL \_ \_ свободным и MIDL \_ \_ , соответственно.)


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




