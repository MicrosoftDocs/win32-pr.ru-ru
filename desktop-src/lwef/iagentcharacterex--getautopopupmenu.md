---
title: Иажентчарактерекс Жетаутопопупмену
description: Иажентчарактерекс Жетаутопопупмену
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b9e23f9c8d9f6fefcc7b2606ebd18ab31ff93c8f8f82c1faf692f92545662d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477982"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>Иажентчарактерекс:: Жетаутопопупмену

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иажентчарактерекс:: сетаутопопупмену**](iagentcharacterex--setautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)


 

 




