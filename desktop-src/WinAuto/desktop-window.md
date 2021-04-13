---
title: Окно рабочего стола (Справочник по элементам пользовательского интерфейса MSAA)
description: В окне рабочего стола отображается представление списка рабочего стола (в котором содержатся значки, такие как Мой компьютер) и панель задач, содержащая кнопку «Пуск».
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410704"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Окно рабочего стола (Справочник по элементам пользовательского интерфейса MSAA)

В окне рабочего стола отображается представление списка рабочего стола (в котором содержатся значки, такие как Мой компьютер) и панель задач, содержащая кнопку « **Пуск** ».

Этот объект редко запрашивается клиентами, так как представление списка и панель задач охватывают весь рабочий стол. Объект Desktop извлекается при входе в систему, прежде чем оболочка операционной системы отобразит представление списка и панель задач. В некоторых случаях Рабочий стол получается при переходе от других объектов.

Имя класса Window для окна рабочего стола — " \# 32769".

## <a name="iaccessible-methods"></a>Методы IAccessible

Окно рабочего стола поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Окно рабочего стола поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                 | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Свойство Name имеет значение "Desktop".                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**получить \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md):[**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





