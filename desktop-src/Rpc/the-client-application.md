---
title: Клиентское приложение
description: Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488181"
---
# <a name="the-client-application"></a>Клиентское приложение

Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK). Исходный файл Хеллок. c содержит директиву, которая включает созданный MIDL-файл заголовка Hello. h. В Hello. h — это директивы для включения RPC. h и рпкндр. h, которые содержат определения для подпрограмм среды выполнения RPC, **хеллопрок** и **завершения работы**, а также типы данных, используемые клиентскими и серверными приложениями. Компилятор MIDL должен использоваться с примером ниже.

Так как клиент управляет подключением к серверу, клиентское приложение вызывает функции времени выполнения, чтобы установить обработчик для сервера и освободить этот обработчик после завершения удаленных вызовов процедур. Функция [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) объединяет компоненты маркера привязки в строковое представление этого обработчика и выделяет память для привязки строки. Функция [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) создает в клиентском приложении маркер привязки сервера, **Hello \_ клиентифхандле**, из этого строкового представления.

В вызове [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)параметры не указывают UUID, поскольку в этом учебнике предполагается, что имеется только одна реализация интерфейса "Hello". Кроме того, при вызове не указывается сетевой адрес, так как приложение будет использовать значение по умолчанию — локальный хост-компьютер. Последовательность протокола — это символьная строка, представляющая базовый сетевой транспорт. Конечная точка — это имя, которое зависит от последовательности протокола. В этом примере для сетевого транспорта используются именованные каналы, поэтому используется последовательность протокола "нкакн \_ NP". Имя конечной точки — " \\ pipe \\ Hello".

Фактические вызовы удаленных процедур, **хеллопрок** и **Shutdown**, выполняются в обработчике исключений RPC — наборе макросов, которые позволяют управлять исключениями, происходящими вне кода приложения. Если модуль времени выполнения RPC сообщает об исключении, управление передается блоку [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Именно здесь можно вставить код, чтобы выполнить необходимую очистку, а затем завершить работу корректно. Этот пример программы просто информирует пользователя о том, что произошло исключение. Если вы не хотите использовать исключения, можно использовать атрибуты ACF [ \_ состояние](/windows/desktop/Midl/comm-status) связи и [ \_ состояние сбоя](/windows/desktop/Midl/fault-status) для сообщения об ошибках.

После завершения удаленных вызовов процедур клиент сначала вызывает [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) , чтобы освободить память, выделенную для привязки строки. Обратите внимание, что после создания маркера привязки клиентская программа может освободить строковую привязку в любое время. Клиент затем вызывает [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) для освобождения маркера.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
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



 

 