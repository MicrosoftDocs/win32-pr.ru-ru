---
description: Позволяет автору указать режим проверки или режимы во время повторной установки, а также пока работает текущее диалоговое окно.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650778"
---
# <a name="reinstallmode-controlevent"></a>ReinstallMode таблице ControlEvent событие

ReinstallMode Контролевенталловс автора, чтобы указать режим или режимы проверки во время повторной установки, а также пока работает текущее диалоговое окно.

Это событие можно опубликовать с помощью [элемента управления "кнопка](pushbutton-control.md) " или [элемента управления селектионтри](selectiontree-control.md). Это событие должно быть создано в [таблице таблице ControlEvent событие](controlevent-table.md)и требует запуска пользовательского интерфейса на [*полном уровне пользовательского интерфейса*](f-gly.md) . Это событие не работает с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md). Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

## <a name="published-by"></a>Кем опубликовано

Этот таблице ControlEvent событие публикуется установщиком.

## <a name="argument"></a>Аргумент

Строка. Список возможных значений см. в разделе свойство [**REINSTALLMODE**](reinstallmode.md) .

## <a name="action-on-subscribers"></a>Действие на подписчиках

Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.

## <a name="typical-use"></a>Типичные случаи использования

Это событие связано с элементом управления " [кнопка](pushbutton-control.md) " в модальном диалоговом окне. Один и тот же элемент управления " [кнопка](pushbutton-control.md) " также должен быть связан с [переустановкой](reinstall-controlevent.md) таблице ControlEvent событие.

 

 



