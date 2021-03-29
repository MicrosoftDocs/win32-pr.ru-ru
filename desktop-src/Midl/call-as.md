---
title: call_as - атрибут
description: Атрибут \ Call \_ as \ позволяет сопоставлять функцию, которая не может быть удаленно вызвана удаленной функцией.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as атрибута MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650316"
---
# <a name="call_as-attribute"></a>вызвать \_ как атрибут

Атрибут **\[ вызвать \_ как \]** позволяет сопоставлять функцию, которая не может быть удаленно вызвана удаленной функцией.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Локальная процедура* 
</dt> <dd>

Задает определяемую операцией подпрограммы.

</dd> <dt>

*Operation-Attribute-список* 
</dt> <dd>

Указывает один или несколько атрибутов, которые применяются к операции. Несколько атрибутов разделяются запятыми.

</dd> <dt>

*имя операции* 
</dt> <dd>

Указывает именованную операцию, представленную для приложения.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Возможность сопоставлять функции, которые нельзя вызывать удаленно в удаленную функцию, особенно полезна в интерфейсах с множеством типов параметров, которые не могут передаваться по сети. Вместо того чтобы использовать многие **\[** типы [**представления \_**](represent-as.md) **\]** и передачи в **\[** [**\_ качестве**](transmit-as.md) **\]** типов, можно объединить все преобразования с помощью **\[ вызова \_ в качестве \]** подпрограмм. Вы предоставляете два **\[ вызова \_ как \]** подпрограммы (на стороне клиента и на стороне сервера) для привязки подпрограммы между вызовами приложения и удаленными вызовами.

Для интерфейсов объектов можно использовать атрибут **\[ Call \_ как \]** . В этом случае определение интерфейса можно использовать для локальных вызовов, а также для удаленных вызовов, так как **\[ вызов \_ как \]** позволяет удаленно сопоставлять интерфейс, который недоступен для прозрачного доступа к удаленному интерфейсу. Атрибут **\[ вызова \_ As \]** не может использоваться с режимом [**/ОСФ**](-osf.md) .

Например, предположим, что для подпрограммы **F1** в интерфейсе объектов **IFace** требуется много преобразований между вызовами пользователя и фактически передаваемыми. В следующих примерах описываются файлы IDL и ACF для интерфейса **IFace**.

В IDL-файле для интерфейса **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

В ACF для интерфейса **IFace**:

``` syntax
[call_as( f1 )] Remf1();
```

В результате созданный файл заголовка определяет интерфейс с помощью определения **F1**, но также предоставляет заглушки для **Remf1**.

Компилятор MIDL создаст следующую таблицу vtable в файле заголовка для интерфейса **IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

Прокси на стороне клиента будет иметь стандартный созданный MIDL прокси для **Remf1**, а заглушка на стороне сервера для **Remf1** будет такой же, как и стандартная заглушка, созданная MIDL:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

Затем два **\[ вызова \_ как \]** подпрограммы облигаций (на стороне клиента и на стороне сервера) должны быть закодированы вручную:

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

Для объектных интерфейсов это прототипы подпрограмм облигаций.

Для клиентской стороны:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Для серверной части:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

Для необъектных интерфейсов это прототипы подпрограмм облигаций.

Для клиентской стороны:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Для серверной части:

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**/осф**](-osf.md)
</dt> <dt>

[**представлять \_ как**](represent-as.md)
</dt> <dt>

[**передать \_ как**](transmit-as.md)
</dt> </dl>

 

 




