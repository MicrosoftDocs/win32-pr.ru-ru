---
title: Иажентбаллунекс Сетнумчарсперлине
description: Иажентбаллунекс Сетнумчарсперлине
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331848"
---
# <a name="iagentballoonexsetnumcharsperline"></a>Иажентбаллунекс:: Сетнумчарсперлине

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Задает количество символов в строке, которые могут отображаться в тексте слова символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.
-   Возвращает значение E \_ INVALIDARG, если значение параметра меньше восьми.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*лчарсперлине*
</dt> <dd>

Число строк, отображаемых в подсказке к слову.

</dd> </dl>

Минимальное значение равно 8, а максимальное — 255. Если текст, указанный в методе [**произношения**](speak-method.md) или [**обработки**](think-method.md) , превышает размер текущего всплывающего окна, агент автоматически прокручивает текст в выноске.

Значение по умолчанию основано на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Жетнумчарсперлине**](iagentballoon--getnumcharsperline.md)


 

 




