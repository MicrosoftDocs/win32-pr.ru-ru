---
title: Указатели и выделение памяти
description: Возможность изменения памяти с помощью указателей часто требует, чтобы сервер и клиент выделили достаточно памяти для элементов массива.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927364"
---
# <a name="pointers-and-memory-allocation"></a>Указатели и выделение памяти

Возможность изменения памяти с помощью указателей часто требует, чтобы сервер и клиент выделили достаточно памяти для элементов массива.

Когда заглушка должна выделить или освободить память, она вызывает функции библиотеки времени выполнения, которые, в свою очередь, вызывают функции [**MIDL для \_ пользовательского \_ выделения**](/windows/desktop/Midl/midl-user-allocate-1) и [**MIDL \_ \_**](/windows/desktop/Midl/midl-user-free-1). Эти функции не включаются в библиотеку времени выполнения. Вам необходимо написать собственные версии этих функций и связать их с приложением. Таким образом можно решить, как управлять памятью. При компиляции файла IDL в режиме использование-Compatibility (**/ОСФ**) не требуется реализовывать эти функции. Эти функции необходимо записать в следующие прототипы:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Например, версии этих функций для приложения могут просто вызывать стандартные функции библиотеки:


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 