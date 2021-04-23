---
title: Рекомендации по Юникоду
description: Функция Вритефмтусертипестг Service, используемая в методе Save Ипапер, требует строковых параметров в Юникоде.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888411"
---
# <a name="unicode-considerations"></a><span data-ttu-id="e525a-103">Рекомендации по Юникоду</span><span class="sxs-lookup"><span data-stu-id="e525a-103">Unicode Considerations</span></span>

<span data-ttu-id="e525a-104">Функция **вритефмтусертипестг** Service, используемая в методе [**Ипапер:: Save**](ipaper--save.md) , требует строковых параметров в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e525a-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="e525a-105">Это происходит в случае вызовов службы COM/OLE, принимающих строковые параметры.</span><span class="sxs-lookup"><span data-stu-id="e525a-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="e525a-106">При компиляции для строк ANSI ожидаемые параметры Юникода требуют преобразования из ANSI в Юникод.</span><span class="sxs-lookup"><span data-stu-id="e525a-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="e525a-107">Этот процесс достигается с помощью некоторых макросов в АППУТИЛ. h, которые могут скрывать преобразования.</span><span class="sxs-lookup"><span data-stu-id="e525a-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="e525a-108">Например, см. раздел **вритефмтусертипестг**.</span><span class="sxs-lookup"><span data-stu-id="e525a-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="e525a-109">Следующий вызов появляется в методе [**Save**](ipaper--save.md) .</span><span class="sxs-lookup"><span data-stu-id="e525a-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="e525a-110">Когда **стосерве** компилируется для ANSI (не для Юникода), этот вызов фактически сокращается до вызова внутренней функции-заместителя аппутил.</span><span class="sxs-lookup"><span data-stu-id="e525a-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="e525a-111">Для этого в Аппутил. h используется следующая схема макросов, которая является включенным файлом во всех примерах кода. CPP файлы.</span><span class="sxs-lookup"><span data-stu-id="e525a-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="e525a-112">В схеме используются суррогатные функции вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e525a-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="e525a-113">Версии вызовов ANSI начинаются с \_ .</span><span class="sxs-lookup"><span data-stu-id="e525a-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="e525a-114">Эти суррогатные функции ANSI реализуются в Аппутил. cpp.</span><span class="sxs-lookup"><span data-stu-id="e525a-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="e525a-115">Они используются при компиляции образца кода для строк ANSI (по умолчанию в файлах Makefile).</span><span class="sxs-lookup"><span data-stu-id="e525a-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="e525a-116">Функции службы, которые заменяют суррогаты, поддерживают только строковые параметры в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e525a-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="e525a-117">Это приводит к преобразованию некоторых строк из ANSI в Юникод, прежде чем реальный вызов службы COM/OLE выполняется внутри суррогата.</span><span class="sxs-lookup"><span data-stu-id="e525a-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="e525a-118">Например, если Юникод не определен во время компиляции, то все вызовы в функциях **вритефмтусертипестг** службы COM фактически изменяются макросами на вызовы \_ функции вритефмтусертипестг, реализованной в аппутил. CPP.</span><span class="sxs-lookup"><span data-stu-id="e525a-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="e525a-119">Эта функция принимает входной указатель строки ANSI, преобразует его в копию в Юникоде и передает эту копию в Юникоде в качестве строкового параметра в вызове реальной функции **вритефмтусертипестг** .</span><span class="sxs-lookup"><span data-stu-id="e525a-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="e525a-120">Вот \_ вритефмтусертипестг из аппутил. cpp.</span><span class="sxs-lookup"><span data-stu-id="e525a-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




