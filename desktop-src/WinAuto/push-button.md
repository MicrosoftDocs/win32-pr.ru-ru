---
title: Кнопка "Отправить" (Справочник по элементам пользовательского интерфейса MSAA)
description: Кнопка "Отправить" — это небольшой прямоугольный объект, используемый для выполнения действия. Например, кнопки ОК и отмена диалогового окна являются кнопками.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e188b58501509fd934ab6396a21beb209857661
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775491"
---
# <a name="push-button-msaa-ui-element-reference"></a>Кнопка "Отправить" (Справочник по элементам пользовательского интерфейса MSAA)

Кнопка "Отправить" — это небольшой прямоугольный объект, используемый для выполнения действия. Например, кнопки **ОК** и **Отмена** диалогового окна являются кнопками.

Имя класса окна для кнопки отправки — "Кнопка".

## <a name="iaccessible-methods"></a>Методы IAccessible

Кнопка "Отправить" поддерживает следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Метод                                                                    | Комментарии                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Метод [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) нажимает кнопку "Отправить". |
| [**акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**аккселект**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Свойства IAccessible

Кнопка "Отправить" поддерживает следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Свойство                                                                             | Комментарии                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**получить \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккчилдкаунт**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Свойство **ChildCount** имеет значение ноль или больше.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**получить \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Свойство **DefaultAction** — "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**получить \_ аккдескриптион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акккэйбоардшорткут**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Свойство **кэйбоардшорткут** — это клавиша доступа кнопки, которая представляет собой подчеркнутый символ в тексте окна кнопки. Например, "Alt + o" — это свойство **кэйбоардшорткут** для кнопки " **ОК** ".                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**получить \_ аккфокус**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акчелп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ акчелптопик**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**получить \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Свойство **Name** получается из текста окна элемента управления (или заголовка), которое отображается в кнопке отправки. Например, "ОК" — это свойство " **имя** " для кнопки " **ОК** ".                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**получить \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **Родительское** свойство является окном ( [**\_ \_ окно системы ролей**](object-roles.md) ), которое окружает элемент управления и имеет **то же имя** свойства и класса окна, что и элемент управления.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**получить \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Свойство **Role** — это [**\_ \_ кнопка системы роли**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**получить \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Свойство **State** представляет собой сочетание одного или нескольких из следующих [значений](object-state-constants.md): [**\_ \_ невидимая**](object-state-constants.md) система состояния системная система состояния \| [**\_ \_ недоступная**](object-state-constants.md) система состояний фокус системы состояния, \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ нажатая**](object-state-constants.md) системой состояния в состоянии системы \| [**\_ \_ по умолчанию**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейс IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Флажок**](check-box.md)
</dt> <dt>

[**Поле группы**](group-box.md)
</dt> <dt>

[**Переключатель**](radio-button.md)
</dt> </dl>

 

 





