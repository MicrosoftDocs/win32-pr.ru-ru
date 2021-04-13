---
title: атрибут midl_user_free
description: '\_ \_ Функция пользовательского освобождения MIDL обеспечивается клиентскими и серверными приложениями для освобождения динамически выделяемой памяти.'
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free атрибута MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337164"
---
# <a name="midl_user_free-attribute"></a>\_свободный пользовательский \_ атрибут MIDL

Функция **\_ пользовательского \_ освобождения MIDL** обеспечивается клиентскими и серверными приложениями для освобождения динамически выделяемой памяти.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Указатель на блок памяти, который должен быть освобожден.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Как клиентское приложение, так и серверное приложение должны реализовывать функцию **\_ пользовательского \_ освобождения MIDL** , если только компиляция не выполняется в режиме использование-Compatibility ([**/ОСФ**](-osf.md)). Функция **\_ \_ бесплатного пользователя MIDL** должна иметь возможность освободить все хранилище, выделенное [**пользователем MIDL \_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Приложения и заглушки **вызывают \_ \_ свободный пользователь MIDL** при работе с объектами, на которые ссылаются указатели:

-   Серверное приложение должно вызывать **MIDL- \_ пользователь \_** , чтобы освободить память, выделенную приложения €, например при удалении указанного узла.
-   Заглушка сервера вызывает **функцию \_ MIDL \_ для освобождения** памяти на сервере после маршалирования всех **\[** аргументов [**out**](out-idl.md) **\]** , **\[** [**in**](in.md), **out \]** и возвращаемого значения.

## <a name="examples"></a>Примеры


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**массивы**](arrays-1.md)
</dt> <dt>

[Массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Атрибуты массива и Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**окне**](in.md)
</dt> <dt>

[**\_пользовательское \_ выделение MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/осф**](-osf.md)
</dt> <dt>

[**заполняет**](out-idl.md)
</dt> <dt>

[**однозначно**](unique.md)
</dt> </dl>

 

 