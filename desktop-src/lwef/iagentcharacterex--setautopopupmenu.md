---
title: Иажентчарактерекс Сетаутопопупмену
description: Иажентчарактерекс Сетаутопопупмену
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477962"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>Иажентчарактерекс:: Сетаутопопупмену

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Указывает, будет ли сервер автоматически отображать всплывающее меню символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*баутопопупмену*
</dt> <dd>

Автоматически отображаемый флаг отображения всплывающего меню. Если этот параметр имеет **значение true**, Microsoft Agent автоматически отображает всплывающее меню символа, когда пользователь щелкает правой кнопкой мыши значок символа или символа на панели задач.

</dd> </dl>

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

Если задать для этого свойства **значение false**, можно создать собственное поведение при обработке меню. Чтобы отобразить меню после присвоения этому свойству значения **false**, используйте метод [**Иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md) .

## <a name="see-also"></a>См. также

[**Иажентчарактерекс:: жетаутопопупмену**](iagentcharacterex--getautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)


 

 




