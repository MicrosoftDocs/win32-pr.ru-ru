---
title: Несовместимые атрибуты элемента управления диапазона ARIA
description: Несовместимые атрибуты элемента управления диапазона ARIA
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- ариаранжеконтролаттрибутесинкомпатиблеид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104533575"
---
# <a name="aria-range-control-attributes-incompatible"></a>Несовместимые атрибуты элемента управления диапазона ARIA

## <a name="text"></a>Текст

Элемент имеет роль **ProgressBar** или **Slider** , но предоставленное значение **ARIA-валуенов** находится вне диапазона **ARIA-валуемин** **ARIA-валуемакс** .

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, у которых [**роль**](https://developer.mozilla.org/docs/Web/HTML/Reference) (неявная или явная) равна **ProgressBar**, **Slider** или **спинбуттон**.

Эта ошибка означает, что предоставленное значение [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) не находится в диапазоне, определенном атрибутами [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Чтобы устранить эту ошибку, проверьте свою реализацию, чтобы убедиться, что атрибуты [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) заданы правильно, а значение атрибута [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) должно поддерживаться правильно.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отсутствуют атрибуты элемента управления диапазона ARIA](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




