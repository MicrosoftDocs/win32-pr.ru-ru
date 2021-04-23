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
# <a name="method-return-values"></a><span data-ttu-id="681aa-103">Возвращаемые значения методов</span><span class="sxs-lookup"><span data-stu-id="681aa-103">Method Return Values</span></span>

<span data-ttu-id="681aa-104">Возвращаемое значение для методов интерфейса C++ всегда имеет тип **HRESULT**; Это значение можно проверить, чтобы определить успешность или сбой.</span><span class="sxs-lookup"><span data-stu-id="681aa-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="681aa-105">Использование параметров OUTPUT позволяет назначать значения переменным во время вызова метода или свойства.</span><span class="sxs-lookup"><span data-stu-id="681aa-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="681aa-106">В следующем примере показан вызов метода C++ для перечисления поставщиков.</span><span class="sxs-lookup"><span data-stu-id="681aa-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="681aa-107">В предыдущем фрагменте кода в переменную "HR" возвращается значение Success или failure.</span><span class="sxs-lookup"><span data-stu-id="681aa-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="681aa-108">Если вызов был успешным, HR будет установлен в значение S \_ ОК, а переменная бстрпровидер будет содержать имя перечисленного поставщика.</span><span class="sxs-lookup"><span data-stu-id="681aa-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="681aa-109">Вызов C++ для получения значения свойства будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="681aa-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="681aa-110">Вызов C++ для установки значения свойства будет следующим:</span><span class="sxs-lookup"><span data-stu-id="681aa-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



