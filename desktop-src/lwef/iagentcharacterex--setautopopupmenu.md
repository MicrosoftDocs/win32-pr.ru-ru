---
title: Иажентчарактерекс Сетаутопопупмену
description: Иажентчарактерекс Сетаутопопупмену
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986534"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>Иажентчарактерекс:: Сетаутопопупмену

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иажентчарактерекс:: жетаутопопупмену**](iagentcharacterex--getautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)


 

 




