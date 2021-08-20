---
title: Иажентбаллун Жетбаккколор
description: Иажентбаллун Жетбаккколор
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888424"
---
# <a name="iagentballoongetbackcolor"></a>Иажентбаллун:: Жетбаккколор

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Извлекает значение цвета фона, отображаемого в подсказке к слову.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*плбгколор*
</dt> <dd>

Адрес переменной, которая получает параметр цвета для фона всплывающего окна.

</dd> </dl>

Цвет фона, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent. Оно не может быть изменено приложением. Однако пользователь может изменить цвет фона для всех символов на странице свойств Microsoft Agent.

## <a name="see-also"></a>См. также:

[**Иажентбаллун::/ForeColor**](iagentballoon--getforecolor.md)


 

 




