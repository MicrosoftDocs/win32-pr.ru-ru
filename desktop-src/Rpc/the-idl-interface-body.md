---
title: Тело интерфейса IDL
description: Текст интерфейса IDL содержит типы данных, используемые в удаленных вызовах процедур, и прототипы функций для удаленных процедур.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792654"
---
# <a name="the-idl-interface-body"></a><span data-ttu-id="3149f-103">Тело интерфейса IDL</span><span class="sxs-lookup"><span data-stu-id="3149f-103">The IDL Interface Body</span></span>

<span data-ttu-id="3149f-104">Текст интерфейса IDL содержит типы данных, используемые в удаленных вызовах процедур, и прототипы функций для удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="3149f-104">The IDL interface body contains data types used in remote procedure calls and the function prototypes for the remote procedures.</span></span> <span data-ttu-id="3149f-105">Тело интерфейса может также содержать импорты, прагмы, объявления констант и объявления типов.</span><span class="sxs-lookup"><span data-stu-id="3149f-105">The interface body can also contain imports, pragmas, constant declarations, and type declarations.</span></span> <span data-ttu-id="3149f-106">В режиме расширений Microsoft компилятор MIDL также допускает неявные объявления в форме определений переменных.</span><span class="sxs-lookup"><span data-stu-id="3149f-106">In Microsoft-extensions mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="3149f-107">В следующем примере показан IDL-файл, содержащий определение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3149f-107">The following example shows an IDL file containing the definition of an interface.</span></span> <span data-ttu-id="3149f-108">Текст определения интерфейса, который находится между фигурными скобками, содержит определение константы (**буфсизе**), тип (**\_ \_ тип обработчика пконтекст**) и некоторые удаленные процедуры (**ремотеопен**, **ремотереад**, **ремотеклосе** и **Shutdown**).</span><span class="sxs-lookup"><span data-stu-id="3149f-108">The body of the interface definition, which occurs between the curly brackets, contains the definition of a constant (**BUFSIZE**), a type (**PCONTEXT\_HANDLE\_TYPE**), and some remote procedures (**RemoteOpen**, **RemoteRead**, **RemoteClose**, and **Shutdown**).</span></span>

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

<span data-ttu-id="3149f-109">Дополнительные сведения см. в [справочнике по языку MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="3149f-109">For more information see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 