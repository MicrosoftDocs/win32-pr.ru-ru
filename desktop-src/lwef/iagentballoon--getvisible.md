---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939026026e18e550ca18838977f00a8878db9039595d9eadd0b30b88235a0248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962324"
---
# <a name="iagentballoongetvisible"></a>Иажентбаллун:: Visible

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Определяет, отображается ли всплывающая подсказка слова как видимая или скрытая.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если всплывающая подсказка слова видима, и **значение false** , если оно скрыто.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иажентбаллун:: Сетвисибле**](iagentballoon--setvisible.md)


 

 




