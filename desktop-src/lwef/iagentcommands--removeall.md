---
title: Иаженткоммандс RemoveAll
description: Иаженткоммандс RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791430"
---
# <a name="iagentcommandsremoveall"></a>Иаженткоммандс:: RemoveAll

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Remove();
```

Удаляет все [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

Удаление всех [**команд**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) также приводит к их удалению из всплывающего меню и **окна «Voice Commands»** , если приложение является входным. **RemoveAll** не удаляет записи сервера или другого клиента.

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md), [**иаженткоммандс:: Remove**](iagentcommands--remove.md)


 

 