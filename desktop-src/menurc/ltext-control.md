---
title: Элемент управления ЛТЕКСТ
description: Определяет элемент управления "текст, выравниваемая влево".
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Меню элементов управления ЛТЕКСТ и другие ресурсы
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105654309"
---
# <a name="ltext-control"></a><span data-ttu-id="b8e21-104">Элемент управления ЛТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="b8e21-104">LTEXT control</span></span>

<span data-ttu-id="b8e21-105">Определяет элемент управления "текст, выравниваемая влево".</span><span class="sxs-lookup"><span data-stu-id="b8e21-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="b8e21-106">Элемент управления — это простой прямоугольник, который отображает заданный текст по левому краю прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b8e21-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="b8e21-107">Перед отображением текст форматируется.</span><span class="sxs-lookup"><span data-stu-id="b8e21-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="b8e21-108">Слова, которые будут расширяться после конца строки, автоматически упаковываются в начало следующей строки.</span><span class="sxs-lookup"><span data-stu-id="b8e21-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="b8e21-109">Слова, длина которых превышает ширину элемента управления, усекаются.</span><span class="sxs-lookup"><span data-stu-id="b8e21-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="b8e21-110">Инструкция **лтекст** , которая может использоваться только в операторе [**диаложекс**](dialogex-resource.md) , определяет текст, идентификатор, измерения и атрибуты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b8e21-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b8e21-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="b8e21-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b8e21-112">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b8e21-112">Control styles.</span></span> <span data-ttu-id="b8e21-113">Это значение может быть любым сочетанием стиля **« \_ переключатель BS** » и следующими стилями **: \_ SS Left**, **WS \_ TABSTOP** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="b8e21-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="b8e21-114">Если стиль не указан, используется стиль по умолчанию `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="b8e21-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="b8e21-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b8e21-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8e21-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8e21-116">Examples</span></span>

<span data-ttu-id="b8e21-117">В этом примере определяется элемент управления "текст с именем, выравниваемая по левому краю" с именем filename:</span><span class="sxs-lookup"><span data-stu-id="b8e21-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="b8e21-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8e21-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e21-119">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="b8e21-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b8e21-120">**СТОЛБЕЦ CTEXT**</span><span class="sxs-lookup"><span data-stu-id="b8e21-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="b8e21-121">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="b8e21-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="b8e21-122">**ртекст**</span><span class="sxs-lookup"><span data-stu-id="b8e21-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 