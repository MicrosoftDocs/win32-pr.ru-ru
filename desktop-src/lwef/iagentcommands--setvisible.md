---
title: Иаженткоммандс Сетвисибле
description: Иаженткоммандс Сетвисибле
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710259"
---
# <a name="iagentcommandssetvisible"></a>Иаженткоммандс:: Сетвисибле

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Задает значение свойства [**Visible**](visible-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*
</dt> <dd>

Логическое значение, определяющее свойство [**Visible**](visible-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . **Значение true** задает отображение [**заголовка**](caption-property.md) коллекции **команд** при отображении всплывающего меню символа; *Значение false* не отображает.

</dd> </dl>

Для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) необходимо установить свойство [**Caption**](caption-property.md) , а для свойства [**Visible**](visible-property.md) — значение **true** , чтобы оно отображалось во всплывающем меню символа. Свойству **Visible** также должно быть присвоено значение **true** , чтобы команды в коллекции отображались, когда клиентское приложение является входным.

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: OnVisible**](iagentcommands--getvisible.md), [ **иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md)


 

 