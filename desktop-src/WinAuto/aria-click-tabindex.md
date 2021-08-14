---
title: Ошибка ARIA TabIndex
description: Ошибка ARIA TabIndex
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- ариатабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1637008b6679f196f7bba0701606e0514abe44410032e1a5ffc063977ddf10e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326754"
---
# <a name="aria-tabindex-error"></a>Ошибка ARIA TabIndex

## <a name="text"></a>Текст

Элемент не отключен и имеет обработчик событий **щелчка** , но имеет **TabIndex** < 0 и не находится в последовательности табуляции по умолчанию.

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют обработчик событий щелчка и не отключены. Эти элементы должны находиться в порядке табуляции. Это гарантирует, что элемент можно будет достигнуть с помощью клавиши TAB, как обычно пользователи с программами чтения с экрана находят на пользовательский интерфейс.

Чтобы устранить эту ошибку, задайте для атрибута [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) значение, равное или больше 0. Не нужно явно задавать атрибут **TabIndex** для тегов, которые находятся в последовательности табуляции по умолчанию, [**например (с**](https://developer.mozilla.org/docs/Web/HTML/Element/a) атрибутом [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), [**кнопки**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**ввода**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (за исключением "Hidden"), [**выбора**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)и [**области**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (в составе гиперкарты).

## <a name="example"></a>Пример


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




