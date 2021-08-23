---
title: Иажентбаллунекс Сетнумчарсперлине
description: Иажентбаллунекс Сетнумчарсперлине
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976464"
---
# <a name="iagentballoonexsetnumcharsperline"></a>Иажентбаллунекс:: Сетнумчарсперлине

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентбаллун:: Жетнумчарсперлине**](iagentballoon--getnumcharsperline.md)


 

 




