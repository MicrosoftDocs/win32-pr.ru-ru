---
description: Некоторые функции политики LSA используют \_ \_ строковую структуру LSA в Юникоде для хранения строковых данных. В этой структуре хранится строка и сведения о ее длине.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Использование строк в Юникоде LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682572"
---
# <a name="using-lsa-unicode-strings"></a>Использование строк в Юникоде LSA

Некоторые функции политики LSA используют [**\_ \_ строковую структуру LSA в Юникоде**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) для хранения строковых данных. В этой структуре хранится строка и сведения о ее длине.

В следующем коде реализуется функция, преобразующая данные **LPWSTR** в структуры [**\_ \_ строк в формате LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) :


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



