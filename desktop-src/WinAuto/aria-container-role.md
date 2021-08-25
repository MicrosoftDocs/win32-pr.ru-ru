---
title: Ошибка роли контейнера ARIA
description: Ошибка роли контейнера ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- ариаконтаинерролиррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507f094a5f7270565de0426b50afd6aef699607d857ef1ba7ed3d6c8bb1a1a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759834"
---
# <a name="aria-container-role-error"></a>Ошибка роли контейнера ARIA

## <a name="text"></a>Текст

Элемент с определенным " **Active-Descendants** " не имеет роли контейнера (**ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **дерево**, **контекстное**, **таблист**, **строка**).

## <a name="type"></a>Тип

Error

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ошибка роли ARIA](aria-role-invalid.md)
</dt> </dl>

 

 




