---
title: Ошибка TabIndex контейнера ARIA
description: Ошибка TabIndex контейнера ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- ариаконтаинертабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411315"
---
# <a name="aria-container-tabindex-error"></a>Ошибка TabIndex контейнера ARIA

## <a name="text"></a>Текст

Элемент является контейнером с фокусом, для которого определены активные потомки, но без значения **TabIndex** больше или равно 0.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют атрибут **ARIA-активедесцендант** , не отключаются и не имеют атрибута **TabIndex** , значение которого больше или равно 0. Эти элементы должны находиться в порядке табуляции, поскольку они отвечают за обработку событий клавиатуры для своих дочерних элементов.

Чтобы устранить эту ошибку, задайте для атрибута **TabIndex** значение, которое больше или равно 0.

## <a name="example"></a>Пример


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Роль контейнера ARIA (без активных потомков), ошибка TabIndex](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




