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
# <a name="return-values-in-c"></a><span data-ttu-id="f30c0-103">Возвращаемые значения в C++</span><span class="sxs-lookup"><span data-stu-id="f30c0-103">Return Values in C++</span></span>

<span data-ttu-id="f30c0-104">В C++ возвращаемое значение обычно имеет тип **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f30c0-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="f30c0-105">Это возвращаемое значение, которое можно определить, успешно ли выполнен метод, и, если это не так, какова ошибка.</span><span class="sxs-lookup"><span data-stu-id="f30c0-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="f30c0-106">Службы сертификатов обычно возвращают \_ значение "ОК" для **HRESULT** после успешного завершения метода.</span><span class="sxs-lookup"><span data-stu-id="f30c0-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="f30c0-107">Программные значения, которые необходимо вернуть, возвращаются с помощью параметров out в методе.</span><span class="sxs-lookup"><span data-stu-id="f30c0-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="f30c0-108">В следующем примере показан вызов метода C++ для получения свойства запроса:</span><span class="sxs-lookup"><span data-stu-id="f30c0-108">The following example shows a C++ method call to retrieve a request property:</span></span>


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



<span data-ttu-id="f30c0-109">В предыдущем фрагменте кода значение Success или Failure возвращается в переменную **HRESULT** , *HR*.</span><span class="sxs-lookup"><span data-stu-id="f30c0-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="f30c0-110">Необходимо проверить переменную **HRESULT** на успешно \[ обработанное в коде на соответствие условию (S \_ OK! = HR) \] .</span><span class="sxs-lookup"><span data-stu-id="f30c0-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="f30c0-111">Если метод завершился успешно, значение свойства Request возвращается в параметре **Variant** *варпроп* .</span><span class="sxs-lookup"><span data-stu-id="f30c0-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



