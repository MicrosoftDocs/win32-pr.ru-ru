---
title: Иажентбаллун Жетбаккколор
description: Иажентбаллун Жетбаккколор
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068172"
---
# <a name="iagentballoongetbackcolor"></a>Иажентбаллун:: Жетбаккколор

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




