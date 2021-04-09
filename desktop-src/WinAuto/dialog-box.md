---
title: Диалоговое окно (Справочник по элементам пользовательского интерфейса MSAA)
description: Диалоговое окно — это временное окно, создаваемое приложением для получения вводимых пользователем данных.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791802"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Диалоговое окно (Справочник по элементам пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **диалоговых окон** для ссылок на элементы ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **диалоговых окон** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Диалоговое окно — это временное окно, создаваемое приложением для получения вводимых пользователем данных. Приложение использует диалоговые окна, чтобы запросить у пользователя дополнительные сведения о командах, выбранных пользователем из меню. Диалоговое окно содержит один или несколько элементов управления (дочерних окон), с которыми пользователь вводит текст, выбирает параметры или направляет действие команды.

Имя класса окна для диалоговых окон — " \# 32770".

## <a name="iaccessible-methods"></a>Методы IAccessible

Диалоговое окно поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Комментарии                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Если диалоговое окно содержит кнопку по умолчанию, метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) вызывает [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea) i с сообщением о нажатии кнопки [**BM \_**](/windows/desktop/Controls/bm-click) , чтобы нажать кнопку по умолчанию. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Диалоговое окно поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                                 | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | Свойство **ChildCount** равно количеству дочерних элементов управления "окно" в диалоговом окне.                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Если диалоговое окно содержит кнопку по умолчанию, свойство **DefaultAction** имеет значение "Press".                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Обычно диалоговые окна не имеют сочетаний клавиш. Если текст окна для диалогового окна содержит символ амперсанда (&), то Microsoft Active Accessibility возвращает строку, отличную от NULL, как свойство **кэйбоардшорткут** .                                                                                                                                                                                                                                        |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | Свойство **Name** — это текст окна или заголовок, который отображается в заголовке диалогового окна.                                                                                                                                                                                                                                                                                                                                                              |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | **Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает диалоговое окно и **имеет то же имя свойства и** класса окна, что и диалоговое окно.                                                                                                                                                                                                                                                        |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | Свойство **Role** является [**\_ \_ диалоговым окном системы роли**](object-roles.md) или [**\_ системой роли \_ страницу свойств**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md):[**\_ \_ невидимая**](object-state-constants.md) система состояния система состояния \| [**\_ \_ недоступна**](object-state-constants.md) система состояний, \| [**\_ \_ сфокусированная**](object-state-constants.md) на \| [**\_ \_ системе состояния**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>Комментарии

Объект диалогового окна не поддерживает метод [**Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) . Чтобы получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) на элемент управления в диалоговом окне, клиенты должны получить маркер окна элемента управления, а затем вызвать [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

