---
description: В соответствии с соглашением, пользователь может выбрать точку вставки (CP), щелкнув конечную половину символа &\# 0034; CP-1&\# 0034; или начальную половину символа &\# 0034; CP&\# 0034;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Смещение нажатия кнопки мыши X в позиции курсора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910103"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Смещение нажатия кнопки мыши X в позиции курсора

В соответствии с соглашением пользователь может выбрать знак позиции курсора (CP), щелкнув конечную половину символа "CP-1" или начальную половину символа "CP". Приложение может реализовать перевод смещения курсора мыши x в позиции курсора следующим образом:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Для скриптов, которые привязывают курсор к границам кластера, вызов [**скрипткстокп**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) возвращает параметру *фтраилинг* значение 0 или ширину кластера в кодовых позициях.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



