---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889111"
---
# <a name="iagentballoongetvisible"></a>Иажентбаллун:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




