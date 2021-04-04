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
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a><span data-ttu-id="c39f2-103">Смещение нажатия кнопки мыши X в позиции курсора</span><span class="sxs-lookup"><span data-stu-id="c39f2-103">Translating Mouse Hit X Offset to Caret Position</span></span>

<span data-ttu-id="c39f2-104">В соответствии с соглашением пользователь может выбрать знак позиции курсора (CP), щелкнув конечную половину символа "CP-1" или начальную половину символа "CP".</span><span class="sxs-lookup"><span data-stu-id="c39f2-104">Conventionally, the user can select caret position (cp) by clicking either the trailing half of character "cp-1" or the leading half of character "cp".</span></span> <span data-ttu-id="c39f2-105">Приложение может реализовать перевод смещения курсора мыши x в позиции курсора следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c39f2-105">An application can implement the translation of mouse hit x offset to caret position as follows:</span></span>


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



<span data-ttu-id="c39f2-106">Для скриптов, которые привязывают курсор к границам кластера, вызов [**скрипткстокп**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) возвращает параметру *фтраилинг* значение 0 или ширину кластера в кодовых позициях.</span><span class="sxs-lookup"><span data-stu-id="c39f2-106">For scripts that snap the caret to cluster boundaries, a call to [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns with *fTrailing* set to either 0 or the width of the cluster in code points.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c39f2-107">См. также</span><span class="sxs-lookup"><span data-stu-id="c39f2-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c39f2-108">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="c39f2-108">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



