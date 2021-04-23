---
title: Создание маркера привязки
description: Клиентская программа распределенного приложения должна создать маркер привязки, указывающий время выполнения RPC, к которому должен быть обращен сервер, и способ связи с сервером.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- Удаленный вызов процедур RPC, задачи, создание маркера привязки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067678"
---
# <a name="creating-a-binding-handle"></a><span data-ttu-id="378c3-104">Создание маркера привязки</span><span class="sxs-lookup"><span data-stu-id="378c3-104">Creating a Binding Handle</span></span>

<span data-ttu-id="378c3-105">Клиентская программа распределенного приложения должна создать маркер привязки, указывающий время выполнения RPC, к которому должен быть обращен сервер, и способ связи с сервером.</span><span class="sxs-lookup"><span data-stu-id="378c3-105">The client program of a distributed application needs to create a binding handle that tells the RPC run time which server should be contacted, and how the server should be contacted.</span></span>

<span data-ttu-id="378c3-106">В следующем фрагменте кода демонстрируется распространенный подход к созданию маркера привязки:</span><span class="sxs-lookup"><span data-stu-id="378c3-106">The following code fragment demonstrates a common approach to creating a binding handle:</span></span>


```C++
RPC_STATUS status;
unsigned short *StringBinding;
RPC_BINDING_HANDLE BindingHandle;
status = RpcStringBindingCompose(NULL,  // Object UUID
             L"ncacn_ip_tcp",           // Protocol sequence to use
             L"MyServer.MyCompany.com", // Server DNS or Netbios Name
             NULL,
             NULL,
             &StringBinding);
// Error checking ommitted. If no error, we proceed below
status = RpcBindingFromStringBinding(StringBinding, &BindingHandle);

// free string regardless of errors from RpcBindingFromStringBinding
RpcStringFree(&StringBinding);

// Error checking ommitted. If no error, we have a valid binding handle
```



 

 




