---
title: Функция midl_user_free
description: '\_Пользовательская \_ функция MIDL должна предоставляться разработчиками RPC.'
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413572"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="8ada8-103">\_ \_ Функция Free пользователя MIDL</span><span class="sxs-lookup"><span data-stu-id="8ada8-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="8ada8-104">**\_ Пользовательская \_ функция MIDL** должна предоставляться разработчиками RPC.</span><span class="sxs-lookup"><span data-stu-id="8ada8-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="8ada8-105">Она выделяет память для заглушек RPC и подпрограмм библиотеки.</span><span class="sxs-lookup"><span data-stu-id="8ada8-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="8ada8-106">Функция **\_ \_ бесплатного пользователя MIDL** должна соответствовать следующему прототипу:</span><span class="sxs-lookup"><span data-stu-id="8ada8-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="8ada8-107">Параметр *pBuffer* указывает указатель на память, которая должна быть освобождена.</span><span class="sxs-lookup"><span data-stu-id="8ada8-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="8ada8-108">Как клиентское приложение, так и серверное приложение должны реализовывать функцию **\_ пользовательского \_ освобождения MIDL** , если только не выполняется компиляция в режиме использование-Compatibility ([**/ОСФ**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="8ada8-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="8ada8-109">Функция **\_ \_ бесплатного пользователя MIDL** должна иметь возможность освободить все хранилище, выделенное [**пользователем MIDL \_ \_**](the-midl-user-allocate-function.md).</span><span class="sxs-lookup"><span data-stu-id="8ada8-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="8ada8-110">Приложения и заглушки **вызывают \_ \_ свободный пользователь MIDL** при работе с выделенными объектами:</span><span class="sxs-lookup"><span data-stu-id="8ada8-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="8ada8-111">Серверное приложение должно вызывать **MIDL \_ user \_ бесплатно** для освобождения памяти, выделенной приложением, например при удалении динамически выделенного узла данных.</span><span class="sxs-lookup"><span data-stu-id="8ada8-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="8ada8-112">Заглушка сервера вызывает **метод \_ MIDL \_ ,** чтобы освободить память на сервере после маршалирования всех \[ \] аргументов out, in, \[ \] \[ out \] и возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="8ada8-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="8ada8-113">Например, программа RPC Windows в образце, которая отображает "Hello, World", применяет **Пользовательский интерфейс MIDL \_ \_ без** функции C:</span><span class="sxs-lookup"><span data-stu-id="8ada8-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="8ada8-114">Если пакет RPCSS включен (например, в результате использования \[ атрибута [**включения \_ выделения**](/windows/desktop/Midl/enable-allocate) \] ), серверная программа должна использовать [**рпксмфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="8ada8-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="8ada8-115">Дополнительные сведения см. в статье [пакет управления памятью RPCSS](rpcss-memory-management-package.md).</span><span class="sxs-lookup"><span data-stu-id="8ada8-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 