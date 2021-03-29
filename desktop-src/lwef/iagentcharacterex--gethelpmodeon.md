---
title: Иажентчарактерекс Жеселпмодеон
description: Иажентчарактерекс Жеселпмодеон
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258925"
---
# <a name="iagentcharacterexgethelpmodeon"></a>Иажентчарактерекс:: Жеселпмодеон

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Возвращает значение, указывающее, включен ли контекстно-зависимый режим справки для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*пбхелпмодеон*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если режим справки включен для символа, и **значение false** в противном случае.

</dd> </dl>

Если для этого свойства задано значение **true**, указатель мыши превращается в контекстно-зависимый рисунок справки при перемещении по символу или во всплывающем меню для символа. Когда пользователь щелкает или перетаскивает символ или щелкает элемент во всплывающем меню символа, сервер запускает событие [**иажентнотифисинкекс:: хелпкомплете**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) и выходит из режима справки.

В режиме справки сервер не отправляет события [**иажентнотифисинк:: Click**](iagentnotifysink--click.md), [**Иажентнотифисинк::D рагстарт**](iagentnotifysink--dragstart.md), [**Иажентнотифисинк::D Рагкомплете**](iagentnotifysink--dragcomplete.md)и [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) , если только свойство [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) не возвращает **значение true**. В этом случае сервер отправит событие **иажентнотифисинк:: Click** (не выходит из режима справки), но только для нажатия правой кнопки мыши, чтобы отобразить всплывающее меню.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иажентчарактерекс:: Сеселпмодеон**](iagentcharacterex--sethelpmodeon.md)


 

 




