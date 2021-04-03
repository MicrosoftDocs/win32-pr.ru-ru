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
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="e2c14-104">Объявление асинхронных функций</span><span class="sxs-lookup"><span data-stu-id="e2c14-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="e2c14-105">Чтобы объявить функцию RPC как асинхронную, сначала объявите функцию как часть определения интерфейса в файле IDL.</span><span class="sxs-lookup"><span data-stu-id="e2c14-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="e2c14-106">Использование асинхронных функций RPC не требует каких-либо специальных изменений IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="e2c14-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="e2c14-107">В следующем примере показан IDL-файл для приложения, использующего одну асинхронную функцию.</span><span class="sxs-lookup"><span data-stu-id="e2c14-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

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

<span data-ttu-id="e2c14-108">Для всех асинхронных функций RPC, используемых приложением, необходимо изменить объявления асинхронных функций в файле ACF приложения.</span><span class="sxs-lookup"><span data-stu-id="e2c14-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="e2c14-109">Примените атрибут [**\[ Async \]**](../midl/async.md) к каждому имени асинхронной функции, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="e2c14-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="e2c14-110">При применении атрибута **\[ Async \]** в файле ACF компилятор MIDL автоматически создает дополнительный параметр асинхронного обработчика в коде заглушки.</span><span class="sxs-lookup"><span data-stu-id="e2c14-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 