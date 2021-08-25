---
description: в таблице таблица eventmapping перечислены элементы управления, которые подписываются на некоторые события элемента управления, а также список изменяемых атрибутов при публикации события другим элементом управления или установщик Windows.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Таблица Таблица eventmapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963114"
---
# <a name="eventmapping-table"></a>Таблица Таблица eventmapping

в таблице таблица eventmapping перечислены элементы управления, которые подписываются на некоторые события элемента управления, а также список изменяемых атрибутов при публикации события другим элементом управления или установщик Windows.

Таблица Таблица eventmapping содержит следующие столбцы.



| Столбец    | Type                         | Ключ | Допускает значения NULL |
|-----------|------------------------------|-----|----------|
| Диалог\_  | [Идентификатор](identifier.md) | Д   | Нет        |
| элементом управления\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| Событие     | [Идентификатор](identifier.md) | Д   | Нет        |
| attribute | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Откроется\_
</dt> <dd>

Внешний ключ к первому столбцу [диалоговой таблицы](dialog-table.md). Это поле и поле элемента управления \_ вместе определяют элемент управления.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Элемента\_
</dt> <dd>

Внешний ключ ко второму столбцу [управляющей таблицы](control-table.md). Это поле и поле диалога \_ вместе определяют элемент управления.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале
</dt> <dd>

Это поле представляет собой идентификатор, указывающий тип события, на которое подписан элемент управления. Дополнительные сведения см. в разделе [таблице ControlEvent событие Overview](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию
</dt> <dd>

Имя атрибута элемента управления \_ , заданное при получении события в столбце событий. Аргумент события передается в качестве аргумента вызова атрибута для изменения этого атрибута элемента управления.

</dd> </dl>

## <a name="remarks"></a>Remarks

В [таблице таблице ControlEvent событие](controlevent-table.md) указываются события элемента управления, которые запускаются, когда пользователь взаимодействует с элементом [управления "кнопка](pushbutton-control.md) [", элементом управления CheckBox](checkbox-control.md)или [элементом управления селектионтри](selectiontree-control.md). Это единственные элементы управления, которые пользователь может использовать для инициации событий элемента управления.

Несколько элементов управления в диалоговом окне могут подписываться на одно и то же событие.

В следующем списке перечислены типичные варианты использования таблицы таблица eventmapping.

-   чтобы подписывать [элемент управления Text](text-control.md) на [актионтекст таблице controlevent событие](actiontext-controlevent.md), [актиондата таблице controlevent событие](actiondata-controlevent.md), [скриптинпрогресс таблице controlevent событие](scriptinprogress-controlevent.md) или [TimeRemaining таблице controlevent событие](timeremaining-controlevent.md) , опубликованных установщик Windows.
-   Для подписки [элемента управления ProgressBar](progressbar-control.md) или [элемента управления объявлением](billboard-control.md) на [сетпрогресс таблице ControlEvent событие](setprogress-controlevent.md).
-   Для подписки [элемента управления директорикомбо](directorycombo-control.md) на [игноречанже таблице ControlEvent событие](ignorechange-controlevent.md).
-   Для автоматического отключения [элемента управления "кнопка](pushbutton-control.md) ", расположенного в том же диалоговом окне с [элементом управления селектионтри](selectiontree-control.md). Чтобы отключить кнопку "Отправить", если в [элементе управления селектионтри](selectiontree-control.md)не указаны какие-либо функции, используйте таблицу таблица eventmapping для подписки элемента управления "Кнопка" на [селектионноитемс таблице ControlEvent событие](selectionnoitems-controlevent.md). Введите **включить** в поле атрибуты таблицы таблица eventmapping.
-   Для отображения [текстового элемента управления](text-control.md) , отображающего путь к расположению установки компонента, выбранного в [элементе управления селектионтри](selectiontree-control.md) в том же диалоговом окне. Используйте таблицу таблица eventmapping для подписки [элемента управления Text](text-control.md) на [Селектионпасон таблице ControlEvent событие](selectionpathon-controlevent.md) и [Селектионпас таблице ControlEvent событие](selectionpath-controlevent.md) , опубликованные [элементом управления селектионтри](selectiontree-control.md).
-   Чтобы отобразить [элемент управления "текст](text-control.md) ", в котором отображается описание элемента, выделенного в элементе [управления селектионтри](selectiontree-control.md) , расположенном в том же диалоговом окне, используйте таблицу таблица eventmapping для подписки [элемента управления Text](text-control.md) на [Селектиондескриптион таблице ControlEvent событие](selectiondescription-controlevent.md), [селектионсизе таблице ControlEvent событие](selectionsize-controlevent.md) или [селектионактион таблице ControlEvent событие](selectionaction-controlevent.md). Введите **текст** в поле атрибут таблицы таблица eventmapping.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



