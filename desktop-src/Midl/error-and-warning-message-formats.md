---
title: Форматы сообщений об ошибках и предупреждений
description: Список форматов сообщений об ошибках MIDL и предупреждений.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- ошибки MIDL, форматы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42552b8106b72d82b2b13b69a7cba7ac2e99e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411345"
---
# <a name="error-and-warning-message-formats"></a>Форматы сообщений об ошибках и предупреждений

Ошибки командной строки отображаются в следующем формате:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

В поле Дополнительные сведения об ошибке предоставляются сведения, зависящие от контекста, в зависимости от сообщения об ошибке. Например, при возникновении неразрешенной ошибки объявления типа в поле дополнительных сведений об ошибке отображается имя типа, который не удалось разрешить.

Предупреждения времени компиляции отображаются в следующем формате:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Ошибки времени компиляции отображаются в следующем формате:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

Необязательные сведения о контексте относятся к контексту, в котором произошла ошибка. Он создается, когда компилятор MIDL обнаруживает ошибку во время семантического анализа сигнатур типа и процедуры. Компилятор MIDL сообщает эти сведения, чтобы помочь быстро найти ошибку в IDL-файле.

Системные сообщения об ошибках отображаются в следующем формате:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Это сообщение сформировано непредвиденной ошибкой. Шестнадцатеричный номер ошибки — это идентификатор системной ошибки Windows XP, Windows 2000, Windows NT, Windows 98 или Windows 95. Дополнительные сведения можно найти в файле Winerror. h или NTSTATUS. h. Дополнительные сведения о работе с условиями, вызвавшими эту ошибку, см. в тексте ошибки [ошибки компилятора](compiler-errors.md) MIDL9008.

 

 




