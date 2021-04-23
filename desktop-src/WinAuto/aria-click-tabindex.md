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
# <a name="aria-tabindex-error"></a><span data-ttu-id="0fbe8-104">Ошибка ARIA TabIndex</span><span class="sxs-lookup"><span data-stu-id="0fbe8-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="0fbe8-105">Текст</span><span class="sxs-lookup"><span data-stu-id="0fbe8-105">Text</span></span>

<span data-ttu-id="0fbe8-106">Элемент не отключен и имеет обработчик событий **щелчка** , но имеет **TabIndex** < 0 и не находится в последовательности табуляции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="0fbe8-107">Тип</span><span class="sxs-lookup"><span data-stu-id="0fbe8-107">Type</span></span>

<span data-ttu-id="0fbe8-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0fbe8-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="0fbe8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0fbe8-109">Description</span></span>

<span data-ttu-id="0fbe8-110">Эта ошибка применяется к элементам, которые имеют обработчик событий щелчка и не отключены.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="0fbe8-111">Эти элементы должны находиться в порядке табуляции.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-111">These elements must be in the tab order.</span></span> <span data-ttu-id="0fbe8-112">Это гарантирует, что элемент можно будет достигнуть с помощью клавиши TAB, как обычно пользователи с программами чтения с экрана находят на пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="0fbe8-113">Чтобы устранить эту ошибку, задайте для атрибута [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) значение, равное или больше 0.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="0fbe8-114">Не нужно явно задавать атрибут **TabIndex** для тегов, которые находятся в последовательности табуляции по умолчанию, [**например (с**](https://developer.mozilla.org/docs/Web/HTML/Element/a) атрибутом [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), [**кнопки**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**ввода**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (за исключением "Hidden"), [**выбора**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)и [**области**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (в составе гиперкарты).</span><span class="sxs-lookup"><span data-stu-id="0fbe8-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="0fbe8-115">Пример</span><span class="sxs-lookup"><span data-stu-id="0fbe8-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




