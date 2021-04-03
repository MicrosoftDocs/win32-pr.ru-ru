---
title: Объявление асинхронных функций
description: Чтобы объявить функцию RPC как асинхронную, сначала объявите функцию как часть определения интерфейса в файле IDL.
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Удаленный вызов процедур RPC, задачи, объявление асинхронных функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103987958"
---
# <a name="declaring-asynchronous-functions"></a>Объявление асинхронных функций

Чтобы объявить функцию RPC как асинхронную, сначала объявите функцию как часть определения интерфейса в файле IDL. Использование асинхронных функций RPC не требует каких-либо специальных изменений IDL-файла. В следующем примере показан IDL-файл для приложения, использующего одну асинхронную функцию.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Для всех асинхронных функций RPC, используемых приложением, необходимо изменить объявления асинхронных функций в файле ACF приложения. Примените атрибут [**\[ Async \]**](../midl/async.md) к каждому имени асинхронной функции, как показано в следующем примере:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

При применении атрибута **\[ Async \]** в файле ACF компилятор MIDL автоматически создает дополнительный параметр асинхронного обработчика в коде заглушки.

 

 