---
description: Возвращаемое значение для методов интерфейса C++ всегда имеет тип HRESULT; Это значение можно проверить, чтобы определить успешность или сбой.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Возвращаемые значения методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662437"
---
# <a name="method-return-values"></a>Возвращаемые значения методов

Возвращаемое значение для методов интерфейса C++ всегда имеет тип **HRESULT**; Это значение можно проверить, чтобы определить успешность или сбой. Использование параметров OUTPUT позволяет назначать значения переменным во время вызова метода или свойства. В следующем примере показан вызов метода C++ для перечисления поставщиков.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



В предыдущем фрагменте кода в переменную "HR" возвращается значение Success или failure. Если вызов был успешным, HR будет установлен в значение S \_ ОК, а переменная бстрпровидер будет содержать имя перечисленного поставщика.

Вызов C++ для получения значения свойства будет выглядеть следующим образом.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Вызов C++ для установки значения свойства будет следующим:


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



