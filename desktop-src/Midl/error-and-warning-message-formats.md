---
title: Форматы сообщений об ошибках и предупреждений
description: Список форматов сообщений об ошибках MIDL и предупреждений.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- ошибки MIDL, форматы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384420"
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

Это сообщение сформировано непредвиденной ошибкой. шестнадцатеричный номер ошибки — это Windows XP, Windows 2000, Windows NT, Windows 98 или Windows 95 идентификатор системной ошибки. Дополнительные сведения можно найти в файле Winerror. h или NTSTATUS. h. Дополнительные сведения о работе с условиями, вызвавшими эту ошибку, см. в тексте ошибки [ошибки компилятора](compiler-errors.md) MIDL9008.

 

 




