---
title: Атрибут async
description: Атрибут \ Async \ ACF определяет удаленный вызов процедуры в качестве асинхронной операции.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- асинхронный атрибут MIDL
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987428"
---
# <a name="async-attribute"></a>Атрибут async

Атрибут \[ **Async** \] ACF определяет удаленный вызов процедуры в качестве асинхронной операции.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*OPT-ACF — атрибуты* 
</dt> <dd>

Указывает необязательные атрибуты конфигурации приложения.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции в IDL-файле.

</dd> <dt>

*Param-List* 
</dt> <dd>

Указывает необязательный список параметров.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот атрибут неприменим в интерфейсах COM.

Чтобы объявить функцию RPC как асинхронную, сначала объявите функцию как часть определения интерфейса в IDL-файле. Затем измените объявление функции в файле конфигурации приложения (ACF), применив \[  \] атрибут Async. Обратите внимание, что в объявлении функции нет упоминания о асинхронном обработчике и что этот маркер привязки является первым параметром. Применение атрибута \[ **Async** \] в файле ACF создает соответствующий код, чтобы при вызове этой функции асинхронный сервер получал асинхронный обработчик перед другими параметрами.

> [!Note]  
> Атрибут async нельзя использовать с параметром командной строки [**/ОСФ**](-osf.md) .

 

## <a name="examples"></a>Примеры

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Асинхронный RPC](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 