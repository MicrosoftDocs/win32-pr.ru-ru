---
title: Иажентбаллун Жетнумчарсперлине
description: Иажентбаллун Жетнумчарсперлине
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068560"
---
# <a name="iagentballoongetnumcharsperline"></a>Иажентбаллун:: Жетнумчарсперлине

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Возвращает значение для среднего количества символов в строке, отображаемых в подсказке к слову.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*пбчарсперлине*
</dt> <dd>

Адрес переменной, которая получает количество символов в строке.

</dd> </dl>

Сервер Microsoft Agent автоматически прокручивает строки, отображаемые для речевого вывода, в окне всплывающей программы. Среднее число символов в строке для всплывающего слова символа определяется в редакторе символов Microsoft Agent. Оно не может быть изменено приложением.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Жетнумлинес**](iagentballoon--getnumlines.md)


 

 




