---
description: Событие Сетинсталллевел изменяет уровень установки на значение, заданное аргументом.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: Сетинсталллевел таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263338"
---
# <a name="setinstalllevel-controlevent"></a>Сетинсталллевел таблице ControlEvent событие

Событие Сетинсталллевел изменяет уровень установки на значение, заданное аргументом.

Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md)" или [элемента управления селектионтри](selectiontree-control.md). Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md).

Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) . Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md). Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

## <a name="published-by"></a>Кем опубликовано

Этот таблице ControlEvent событие публикуется установщиком.

## <a name="argument"></a>Аргумент

Целое число, которое является новым значением уровня установки.

## <a name="action-on-subscribers"></a>Действие на подписчиках

Нет.

## <a name="typical-use"></a>Типичные случаи использования

Элемент управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) для изменения уровня установки.

 

 



