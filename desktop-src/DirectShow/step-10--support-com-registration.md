---
description: Шаг 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Шаг 10. Поддержка регистрации COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68efdeda754d5f7b728138a26a6bc9f4b782918f8c4b5140fd2457bcee6012f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652154"
---
# <a name="step-10-support-com-registration"></a>Шаг 10. Поддержка регистрации COM

Последняя оставшаяся задача — поддержка регистрации COM, чтобы кадр свойств мог создавать новые экземпляры страницы свойств. Добавьте еще одну запись [**кфакторитемплате**](cfactorytemplate.md) в массив Global *g \_ Templates* , который используется для регистрации всех COM-объектов в библиотеке DLL. Не включайте какие-либо сведения о настройке фильтра для страницы свойств.


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



Если вы объявили *g \_ ктемплатес* , как показано в следующем коде, он автоматически имеет правильное значение в зависимости от размера массива:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Кроме того, добавьте статический `CreateInstance` метод в класс страницы свойств. Вы можете назвать метод любым предпочтительным, но подпись должна соответствовать показанной в следующем примере:


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



Чтобы протестировать страницу свойств, зарегистрируйте библиотеку DLL, а затем загрузите фильтр в Графедит. Щелкните правой кнопкой мыши фильтр и выберите пункт **Свойства фильтра**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> <dt>

[создание библиотеки DLL для фильтра DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 



