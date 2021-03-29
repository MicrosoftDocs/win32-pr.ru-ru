---
title: Переключатель (Справочник по элементу пользовательского интерфейса MSAA)
description: Переключатели используются для выбора одного из нескольких параметров, обычно в диалоговом окне.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9766e85f530281e4f843c4d39fd41fe35d4fb620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774168"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Переключатель (Справочник по элементу пользовательского интерфейса MSAA)

> [!Note]  
> В этом разделе описываются объекты **переключателей** для Справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA. Создание объектов **переключателей** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь. См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.

 

Переключатели используются для выбора одного из нескольких параметров, обычно в диалоговом окне. Переключатель содержит небольшой круг с текстом рядом с ним. Если этот флажок установлен, круговая скобка содержит закрашенный кружок. При выборе одной кнопки в наборе выделена ранее выбранная кнопка, поэтому одновременно выбирается только один из параметров набора.

Имя класса окна для переключателя — "Кнопка".

## <a name="iaccessible-methods"></a>Методы IAccessible

Переключатель поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Комментарии                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) нажимает переключатель. |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Переключатель поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Свойство **ChildCount** равно нулю.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Свойство **DefaultAction** переключателя — Check.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Свойство **кэйбоардшорткут** является ключом доступа переключателя, который является подчеркнутым символом в тексте окна элемента управления. Эта строка содержит символ клавиши доступа, добавленный к строке "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** получается из текста окна элемента управления (или заголовка), которое отображается вместе с переключателем.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** является [**\_ \_ переключателем системы роли**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): система состояния " [**\_ \_ невидимая**](object-state-constants.md) система состояния" \| [**\_ \_ недоступная**](object-state-constants.md) \| Система состояний [**\_ \_ состояние**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) системы в системе состояния<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Флажок**](check-box.md)
</dt> <dt>

[**Поле группы**](group-box.md)
</dt> <dt>

[**Кнопка "Отправить"**](push-button.md)
</dt> </dl>

 

 





