---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133719"
---
# <a name="iagentcharactergetvisible"></a>Иажентчарактер:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

Определяет, видима ли в данный момент кадр анимации символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если фрейм символа является видимым, и **false** , если он скрыт.

</dd> </dl>

С помощью этого метода можно определить, видима ли в данный момент рамка символа. Чтобы сделать символ видимым, используйте метод [**Показать**](/windows/desktop/lwef/iagentcharacter--show) . Чтобы скрыть символ, используйте метод [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .

 

 