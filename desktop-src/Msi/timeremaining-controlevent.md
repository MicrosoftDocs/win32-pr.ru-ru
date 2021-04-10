---
description: Установщик использует событие TimeRemaining для публикации приблизительного оставшегося времени в секундах для текущей последовательности хода выполнения.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081440"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining таблице ControlEvent событие

Установщик использует событие TimeRemaining для публикации приблизительного оставшегося времени в секундах для текущей последовательности хода выполнения. Оставшееся время может отображаться в диалоговом окне с помощью [элемента управления "текст](text-control.md) ", который подписывается на этот таблице ControlEvent событие. Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).

Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) . Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

## <a name="published-by"></a>Кем опубликовано

Этот таблице ControlEvent событие публикуется установщиком.

## <a name="argument"></a>Аргумент

Нет.

## <a name="action-on-subscribers"></a>Действие на подписчиках

Нет.

## <a name="typical-use"></a>Типичные случаи использования

[Элемент управления "текст](text-control.md) " в немодальном диалоговом окне подписывается на это событие через [таблицу таблица eventmapping](eventmapping-table.md) и использует [атрибут TimeRemaining](timeremaining-control-attribute.md) для просмотра оставшегося времени.

Тот же элемент управления текстом, который подписывается на TimeRemaining таблице ControlEvent событие, может также подписываться на [Скриптинпрогресс таблице ControlEvent событие](scriptinprogress-controlevent.md). В этом случае в качестве предварительной строки сообщения Скриптинпрогресс она заменяется строкой "оставшееся время: XX минут".

 

 



