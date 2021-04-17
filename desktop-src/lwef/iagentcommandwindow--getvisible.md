---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710055"
---
# <a name="iagentcommandwindowgetvisible"></a>Иаженткоммандвиндов:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Определяет, является ли окно "Voice Commands" видимым или скрытым.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, которая получает **значение true** , если отображается окно "Voice Commands", или **значение false** , если оно скрыто.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандвиндов:: Сетвисибле**](iagentcommandwindow--setvisible.md)


 

 




