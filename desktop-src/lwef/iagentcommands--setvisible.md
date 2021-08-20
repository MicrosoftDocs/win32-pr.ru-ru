---
title: Иаженткоммандс Сетвисибле
description: Иаженткоммандс Сетвисибле
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979651635c27f5633d5ebeada8e5f2866d383ece0b19a38dd32082596e4712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692787"
---
# <a name="iagentcommandssetvisible"></a>Иаженткоммандс:: Сетвисибле

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 