---
title: Иаженткоммандс Сеткаптион
description: Иаженткоммандс Сеткаптион
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412822"
---
# <a name="iagentcommandssetcaption"></a>Иаженткоммандс:: Сеткаптион

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Задает текст [**заголовка**](caption-property.md) , отображаемого для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*
</dt> <dd>

Объект BSTR, указывающий значение для свойства [**Caption**](caption-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Установка свойства [**Caption**](caption-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение **true** , а приложение не является клиентом ввода-активного. Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.

При определении команд для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , для которой задан [**заголовок**](caption-property.md) , обычно также определяется **заголовок** для коллекции **Commands** .

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: oncaption**](iagentcommands--getcaption.md), [**Иаженткоммандс:: сетвисибле**](iagentcommands--setvisible.md), [**иаженткоммандс:: сетвоице**](iagentcommands--setvoice.md)


 

 