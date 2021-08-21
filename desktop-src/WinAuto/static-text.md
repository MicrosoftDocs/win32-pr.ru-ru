---
title: Статический текст (Справочник по элементам пользовательского интерфейса MSAA)
description: Элементы управления "статический текст" предоставляют удобный способ для вывода текста в диалоговых окнах и других окнах. Статические текстовые элементы управления часто служат метками для других элементов управления.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052492"
---
# <a name="static-text-msaa-ui-element-reference"></a>Статический текст (Справочник по элементам пользовательского интерфейса MSAA)

Элементы управления "статический текст" предоставляют удобный способ для вывода текста в диалоговых окнах и других окнах. Статические текстовые элементы управления часто служат метками для других элементов управления.

Имя класса окна для статического текстового элемента управления — «STATIC».

## <a name="iaccessible-methods"></a>Методы IAccessible

Элементы управления "статический текст" поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Свойства IAccessible

Элементы управления "статический текст" поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Примечания                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Свойство **ChildCount** равно нулю.                                                                                                                                                                                                                                                          |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Свойство **кэйбоардшорткут** — это клавиша доступа, которая является подчеркнутым символом в тексте, который активирует элемент управления, связанный со статическим текстом. Возвращаемая строка содержит символ клавиши доступа, добавленный к строке "Alt +".                                           |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** совпадает с текстом в элементе управления "статический текст".                                                                                                                                                                                                                     |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.                                                                                   |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** имеет [**роль \_ System \_ статиктекст**](object-roles.md).                                                                                                                                                                                             |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): системная система состояний с состоянием " [**\_ \_ только для чтения**](object-state-constants.md) " \| [**\_ \_ невидима**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Примечания

-   Метод [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) Возвращает отображаемое значение \_ E \_ мембернотфаунд при вызове с помощью [**селфлаг \_ такефокус**](selflag.md) для статического текстового объекта.
-   Статические элементы управления с \_ стилем значка SS возвращают недопустимые данные в свойстве **Name** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





