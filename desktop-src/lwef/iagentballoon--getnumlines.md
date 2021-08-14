---
title: Иажентбаллун Жетнумлинес
description: Иажентбаллун Жетнумлинес
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478628"
---
# <a name="iagentballoongetnumlines"></a>Иажентбаллун:: Жетнумлинес

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентбаллун:: Жетнумчарсперлине**](iagentballoon--getnumcharsperline.md)


 

 




