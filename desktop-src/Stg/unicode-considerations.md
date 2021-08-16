---
title: Рекомендации по Юникоду
description: Функция Вритефмтусертипестг Service, используемая в методе Save Ипапер, требует строковых параметров в Юникоде.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06f8fa9592d3f29ccf82d42f38a48b2dc57d36bccf79b22b8fe159bad337cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886742"
---
# <a name="unicode-considerations"></a>Рекомендации по Юникоду

Функция **вритефмтусертипестг** Service, используемая в методе [**Ипапер:: Save**](ipaper--save.md) , требует строковых параметров в Юникоде. Это происходит в случае вызовов службы COM/OLE, принимающих строковые параметры. При компиляции для строк ANSI ожидаемые параметры Юникода требуют преобразования из ANSI в Юникод. Этот процесс достигается с помощью некоторых макросов в АППУТИЛ. h, которые могут скрывать преобразования. Например, см. раздел **вритефмтусертипестг**.

Следующий вызов появляется в методе [**Save**](ipaper--save.md) .


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Когда **стосерве** компилируется для ANSI (не для Юникода), этот вызов фактически сокращается до вызова внутренней функции-заместителя аппутил. Для этого в Аппутил. h используется следующая схема макросов, которая является включенным файлом во всех примерах кода. CPP файлы.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



В схеме используются суррогатные функции вызова службы. Версии вызовов ANSI начинаются с \_ . Эти суррогатные функции ANSI реализуются в Аппутил. cpp. Они используются при компиляции образца кода для строк ANSI (по умолчанию в файлах Makefile). Функции службы, которые заменяют суррогаты, поддерживают только строковые параметры в Юникоде. Это приводит к преобразованию некоторых строк из ANSI в Юникод, прежде чем реальный вызов службы COM/OLE выполняется внутри суррогата.

Например, если Юникод не определен во время компиляции, то все вызовы в функциях **вритефмтусертипестг** службы COM фактически изменяются макросами на вызовы \_ функции вритефмтусертипестг, реализованной в аппутил. CPP. Эта функция принимает входной указатель строки ANSI, преобразует его в копию в Юникоде и передает эту копию в Юникоде в качестве строкового параметра в вызове реальной функции **вритефмтусертипестг** .

Вот \_ вритефмтусертипестг из аппутил. cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




