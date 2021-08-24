---
title: Отсутствуют атрибуты элемента управления диапазона ARIA
description: Отсутствуют атрибуты элемента управления диапазона ARIA
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- ариаранжеконтролаттрибутесабсентид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645123"
---
# <a name="aria-range-control-attributes-missing"></a>Отсутствуют атрибуты элемента управления диапазона ARIA

## <a name="text"></a>Текст

Элемент имеет роль **ProgressBar** или **Slider** , но не предоставляет соответствующие атрибуты **ARIA-валуемин** , **ARIA-валуемакс** и **ARIA-валуенов** .

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют [**роль**](https://developer.mozilla.org/docs/Web/HTML/Reference) (неявный или явный), равную **ProgressBar**, **Slider** или **спинбуттон**.

В соответствии со спецификацией специальных возможностей веб-приложений для Интернета (ожидать-ARIA), элементы, имеющие роль **ProgressBar**, **ползунка** или **спинбуттон** , должны предоставлять атрибуты [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)и [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Чтобы устранить эту ошибку, задайте атрибуты [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)и [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и динамически сохраняйте значение **ARIA-валуенов** , чтобы обеспечить доступ к текущему значению. Кроме того, необходимо задать атрибут [**ARIA-валуетекст**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) , чтобы добавить дополнительное значение к предоставленному значению **ARIA-валуенов** .

## <a name="example"></a>Пример


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Несовместимые атрибуты элемента управления диапазона ARIA](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




