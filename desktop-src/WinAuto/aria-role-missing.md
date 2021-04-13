---
title: Ошибка роли ARIA для элементов с обработчиками событий
description: Ошибка роли ARIA для элементов с обработчиками событий
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- ариаконтаинерролиррормессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104414013"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Ошибка роли ARIA для элементов с обработчиками событий

## <a name="text"></a>Текст

Элемент имеет обработчик событий, но допустимая роль ожидать-ARIA не определена.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка относится к элементам, у которых нет неявной роли веб-приложений с широкими возможностями доступа к Интернету (ожидать-ARIA).

Эта ошибка означает, что элемент имеет обработчик событий мыши или клавиатуры (щелчок, кнопка " **вниз****", "** **MouseUp**", " **Перемещение**", " **указатель мыши** **", "** **KeyUp**", " **вниз**" или " **Нажатие клавиши**"), но не имеет атрибута [**роли**](https://developer.mozilla.org/docs/Web/HTML/Reference) и не является одним из тегов HTML с неявной ролью ожидать-Aria ( **например,** **кнопка**, **img**, **input**, **SELECT** и т

Задание атрибута [**роли**](https://developer.mozilla.org/docs/Web/HTML/Reference) для интерактивных элементов, не имеющих неявной роли (например, тега **div** ), необходимо для предоставления шаблонов поведения элемента средствам чтения с экрана и другим вспомогательным технологиям.

Чтобы устранить эту ошибку, присвойте атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) допустимую роль ожидать-ARIA, которая лучше подходит для шаблонов поведения этого элемента и необходимых атрибутов. Например, если тег **div** выступает в качестве кнопки, задайте для атрибута role значение "Button".

## <a name="example"></a>Пример


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




