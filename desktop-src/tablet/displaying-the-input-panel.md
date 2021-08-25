---
description: Общие сведения о отображении панели ввода.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Отображение панели ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940794"
---
# <a name="displaying-the-input-panel"></a>Отображение панели ввода

\[[**Пенинпутпанел**](peninputpanel-class.md) был заменен [**текстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) для управляемого кода). Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]

Порядок различных событий фокуса для элемента управления выглядит следующим образом:

-   [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control. Проверка](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control. Validated](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Нет никакой гарантии, что элемент управления на самом деле имеет фокус на момент, когда свойство [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) записывается, когда оно задано в обработчике событий [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) . Событие Control. Enter является лучшим местом для присоединения объекта [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) к элементу управления, но событие [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) является лучшим местом для изменения свойства [пенинпутпанел. Visible](/previous-versions/ms571984(v=vs.100)) .

 

 
