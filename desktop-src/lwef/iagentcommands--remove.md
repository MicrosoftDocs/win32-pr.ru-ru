---
title: Иаженткоммандс удалить
description: Иаженткоммандс удалить
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477197"
---
# <a name="iagentcommandsremove"></a>Иаженткоммандс:: Remove

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Удаляет указанную [**команду**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*двид*
</dt> <dd>

Идентификатор [**команды**](/windows/desktop/lwef/the-command-object) , удаляемой из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

При удалении [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) она также удаляется из всплывающего меню и из окна " **голосовые команды** ", если приложение является входным.

## <a name="see-also"></a>См. также

[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md), [**иаженткоммандс:: RemoveAll**](iagentcommands--removeall.md)


 

 