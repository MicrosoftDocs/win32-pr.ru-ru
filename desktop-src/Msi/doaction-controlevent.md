---
description: DoAction таблице ControlEvent событие уведомляет установщик о необходимости выполнения настраиваемого действия. Это событие может быть опубликовано элементом управления "Кнопка", элементом управления CheckBox или элементом управления Селектионтри. Это событие должно быть создано в таблице таблице ControlEvent событие.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: DoAction таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc4133c9b9fb0b312423952ee72d1e9e38defc2713345e1a7ed106fb141f0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692624"
---
# <a name="doaction-controlevent"></a>DoAction таблице ControlEvent событие

DoAction таблице ControlEvent событие уведомляет установщик о необходимости выполнения настраиваемого действия. Это событие может быть опубликовано элементом управления " [кнопка](pushbutton-control.md) ", элементом управления [CheckBox](checkbox-control.md) или элементом управления [селектионтри](selectiontree-control.md) . Это событие должно быть создано в таблице [таблице ControlEvent событие](controlevent-table.md) .

Обратите внимание, что настраиваемые действия, запускаемые DoAction таблице ControlEvent событие, могут отправить сообщение с помощью [**метода Message**](session-message.md), но не могут отправить сообщение с помощью [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). в системах до Windows Server 2003 настраиваемые действия, запускаемые DoAction таблице controlevent событие, не могут отправить сообщения с помощью метода **мсипроцессмессаже** или **message**. дополнительные сведения см. [в разделе отправка сообщений в установщик Windows с помощью мсипроцессмессаже](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Для этого таблице ControlEvent событие требуется, чтобы пользовательский интерфейс выполнялся на [*полном уровне пользовательского интерфейса*](f-gly.md) . Это событие не будет работать с [*ограниченным пользовательским*](r-gly.md) интерфейсом или [*базовым интерфейсом*](b-gly.md). Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).

## <a name="published-by"></a>Кем опубликовано

Этот таблице ControlEvent событие публикуется установщиком.

## <a name="argument"></a>Аргумент

Строка, имя настраиваемого действия, которое необходимо выполнить.

## <a name="action-on-subscribers"></a>Действие на подписчиках

Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.

## <a name="typical-use"></a>Типичные случаи использования

Элемент управления " [кнопка](pushbutton-control.md) " в диалоговом окне связан с этим событием в таблице [таблице ControlEvent событие](controlevent-table.md) для вызова настраиваемого действия.

 

 



