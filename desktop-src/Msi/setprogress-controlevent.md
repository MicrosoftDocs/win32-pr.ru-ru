---
description: Установщик использует событие Сетпрогресс для публикации информации о ходе установки.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: Сетпрогресс таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625084"
---
# <a name="setprogress-controlevent"></a>Сетпрогресс таблице ControlEvent событие

Установщик использует событие Сетпрогресс для публикации информации о ходе установки. [Элемент управления ProgressBar](progressbar-control.md) или [элемент управления "объявление](billboard-control.md) " должен подписываться на событие через [таблицу таблица eventmapping](eventmapping-table.md) , присваивая имя действия, ход выполнения которого указывается. Это событие должно быть создано в [таблице таблица eventmapping](eventmapping-table.md).

Этот таблице ControlEvent событие может обрабатываться пользовательским интерфейсом, который работает на [*базовом интерфейсе*](b-gly.md), [*сокращенном пользовательском интерфейсе*](r-gly.md)или на [*всех уровнях пользовательского интерфейса*](f-gly.md) . Сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

## <a name="published-by"></a>Кем опубликовано

Этот таблице ControlEvent событие публикуется установщиком.

## <a name="argument"></a>Аргумент

Нет.

## <a name="action-on-subscribers"></a>Действие на подписчиках

Нет.

## <a name="typical-use"></a>Типичные случаи использования

Элемент управления [ProgressBar](progressbar-control.md) в немодальном диалоговом окне подписывается на это событие с помощью атрибута [Progress](progress-control-attribute.md) для получения сведений о ходе выполнения.

 

 



