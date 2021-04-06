---
description: Контролевентс аналогичны сообщениям Microsoft Windows в приложениях на основе Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Обзор таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913083"
---
# <a name="controlevent-overview"></a>Обзор таблице ControlEvent событие

Контролевентс аналогичны сообщениям Microsoft Windows в приложениях на основе Win32. Однако вместо того, чтобы создавать функцию обратного вызова для получения сообщений Windows и отправки сообщений Windows с помощью функции [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , установщик пользовательского интерфейса и элементы управления публикуют [контролевентс](control-events.md). Другие элементы управления и установщик можно указать для подписки на определенные Контролевентс, которые затем будут изменять атрибуты элемента управления подписки. Чтобы добавить рабочие элементы управления в диалоговые окна, автор пользовательского интерфейса определяет публикацию Контролевентс в [таблице таблице ControlEvent событие](controlevent-table.md) и подписывает элементы управления в контролевентс в [таблице таблица eventmapping](eventmapping-table.md).

Установщик опубликует следующие события для подписки на элементы управления, перечисленные в [таблице таблица eventmapping](eventmapping-table.md). [Элемент управления ProgressBar](progressbar-control.md) или [элемент управления "объявление](billboard-control.md) " обычно подписывается на сетпрогресс, а остальные подписываются [элементами управления "текст](text-control.md)".

[Актиондата таблице ControlEvent событие](actiondata-controlevent.md)

[Актионтекст таблице ControlEvent событие](actiontext-controlevent.md)

[Сетпрогресс таблице ControlEvent событие](setprogress-controlevent.md)

[TimeRemaining таблице ControlEvent событие](timeremaining-controlevent.md)

[Скриптинпрогресс таблице ControlEvent событие](scriptinprogress-controlevent.md)

Следующие события публикуются элементом управления при перемещении выбора элементов в элемент управления [селектионтри](selectiontree-control.md) или [директорилист](directorylist-control.md). Элементы управления подписки должны находиться в одном и том же диалоговом окне и перечислены в таблице таблица eventmapping.

[Игноречанже таблице ControlEvent событие](ignorechange-controlevent.md)

[Селектиондескриптион таблице ControlEvent событие](selectiondescription-controlevent.md)

[Селектионсизе таблице ControlEvent событие](selectionsize-controlevent.md)

[Селектионпас таблице ControlEvent событие](selectionpath-controlevent.md)

[Селектионактион таблице ControlEvent событие](selectionaction-controlevent.md)

[Селектионноитемс таблице ControlEvent событие](selectionnoitems-controlevent.md)

Следующие Контролевентс могут быть опубликованы по собственному усмотрению пользователя путем взаимодействия с [элементом управления "кнопка](pushbutton-control.md) " или ["флажок](checkbox-control.md) " в диалоговом окне. Элемент управления CheckBox может публиковать только события AddLocal, Аддсаурце, Remove, DoAction и SetProperty. С установщик Windows версиями, поставляемыми в составе Windows Server 2003 и более поздних версий, [элемент управления селектионтри](selectiontree-control.md) может публиковать DoAction, таблице ControlEvent событие и SetProperty контролевентс. Автор пользовательского интерфейса должен вывести список таблице ControlEvent событие в [таблице таблице ControlEvent событие](controlevent-table.md). Обработчик пользовательского интерфейса установщика — это подписчик на эти события.

[AddLocal таблице ControlEvent событие](addlocal-controlevent.md)

[Аддсаурце таблице ControlEvent событие](addsource-controlevent.md)

[Чеккексистингтаржетпас таблице ControlEvent событие](checkexistingtargetpath-controlevent.md)

[Чекктаржетпас таблице ControlEvent событие](checktargetpath-controlevent.md)

[DoAction таблице ControlEvent событие](doaction-controlevent.md)

[Енаблероллбакк таблице ControlEvent событие](enablerollback-controlevent.md)

[EndDialog таблице ControlEvent событие](enddialog-controlevent.md)

[Невдиалог таблице ControlEvent событие](newdialog-controlevent.md)

[Повторная установка таблице ControlEvent событие](reinstall-controlevent.md)

[ReinstallMode таблице ControlEvent событие](reinstallmode-controlevent.md)

[Удалить таблице ControlEvent событие](remove-controlevent.md)

[Сбросить таблице ControlEvent событие](reset-controlevent.md)

[Сетинсталллевел таблице ControlEvent событие](setinstalllevel-controlevent.md)

[SetProperty таблице ControlEvent событие](setproperty-controlevent.md)

[Сеттаржетпас таблице ControlEvent событие](settargetpath-controlevent.md)

[Спавндиалог таблице ControlEvent событие](spawndialog-controlevent.md)

[Спавнваитдиалог таблице ControlEvent событие](spawnwaitdialog-controlevent.md)

[Валидатепродуктид таблице ControlEvent событие](validateproductid-controlevent.md)

[Элемент управления "кнопка](pushbutton-control.md) " может публиковать следующие события в подписке [элемента управления селектионтри](selectiontree-control.md) или [элементе управления директорилист](directorylist-control.md) , расположенном в том же диалоговом окне. Элемент управления "Кнопка" должен быть указан в таблице таблице ControlEvent событие, а элементы управления подписки должны присутствовать в таблице таблица eventmapping.

[Селектионбровсе таблице ControlEvent событие](selectionbrowse-controlevent.md)

[Директорилиступ таблице ControlEvent событие](directorylistup-controlevent.md)

[Директорилистнев таблице ControlEvent событие](directorylistnew-controlevent.md)

[Директорилистопен таблице ControlEvent событие](directorylistopen-controlevent.md)

Для событий элемента управления обычно требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) . Большинство Контролевентс не будут работать с [*меньшим пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md) пользователя, поскольку на этих уровнях отображаются только немодальные диалоговые окна. События Актионтекст, Аддсаурце, Сетпрогресс, TimeRemaining и Скриптинпрогресс являются исключениями и будут работать в сокращенном или базовом пользовательском интерфейсе. Дополнительные сведения об уровнях ПОЛЬЗОВАТЕЛЬСКОГО интерфейса см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

Для выполнения [настраиваемых действий](custom-actions.md) можно опубликовать таблице ControlEvent событие из [элемента управления "кнопка](pushbutton-control.md) [" или "флажок"](checkbox-control.md). Добавьте запись в [таблицу таблице ControlEvent событие](controlevent-table.md) с именами диалогового окна и элементом управления, публикующий таблице ControlEvent событие. Этот элемент управления должен публиковать [DoAction таблице ControlEvent событие](doaction-controlevent.md) , уведомляя установщик о необходимости запуска настраиваемого действия. В Windows XP или более ранних системах нельзя выполнить пользовательское действие путем публикации таблице ControlEvent событие из [элемента управления селектионтри](selectiontree-control.md).

Дополнительные сведения о конкретных Контролевентс см. в списке стандартных [контролевентс](control-events.md) в [справочнике по пользовательскому интерфейсу](user-interface-reference.md).

 

 
