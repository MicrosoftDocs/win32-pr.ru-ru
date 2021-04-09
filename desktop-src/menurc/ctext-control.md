---
title: Элемент управления столбец CTEXT
description: Определяет элемент управления центра текста.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Меню элементов управления столбец CTEXT и другие ресурсы
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133787"
---
# <a name="ctext-control"></a><span data-ttu-id="b52ac-104">Элемент управления столбец CTEXT</span><span class="sxs-lookup"><span data-stu-id="b52ac-104">CTEXT control</span></span>

<span data-ttu-id="b52ac-105">Определяет элемент управления центра текста.</span><span class="sxs-lookup"><span data-stu-id="b52ac-105">Defines a centered-text control.</span></span> <span data-ttu-id="b52ac-106">Элемент управления — это простой прямоугольник, который отображает заданный текст в центре прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b52ac-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="b52ac-107">Перед отображением текст форматируется.</span><span class="sxs-lookup"><span data-stu-id="b52ac-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="b52ac-108">Слова, которые будут расширяться после конца строки, автоматически упаковываются в начало следующей строки.</span><span class="sxs-lookup"><span data-stu-id="b52ac-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="b52ac-109">Слова, длина которых превышает ширину элемента управления, усекаются.</span><span class="sxs-lookup"><span data-stu-id="b52ac-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="b52ac-110">Инструкция [**лтекст**](ltext-control.md) , которая может использоваться только в операторе представителя, определяет текст, идентификатор, измерения и атрибуты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b52ac-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b52ac-111"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="b52ac-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="b52ac-112">Текст, который должен быть центрирован в прямоугольной области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b52ac-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="b52ac-113"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="b52ac-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b52ac-114">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b52ac-114">Control styles.</span></span> <span data-ttu-id="b52ac-115">Это значение может быть любым сочетанием следующих стилей: **SS \_ Center**, **WS \_ TABSTOP** и **WS \_**.</span><span class="sxs-lookup"><span data-stu-id="b52ac-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="b52ac-116">Если стиль не указан, используется стиль по умолчанию `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="b52ac-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="b52ac-117">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b52ac-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b52ac-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="b52ac-118">Examples</span></span>

<span data-ttu-id="b52ac-119">В этом примере определяется центрированный текст элемента управления с именем filename:</span><span class="sxs-lookup"><span data-stu-id="b52ac-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="b52ac-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b52ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52ac-121">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="b52ac-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b52ac-122">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="b52ac-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="b52ac-123">**лтекст**</span><span class="sxs-lookup"><span data-stu-id="b52ac-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="b52ac-124">**ртекст**</span><span class="sxs-lookup"><span data-stu-id="b52ac-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 