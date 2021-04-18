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
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="dcc0b-104">Несовместимые атрибуты элемента управления диапазона ARIA</span><span class="sxs-lookup"><span data-stu-id="dcc0b-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="dcc0b-105">Текст</span><span class="sxs-lookup"><span data-stu-id="dcc0b-105">Text</span></span>

<span data-ttu-id="dcc0b-106">Элемент имеет роль **ProgressBar** или **Slider** , но предоставленное значение **ARIA-валуенов** находится вне диапазона **ARIA-валуемин** **ARIA-валуемакс** .</span><span class="sxs-lookup"><span data-stu-id="dcc0b-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="dcc0b-107">Тип</span><span class="sxs-lookup"><span data-stu-id="dcc0b-107">Type</span></span>

<span data-ttu-id="dcc0b-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="dcc0b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="dcc0b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dcc0b-109">Description</span></span>

<span data-ttu-id="dcc0b-110">Эта ошибка применяется к элементам, у которых [**роль**](https://developer.mozilla.org/docs/Web/HTML/Reference) (неявная или явная) равна **ProgressBar**, **Slider** или **спинбуттон**.</span><span class="sxs-lookup"><span data-stu-id="dcc0b-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="dcc0b-111">Эта ошибка означает, что предоставленное значение [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) не находится в диапазоне, определенном атрибутами [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="dcc0b-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="dcc0b-112">Чтобы устранить эту ошибку, проверьте свою реализацию, чтобы убедиться, что атрибуты [**ARIA-валуемин**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) и [**ARIA-валуемакс**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) заданы правильно, а значение атрибута [**ARIA-валуенов**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) должно поддерживаться правильно.</span><span class="sxs-lookup"><span data-stu-id="dcc0b-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcc0b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="dcc0b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc0b-114">Отсутствуют атрибуты элемента управления диапазона ARIA</span><span class="sxs-lookup"><span data-stu-id="dcc0b-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




