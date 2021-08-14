---
title: Получение атрибута objectClass
description: Атрибут objectClass содержит класс, экземпляр которого является объектом, а также все классы, из которых этот класс является производным.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c4ae206298937839a965eca787b0d56b0021cff32c7d89b06865bb27855a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184145"
---
# <a name="retrieving-the-objectclass-attribute"></a>Получение атрибута objectClass

Атрибут **objectClass** содержит класс, экземпляр которого является объектом, а также все классы, из которых этот класс является производным. Например, класс **User** наследуется от **Top**, **Person** и **организатионалперсон**; Таким образом, атрибут **objectClass** содержит имена этих классов, а также пользователя. Итак, как узнать, какой класс является экземпляром объекта? Атрибут **objectClass** является единственным атрибутом с несколькими значениями, имеющими упорядоченные значения. Первое значение — это вершина иерархии классов, которая является самым верхним классом, а Последнее значение является самым производным классом, который является классом, экземпляром которого является объект.

Следующая функция принимает указатель на столбец, содержащий атрибут **objectClass** , и возвращает экземпляр **objectClass** объекта.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




