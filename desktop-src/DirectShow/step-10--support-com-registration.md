---
description: Шаг 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Шаг 10. Поддержка регистрации COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673993"
---
# <a name="step-10-support-com-registration"></a><span data-ttu-id="5fe1c-104">Шаг 10.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-104">Step 10.</span></span> <span data-ttu-id="5fe1c-105">Поддержка регистрации COM</span><span class="sxs-lookup"><span data-stu-id="5fe1c-105">Support COM Registration</span></span>

<span data-ttu-id="5fe1c-106">Последняя оставшаяся задача — поддержка регистрации COM, чтобы кадр свойств мог создавать новые экземпляры страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="5fe1c-107">Добавьте еще одну запись [**кфакторитемплате**](cfactorytemplate.md) в массив Global *g \_ Templates* , который используется для регистрации всех COM-объектов в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="5fe1c-108">Не включайте какие-либо сведения о настройке фильтра для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-108">Do not include any filter set-up information for the property page.</span></span>


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



<span data-ttu-id="5fe1c-109">Если вы объявили *g \_ ктемплатес* , как показано в следующем коде, он автоматически имеет правильное значение в зависимости от размера массива:</span><span class="sxs-lookup"><span data-stu-id="5fe1c-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="5fe1c-110">Кроме того, добавьте статический `CreateInstance` метод в класс страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="5fe1c-111">Вы можете назвать метод любым предпочтительным, но подпись должна соответствовать показанной в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="5fe1c-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



<span data-ttu-id="5fe1c-112">Чтобы протестировать страницу свойств, зарегистрируйте библиотеку DLL, а затем загрузите фильтр в Графедит.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="5fe1c-113">Щелкните правой кнопкой мыши фильтр и выберите пункт **Свойства фильтра**.</span><span class="sxs-lookup"><span data-stu-id="5fe1c-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fe1c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5fe1c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe1c-115">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="5fe1c-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="5fe1c-116">Создание библиотеки DLL фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="5fe1c-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



