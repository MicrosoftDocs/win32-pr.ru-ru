---
title: Окно клиента MDI (Справочник по элементам пользовательского интерфейса MSAA)
description: Многодокументный интерфейс (MDI) — это спецификация, определяющая стандартный пользовательский интерфейс для приложений, написанных для Windows. Приложение MDI позволяет пользователю работать с несколькими документами за раз.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986432"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Окно клиента MDI (Справочник по элементам пользовательского интерфейса MSAA)

Многодокументный интерфейс (MDI) — это спецификация, определяющая стандартный пользовательский интерфейс для приложений, написанных для Windows. Приложение MDI позволяет пользователю работать с несколькими документами за раз.

Приложение MDI имеет три вида окон: окно фрейма, окно клиента и несколько дочерних окон. Окно фрейма аналогично главному окну приложения и окружено клиентским окном. Окно клиента является дочерним по отношению к окну фрейма и служит фоном для дочерних окон. Клиентское окно также обеспечивает поддержку для создания дочерних окон, в которых отображаются документы, и управления ими.

Имя класса окна для клиентского окна MDI — "Мдиклиент".

## <a name="iaccessible-methods"></a>Методы IAccessible

MDI-окно клиента поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

MDI-окно клиента поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                 | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Свойство **ChildCount** — это количество дочерних окон, в которых отображаются документы.                                                                                                                                                                                                                                                                                                                                                                              |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Свойство **Name** имеет значение "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | **Родительское** свойство — это окно фрейма MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Свойство **Role** является [**\_ \_ клиентской системой роли**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





