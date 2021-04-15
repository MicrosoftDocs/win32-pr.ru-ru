---
title: Иаженткомманд GetID
description: Иаженткомманд GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412802"
---
# <a name="iagentcommandgetid"></a>Иаженткомманд:: GetID

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

Возвращает идентификатор для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*пдвид*
</dt> <dd>

Адрес переменной, которая получает идентификатор [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md), [**иаженткоммандс:: Remove**](iagentcommands--remove.md)


 

 