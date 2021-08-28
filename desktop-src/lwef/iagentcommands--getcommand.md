---
title: Иаженткоммандс, команда
description: Иаженткоммандс, команда
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ae5e8a92ce8d4a8e04ff049569195e5a2baa21ec3bc398f5fa6ba6ef3c1e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609694"
---
# <a name="iagentcommandsgetcommand"></a>Иаженткоммандс:: Command

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Извлекает объект [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*двкоммандид*
</dt> <dd>

Идентификатор объекта [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Адрес интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для объекта [**Command**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

## <a name="see-also"></a>См. также:

[**иаженткомманд**](iagentcommand.md)


 

 