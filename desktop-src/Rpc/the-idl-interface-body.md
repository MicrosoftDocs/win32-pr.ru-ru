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
# <a name="the-idl-interface-body"></a>Тело интерфейса IDL

Текст интерфейса IDL содержит типы данных, используемые в удаленных вызовах процедур, и прототипы функций для удаленных процедур. Тело интерфейса может также содержать импорты, прагмы, объявления констант и объявления типов. В режиме расширений Microsoft компилятор MIDL также допускает неявные объявления в форме определений переменных.

В следующем примере показан IDL-файл, содержащий определение интерфейса. Текст определения интерфейса, который находится между фигурными скобками, содержит определение константы (**буфсизе**), тип (**\_ \_ тип обработчика пконтекст**) и некоторые удаленные процедуры (**ремотеопен**, **ремотереад**, **ремотеклосе** и **Shutdown**).

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

Дополнительные сведения см. в [справочнике по языку MIDL](/windows/desktop/Midl/midl-language-reference).

 

 