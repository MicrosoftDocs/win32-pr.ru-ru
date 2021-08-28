---
title: Иажентбаллунекс Сетнумлинес
description: Иажентбаллунекс Сетнумлинес
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848724"
---
# <a name="iagentballoonexsetnumlines"></a>Иажентбаллунекс:: Сетнумлинес

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Задает количество строк вывода текста, которые могут отображаться в тексте всплывающего слова символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.
-   Возвращает значение E \_ INVALIDARG, если параметр равен нулю.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*ллинес*
</dt> <dd>

Число строк, отображаемых в подсказке к слову.

</dd> </dl>

Минимальное значение — 1, а максимальное — 128. Если текст, указанный в методе [**произношения**](speak-method.md) или [**обработки**](think-method.md) , превышает размер текущего всплывающего окна, агент автоматически прокручивает текст в выноске.

Этот метод завершится ошибкой, если установлен бит стиля всплывающего окна **сизетотекст** .

Значение по умолчанию основано на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.

## <a name="see-also"></a>См. также

[**Иажентбаллун:: жетнумлинес**](iagentballoon--getnumlines.md), [**Иажентбаллунекс:: Style**](iagentballoonex--getstyle.md), [**иажентбаллунекс:: SetStyle**](iagentballoonex--setstyle.md)


 

 




