---
title: Ошибка ARIA TabIndex
description: Ошибка ARIA TabIndex
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- ариатабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104070793"
---
# <a name="aria-tabindex-error"></a>Ошибка ARIA TabIndex

## <a name="text"></a>Текст

Элемент не отключен и имеет обработчик событий **щелчка** , но имеет **TabIndex** < 0 и не находится в последовательности табуляции по умолчанию.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют обработчик событий щелчка и не отключены. Эти элементы должны находиться в порядке табуляции. Это гарантирует, что элемент можно будет достигнуть с помощью клавиши TAB, как обычно пользователи с программами чтения с экрана находят на пользовательский интерфейс.

Чтобы устранить эту ошибку, задайте для атрибута [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) значение, равное или больше 0. Не нужно явно задавать атрибут **TabIndex** для тегов, которые находятся в последовательности табуляции по умолчанию, [**например (с**](https://developer.mozilla.org/docs/Web/HTML/Element/a) атрибутом [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), [**кнопки**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**ввода**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (за исключением "Hidden"), [**выбора**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)и [**области**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (в составе гиперкарты).

## <a name="example"></a>Пример


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




