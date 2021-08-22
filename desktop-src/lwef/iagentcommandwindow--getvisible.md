---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949591bc22c93711af19ce18cb024ede9714335f249839eb4819a73e231e0d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976244"
---
# <a name="iagentcommandwindowgetvisible"></a>Иаженткоммандвиндов:: Visible

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткоммандвиндов:: Сетвисибле**](iagentcommandwindow--setvisible.md)


 

 




