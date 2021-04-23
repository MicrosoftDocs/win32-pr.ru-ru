---
description: Возвращает значение HRESULT. В этом значении HRESULT значение S \_ ОК указывает, что метод успешно выполнен.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Свойства управления регистрацией сертификатов в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541135"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="19520-104">Свойства управления регистрацией сертификатов в C++</span><span class="sxs-lookup"><span data-stu-id="19520-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="19520-105">При установке или извлечении свойства управления регистрацией сертификата в C++ вызов метода возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="19520-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="19520-106">В этом значении **HRESULT** значение S \_ ОК указывает, что метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="19520-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="19520-107">Программы, написанные на C++, могут извлекать свойства управления регистрацией сертификатов по вызовам методов в следующей форме.</span><span class="sxs-lookup"><span data-stu-id="19520-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="19520-108">Где *PropertyName* указывает имя свойства, к которому осуществляется доступ, а *ппропвалуе* — указатель на переменную соответствующего типа данных.</span><span class="sxs-lookup"><span data-stu-id="19520-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="19520-109">После успешного завершения этого вызова метода *ппропвалуе* будет указывать на переменную, содержащую значение свойства *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="19520-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="19520-110">Например, чтобы получить значение для свойства **рутсторетипе** , используйте следующий код.</span><span class="sxs-lookup"><span data-stu-id="19520-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="19520-111">Программы, написанные на языке C++, могут задавать свойства управления регистрацией сертификатов путем вызова методов в следующей форме.</span><span class="sxs-lookup"><span data-stu-id="19520-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="19520-112">Где *PropertyName* указывает имя свойства, к которому осуществляется доступ, а *пропвалуе* — значение соответствующего типа данных.</span><span class="sxs-lookup"><span data-stu-id="19520-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="19520-113">После успешного завершения вызова этого метода новое значение свойства *PropertyName* будет *пропвалуе*.</span><span class="sxs-lookup"><span data-stu-id="19520-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="19520-114">Например, чтобы задать значение свойства для **рутсторетипе**, можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="19520-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



