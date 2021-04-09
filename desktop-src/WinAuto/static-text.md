---
title: Статический текст (Справочник по элементам пользовательского интерфейса MSAA)
description: Элементы управления "статический текст" предоставляют удобный способ для вывода текста в диалоговых окнах и других окнах. Статические текстовые элементы управления часто служат метками для других элементов управления.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889095"
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



| Свойство                                                                             | Комментарии                                                                                                                                                                                                                                                                                      |
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





