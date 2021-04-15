---
title: Пример кода для проверки прав на создание объектов схемы
description: В следующем примере кода C/C++ показана функция, которая проверяет атрибут Алловедчилдклассесеффективе в контейнере схемы (указатель IADs на контейнер схемы передается в качестве параметра) для классов attributeSchema и classSchema.
ms.assetid: 3abc2351-a3cf-4a6c-9a13-15dd51723883
ms.tgt_platform: multiple
keywords:
- Пример кода для проверки прав на создание объектов схемы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef0d4958313a189a0a50c0b4233fdb4a30aaf75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486616"
---
# <a name="example-code-for-checking-for-rights-to-create-schema-objects"></a>Пример кода для проверки прав на создание объектов схемы

В следующем примере кода C/C++ показана функция, которая проверяет атрибут **алловедчилдклассесеффективе** в контейнере схемы (указатель iAds на контейнер схемы передается в качестве параметра) для классов **attributeSchema** и **classSchema** . Он возвращает **\_ ОК** , если оба класса перечислены в **алловедчилдклассесеффективе**. Если эти значения не равны, возвращается **\_ значение S false**.


```C++

// Function takes an IADs pointer to schema container as a parameter.
 
HRESULT HasSchemaAdditionRights(IADs *pSchema)
{
if (!pSchema)
  return E_POINTER;
HRESULT hr = E_FAIL;
VARIANT var;
VARIANT *pVar;
// Check access rights.
BOOL bIsAddAttributeAllowed = FALSE;
BOOL bIsAddClassAllowed = FALSE;
// Get AllowedChildClassesEffective. It is constructed;
// therefore, you must use GetInfoEx to explicitly 
// get it into the cache.
LPOLESTR pwszArray[] = {L"allowedChildClassesEffective"};
DWORD dwArrayItems = sizeof(pwszArray)/sizeof(LPOLESTR);
VARIANT vArray;
VariantInit(&vArray);
// Build a Variant of array type, using the specified string array.
hr = ADsBuildVarArrayStr(pwszArray, dwArrayItems, &vArray);
if (SUCCEEDED(hr))
{
  hr = pSchema->GetInfoEx(vArray,0L);
  if (SUCCEEDED(hr))
  {
    hr = pSchema->GetEx(CComBSTR("allowedChildClassesEffective"), 
                        &var);
    if (SUCCEEDED(hr))
    {
       hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), 
                                (void HUGEP* FAR*)&pVar);
       long lLBound, lUBound;
       // One-dimensional array. Get the bounds for the array.
       hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 
                               1,
                               &lLBound);
       hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 
                               1, 
                               &lUBound);
       // Get the count of elements
       long cElements = lUBound-lLBound + 1;
       // Get the elements of the array.
       if (SUCCEEDED(hr))
       {
        for (int i = 0; i < cElements; i++ ) 
        {
          // Check each element to verify that attributeSchema 
          // or classSchema is there.
          if (VT_BSTR == pVar[i].vt)
          {
            if (0==_wcsicmp(L"attributeSchema", pVar[i].bstrVal))
              bIsAddAttributeAllowed = TRUE;
            else if (0==_wcsicmp(L"classSchema", pVar[i].bstrVal))
              bIsAddClassAllowed = TRUE;
          }
        }
        if (bIsAddAttributeAllowed && bIsAddClassAllowed)
          hr = S_OK;
        else
          hr = S_FALSE;
       }
    }
    VariantClear(&var);
  }
}
 
return hr;
 
};
```



 

 




