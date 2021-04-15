---
title: Иажентбаллун Жетнумлинес
description: Иажентбаллун Жетнумлинес
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411357"
---
# <a name="iagentballoongetnumlines"></a>Иажентбаллун:: Жетнумлинес

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Получает значение числа строк, отображаемых в выноске.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*пклинес*
</dt> <dd>

Адрес переменной, которая получает количество отображаемых строк.

</dd> </dl>

Сервер Microsoft Agent автоматически прокручивает строки, отображаемые для речевого вывода, в окне всплывающей программы. Число строк для текстового всплывающего слова определяется в редакторе символов Microsoft Agent. Оно не может быть изменено приложением.

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Жетнумчарсперлине**](iagentballoon--getnumcharsperline.md)


 

 




