---
title: Иажентчарактерекс Жетаутопопупмену
description: Иажентчарактерекс Жетаутопопупмену
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986678"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>Иажентчарактерекс:: Жетаутопопупмену

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

Определяет, будет ли сервер автоматически отображать всплывающее меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*пбаутопопупмену*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если сервер Microsoft Agent автоматически обрабатывает отображение всплывающего меню символа и **значение false** в противном случае.

</dd> </dl>

Если для этого свойства задано значение **false**, приложение должно отобразить всплывающее меню с помощью метода [**Иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md) .

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также:

[**Иажентчарактерекс:: сетаутопопупмену**](iagentcharacterex--setautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)


 

 




