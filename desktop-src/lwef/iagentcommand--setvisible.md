---
title: Иаженткомманд Сетвисибле
description: Иаженткомманд Сетвисибле
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691504"
---
# <a name="iagentcommandsetvisible"></a>Иаженткомманд:: Сетвисибле

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Задает значение свойства [**Visible**](visible-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*
</dt> <dd>

Логическое значение, определяющее свойство [**Visible**](visible-property.md) [**команды**](/windows/desktop/lwef/the-command-object). **Значение true** показывает **команду**; **Значение false** скрывает его.

</dd> </dl>

Свойству [**Visible**](visible-property.md) [**команды**](/windows/desktop/lwef/the-command-object) должно быть присвоено значение **true** , а свойство [**Caption**](caption-property.md) со значением отображается во всплывающем меню символа.

## <a name="see-also"></a>См. также:

[**Иаженткомманд::**](iagentcommand--getvisible.md), [**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)


 

 