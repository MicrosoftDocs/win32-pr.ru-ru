---
description: Возвращает значение HRESULT. В этом значении HRESULT значение S \_ ОК указывает, что метод успешно выполнен.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Свойства управления регистрацией сертификатов в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771923"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Свойства управления регистрацией сертификатов в C++

При установке или извлечении свойства управления регистрацией сертификата в C++ вызов метода возвращает **значение HRESULT**. В этом значении **HRESULT** значение S \_ ОК указывает, что метод успешно выполнен.

Программы, написанные на C++, могут извлекать свойства управления регистрацией сертификатов по вызовам методов в следующей форме.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Где *PropertyName* указывает имя свойства, к которому осуществляется доступ, а *ппропвалуе* — указатель на переменную соответствующего типа данных. После успешного завершения этого вызова метода *ппропвалуе* будет указывать на переменную, содержащую значение свойства *PropertyName* .

Например, чтобы получить значение для свойства **рутсторетипе** , используйте следующий код.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



Программы, написанные на языке C++, могут задавать свойства управления регистрацией сертификатов путем вызова методов в следующей форме.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Где *PropertyName* указывает имя свойства, к которому осуществляется доступ, а *пропвалуе* — значение соответствующего типа данных. После успешного завершения вызова этого метода новое значение свойства *PropertyName* будет *пропвалуе*.

Например, чтобы задать значение свойства для **рутсторетипе**, можно использовать следующий код.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



