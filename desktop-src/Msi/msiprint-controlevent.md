---
description: Это событие публикуется элементом управления Скроллаблетекст, чтобы позволить пользователю распечатать содержимое этого элемента управления.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: Мсипринт таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913263"
---
# <a name="msiprint-controlevent"></a>Мсипринт таблице ControlEvent событие

Это событие публикуется [элементом управления скроллаблетекст](scrollabletext-control.md) , чтобы позволить пользователю распечатать содержимое этого элемента управления.

**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. Этот таблице ControlEvent событие доступен начиная с установщик Windows 5,0.

На это событие следует подписывать [элемент управления "кнопка](pushbutton-control.md) ", расположенный в том же диалоговом окне, что и [элемент управления скроллаблетекст](scrollabletext-control.md). Семсипринт таблице ControlEvent событие должен быть создан в [таблице таблице ControlEvent событие](controlevent-table.md).

## <a name="published-by"></a>Кем опубликовано

[скроллаблетекст](scrollabletext-control.md)

## <a name="argument"></a>Аргумент

В этом таблице ControlEvent событие не используется аргумент.

## <a name="action-on-subscribers"></a>Действие на подписчиках

Эта таблице ControlEvent событие не выполняет никаких действий с подписчиками.

## <a name="typical-use"></a>Типичные случаи использования

Элемент управления " [кнопка](pushbutton-control.md) " в том же диалоговом окне, что и [элемент управления скроллаблетекст](scrollabletext-control.md) , может использоваться для отображения модального диалогового окна, позволяющего пользователю распечатать содержимое элемента управления скроллаблетекст.

 

 



