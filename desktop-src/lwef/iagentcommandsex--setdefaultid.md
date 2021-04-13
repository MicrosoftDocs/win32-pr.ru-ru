---
title: Иаженткоммандсекс Сетдефаултид
description: Иаженткоммандсекс Сетдефаултид
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412864"
---
# <a name="iagentcommandsexsetdefaultid"></a>Иаженткоммандсекс:: Сетдефаултид

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Задает идентификатор команды по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*двид*
</dt> <dd>

Идентификатор для [**команды**](/windows/desktop/lwef/the-command-object) , которая должна быть задана в качестве значения по умолчанию.

</dd> </dl>

Это свойство задает объект [**команды**](/windows/desktop/lwef/the-command-object) по умолчанию, заданный в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Команда по умолчанию выделяется полужирным шрифтом во всплывающем меню символа. Однако установка команды по умолчанию не изменяет обработку команд или события двойного щелчка.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: Жетдефаултид**](iagentcommandsex--getdefaultid.md)


 

 