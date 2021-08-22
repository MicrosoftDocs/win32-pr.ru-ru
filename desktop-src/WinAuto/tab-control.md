---
title: Элемент управления вкладки (Справочник по элементам пользовательского интерфейса MSAA)
description: Элемент управления "Вкладка" определяет несколько страниц для одной области окна или диалогового окна.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fe3216194da590b0c0802343afc41b1f7765c13d194e533163f9af2c22b287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505664"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Элемент управления вкладки (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются **управляющие объекты вкладки** для ссылки на элемент ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание **управляющих объектов вкладок** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Элемент управления "Вкладка" определяет несколько страниц для одной области окна или диалогового окна. Каждая страница состоит из набора сведений или группы элементов управления, которые отображаются приложением, когда пользователь выбирает соответствующую вкладку. Windows операционная система использует элементы управления вкладки для вывода кнопок панели задач, за исключением кнопки **запустить** .

Имя класса окна для элемента управления "Вкладка" — это WC \_ TABCONTROL, который определен как "систабконтрол" в коммктрл. h.

## <a name="iaccessible-methods"></a>Методы IAccessible

Элемент управления "Вкладка" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Примечания                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) выбирает вкладку страницы. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элемент управления "Вкладка" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Свойство **DefaultAction** имеет значение "Switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Свойство **кэйбоардшорткут** — это клавиша доступа элемента управления «вкладка», которая представляет собой подчеркнутый символ в тексте окна элемента управления. Эта строка содержит символ клавиши доступа, добавленный к строке "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** получается из текста окна элемента управления (или заголовка), которое отображается внутри элемента управления "Вкладка".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **Родительское** свойство — это окно ( [**\_ \_ пажетаблист системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет то же имя класса окна, что и элемент управления.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** имеет [**роль \_ System \_ пажетаб**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**получить \_ аккселектион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** — это сочетание одного или нескольких из следующих [значений](object-state-constants.md): системная система состояния " [**\_ \_ невидимая**](object-state-constants.md) система состояния" \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Выбранная**](object-state-constants.md) система состояний \| [**\_ \_ фокус**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) системы состояния \| [**\_ \_**](object-state-constants.md) выбранной системы<br/> |



 

## <a name="notes"></a>Примечания

Элементы управления "Вкладка" неправильно возвращают " \_ ОК" из метода [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) при вызове с флагом [**селфлаг \_ такефокус**](selflag.md) . Элементы управления "Вкладка" не могут принимать фокус клавиатуры.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





