---
title: Расширение вспомогательного класса NDF с передачей
description: Этот вспомогательный класс имеет зависимость низкого уровня работоспособности от Симплефилехелперкласс, закодированной в первом примере.
ms.assetid: b59cd855-c68a-4f5c-b145-ceac395ddcc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dab07fb29b8ccebad0263cd3c71cccd83c98ba6d28b8ceb05e4334d61d1059c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802184"
---
# <a name="ndf-helper-class-extension-with-handoff"></a>Расширение вспомогательного класса NDF с передачей

Этот вспомогательный класс имеет зависимость низкого уровня работоспособности от Симплефилехелперкласс, закодированной в первом примере.

Второй вспомогательный класс передачи является простым транзитным вспомогательным классом, который не выполняет никакой диагностики. Вместо этого он всегда создает более низкую гипотезу о работоспособности для Симплефилехелперкласс. Это полезно в качестве заполнителя для будущего добавления возможностей диагностики в этом вспомогательном классе. Вспомогательный класс передачи реализует два метода.

Метод Ловхеалс используется для установки состояния диагностики DS \_ неопределенный. Это делает NDF вызовом Жетловерхипосесес.


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::LowHealth( 
    /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
    /* [string][out] */ LPWSTR *ppwszDescription,
    /* [out] */ long *pDeferredTime,
    /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    *pStatus = DS_INDETERMINATE;
    return S_OK;
}

```



Затем Жетловерхипосесес реализуется, чтобы сообщить NDF, какой вспомогательный класс следует диагностировать.


```C++
#include <windows.h>

HRESULT HandOffTestHelperClass::GetLowerHypotheses( 
ULONG *Count,
HYPOTHESIS **Hypotheses)
{
    HRESULT hr = S_OK;
    HYPOTHESIS *pHypothesis=NULL;
    HELPER_ATTRIBUTE *pAttr=NULL;

    pHypothesis = (PHYPOTHESIS)CoTaskMemAlloc(sizeof(HYPOTHESIS));
    if (pHypothesis == NULL)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pHypothesis, sizeof(HYPOTHESIS));

    pAttr = (PHELPER_ATTRIBUTE)CoTaskMemAlloc(sizeof(HELPER_ATTRIBUTE));
    if (pAttr  == NULL)
    {
       hr = E_OUTOFMEMORY;
       goto Error;
    }
    SecureZeroMemory(pAttr, sizeof(HELPER_ATTRIBUTE));

    //set the helper class name to hand off to
    hr = StringCchCopyWithAlloc(&pHypothesis->pwszClassName, MAX_PATH,
                 L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    //populate the attribute
    //set the attribute name
    hr = StringCchCopyWithAlloc(&pAttr->pwszName, MAX_PATH, L"filename");
    if (FAILED(hr))
    {
        goto Error;  
    }

    //set attribute data
    pAttr->type = AT_STRING;
    hr = StringCchCopyWithAlloc(&pAttr->PWStr, MAX_PATH, m_pwszTestFile);
    if (FAILED(hr))
    {
        goto Error;
    }

    //set the attributes to the hypothesis  
    pHypothesis->celt = 1; //number of attributes
    pHypothesis->rgAttributes=pAttr;

    //pass data back
    *pcelt = 1; //one hypothesis
    *pprgHypotheses = pHypothesis;

    return S_OK;

Error:

    if (pAttr)
    {
        if (pAttr->PWStr) 
            CoTaskMemFree(pAttr->PWStr);
        if (pAttr->pwszName) 
            CoTaskMemFree(pAttr->pwszName);
    }

    if (pHypothesis)
    {
        if (pHypothesis->pwszClassName) 
            CoTaskMemFree(pHypothesis->pwszClassName);
        CoTaskMemFree(pHypothesis);
    }
    return hr;
}

```



 

 




