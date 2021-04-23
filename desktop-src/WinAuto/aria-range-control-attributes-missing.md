---
title: Отсутствуют атрибуты элемента управления диапазона ARIA
description: Отсутствуют атрибуты элемента управления диапазона ARIA
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- ариаранжеконтролаттрибутесабсентид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104070789"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="586d3-104">Отсутствуют атрибуты элемента управления диапазона ARIA</span><span class="sxs-lookup"><span data-stu-id="586d3-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="586d3-105">Текст</span><span class="sxs-lookup"><span data-stu-id="586d3-105">Text</span></span>

<span data-ttu-id="586d3-106">Элемент имеет роль **ProgressBar** или **Slider** , но не предоставляет соответствующие атрибуты **ARIA-валуемин** , **ARIA-валуемакс** и **ARIA-валуенов** .</span><span class="sxs-lookup"><span data-stu-id="586d3-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="586d3-107">Тип</span><span class="sxs-lookup"><span data-stu-id="586d3-107">Type</span></span>

<span data-ttu-id="586d3-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="586d3-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="586d3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="586d3-109">Description</span></span>

<span data-ttu-id="586d3-110">Эта ошибка применяется к элементам, которые имеют [**роль**](https://developer.mozilla.org/docs/Web/HTML/Reference) (неявный или явный), равную **ProgressBar**, **Slider** или **спинбуттон**.</span><span class="sxs-lookup"><span data-stu-id="586d3-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="586d3-111">В соответствии со спецификацией специальных возможностей веб-приложений для Интернета (ожидать-ARIA), элементы, имеющие роль **ProgressBar**, **ползунка** или **спинбуттон** , должны предоставлять атрибуты [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)и [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="586d3-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="586d3-112">Чтобы устранить эту ошибку, задайте атрибуты [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)и [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и динамически сохраняйте значение **ARIA-валуенов** , чтобы обеспечить доступ к текущему значению.</span><span class="sxs-lookup"><span data-stu-id="586d3-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="586d3-113">Кроме того, необходимо задать атрибут [**ARIA-валуетекст**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) , чтобы добавить дополнительное значение к предоставленному значению **ARIA-валуенов** .</span><span class="sxs-lookup"><span data-stu-id="586d3-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="586d3-114">Пример</span><span class="sxs-lookup"><span data-stu-id="586d3-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="586d3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="586d3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="586d3-116">Несовместимые атрибуты элемента управления диапазона ARIA</span><span class="sxs-lookup"><span data-stu-id="586d3-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




