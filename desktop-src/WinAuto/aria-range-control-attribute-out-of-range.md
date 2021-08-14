---
title: Несовместимые атрибуты элемента управления диапазона ARIA
description: Несовместимые атрибуты элемента управления диапазона ARIA
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- ариаранжеконтролаттрибутесинкомпатиблеид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326756"
---
# <a name="aria-range-control-attributes-incompatible"></a>Несовместимые атрибуты элемента управления диапазона ARIA

## <a name="text"></a>Текст

Элемент имеет роль **ProgressBar** или **Slider** , но предоставленное значение **ARIA-валуенов** находится вне диапазона **ARIA-валуемин** **ARIA-валуемакс** .

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, у которых [**роль**](https://developer.mozilla.org/docs/Web/HTML/Reference) (неявная или явная) равна **ProgressBar**, **Slider** или **спинбуттон**.

Эта ошибка означает, что предоставленное значение [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) не находится в диапазоне, определенном атрибутами [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Чтобы устранить эту ошибку, проверьте свою реализацию, чтобы убедиться, что атрибуты [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) заданы правильно, а значение атрибута [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) должно поддерживаться правильно.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отсутствуют атрибуты элемента управления диапазона ARIA](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




