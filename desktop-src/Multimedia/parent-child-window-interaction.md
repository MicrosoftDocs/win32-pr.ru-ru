---
title: Взаимодействие с окном Parent-Child
description: Взаимодействие с окном Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790548"
---
# <a name="parent-child-window-interaction"></a>Взаимодействие с окном Parent-Child

Некоторые сообщения на уровне системы, такие как [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette), отправляются только в окна верхнего уровня и перекрывающихся окон. Если окно записи является дочерним окном, его родительский элемент должен пересылать эти сообщения.

Аналогично, если размер родительского окна изменится, может потребоваться отправить сообщения уведомления в окно Capture (захват). И наоборот, при изменении размера записанного видео в окне Capture может потребоваться отправить уведомления родительскому окну. Самый простой способ управления этим — всегда сохранять размеры окна захвата равными размеру захваченного видеопотока, уведомляя родительский элемент при изменении этих измерений.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Окна захвата](capture-windows.md)
</dt> </dl>

 

 