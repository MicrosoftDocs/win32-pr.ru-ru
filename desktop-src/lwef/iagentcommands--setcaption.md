---
title: Иаженткоммандс Сеткаптион
description: Иаженткоммандс Сеткаптион
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665474"
---
# <a name="iagentcommandssetcaption"></a>Иаженткоммандс:: Сеткаптион

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 