---
description: В C++ возвращаемое значение обычно имеет тип HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Возвращаемые значения в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264474"
---
# <a name="return-values-in-c"></a>Возвращаемые значения в C++

В C++ возвращаемое значение обычно имеет тип **HRESULT**. Это возвращаемое значение, которое можно определить, успешно ли выполнен метод, и, если это не так, какова ошибка. Службы сертификатов обычно возвращают \_ значение "ОК" для **HRESULT** после успешного завершения метода. Программные значения, которые необходимо вернуть, возвращаются с помощью параметров out в методе. В следующем примере показан вызов метода C++ для получения свойства запроса:


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



В предыдущем фрагменте кода значение Success или Failure возвращается в переменную **HRESULT** , *HR*. Необходимо проверить переменную **HRESULT** на успешно \[ обработанное в коде на соответствие условию (S \_ OK! = HR) \] . Если метод завершился успешно, значение свойства Request возвращается в параметре **Variant** *варпроп* .

 

 



