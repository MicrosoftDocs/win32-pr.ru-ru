---
title: Иажентчарактерекс Сеселпмодеон
description: Иажентчарактерекс Сеселпмодеон
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133731"
---
# <a name="iagentcharacterexsethelpmodeon"></a>Иажентчарактерекс:: Сеселпмодеон

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Задает контекстно-зависимый режим справки для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*бхелпмодеон*
</dt> <dd>

Флаг режима справки. Если этот параметр имеет **значение true**, Microsoft Agent включает режим справки для символа.

</dd> </dl>

Если для этого свойства задано **значение true**, то при перемещении по символу или во всплывающем меню для символа указатель мыши превращается в контекстно-зависимый рисунок справки. Когда пользователь щелкает или перетаскивает символ или щелкает элемент во всплывающем меню символа, сервер запускает событие [**иажентнотифисинкекс:: хелпкомплете**](iagentnotifysinkex--helpcomplete.md) и выходит из режима справки.

В режиме справки сервер не отправляет события [**Click**](click-event.md), [**драгстарт**](/windows/desktop/lwef/dragstart-event), [**драгкомплете**](https://www.bing.com/search?q=**DragComplete**)и [**Command**](command-event.md) , если свойство [**жетаутопопупмену**](iagentcharacterex--getautopopupmenu.md) не возвращает **значение true**. В этом случае сервер будет отсылать событие **щелчка** (не выходя из режима справки), но только для правой кнопки мыши, чтобы можно было отобразить всплывающее меню.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иажентчарактерекс:: жеселпмодеон**](iagentcharacterex--gethelpmodeon.md), [ **иажентнотифисинкекс:: хелпкомплете**](iagentnotifysinkex--helpcomplete.md)


 

 