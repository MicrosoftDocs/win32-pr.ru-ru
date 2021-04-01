---
title: Ошибка роли контейнера ARIA
description: Ошибка роли контейнера ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- ариаконтаинерролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986784"
---
# <a name="aria-container-role-error"></a>Ошибка роли контейнера ARIA

## <a name="text"></a>Текст

Элемент с определенным " **Active-Descendants** " не имеет роли контейнера (**ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **дерево**, **контекстное**, **таблист**, **строка**).

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, имеющим атрибут **ARIA-активедесцендант** .

Элемент выглядит как контейнер с установленным атрибутом **ARIA-активедесцендант** , но атрибут Role элемента не имеет значения, допустимого для контейнера.

Чтобы устранить эту ошибку, установите атрибут **Role** в качестве значения роли "веб-приложения со специальными возможностями" (ожидать-ARIA), допустимого для элемента контейнера: **ComboBox**, **Grid**, **ListBox**, **меню**, **MenuBar**, **RadioGroup**, **таблист**, **Tree** или **контекстное**.

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

[Ошибка роли ARIA](aria-role-invalid.md)
</dt> </dl>

 

 




