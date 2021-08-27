---
description: Возвращаемое значение для методов интерфейса C++ всегда имеет тип HRESULT; Это значение можно проверить, чтобы определить успешность или сбой.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Возвращаемые значения методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073df1d306fb991d7e1347ff90a21d578bf42583c642a694de3160b405963a28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100764"
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



 

 



