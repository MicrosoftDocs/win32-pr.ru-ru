---
title: Элемент управления РТЕКСТ
description: Определяет элемент управления текстом, выравниваемая по правому краю.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Меню элементов управления РТЕКСТ и другие ресурсы
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487709"
---
# <a name="rtext-control"></a><span data-ttu-id="8d5ce-104">Элемент управления РТЕКСТ</span><span class="sxs-lookup"><span data-stu-id="8d5ce-104">RTEXT control</span></span>

<span data-ttu-id="8d5ce-105">Определяет элемент управления текстом, выравниваемая по правому краю.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="8d5ce-106">Элемент управления — это простой прямоугольник, который отображает заданный текст по правому краю прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="8d5ce-107">Перед отображением текст форматируется.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="8d5ce-108">Слова, которые будут расширяться после конца строки, автоматически упаковываются в начало следующей строки.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="8d5ce-109">Слова, длина которых превышает ширину элемента управления, усекаются.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="8d5ce-110">Инструкция **ртекст** , которая может использоваться только в операторе [**диаложекс**](dialogex-resource.md) , определяет текст, идентификатор, измерения и атрибуты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="8d5ce-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="8d5ce-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="8d5ce-112">Стили для элемента управления "текст", которые могут быть любым сочетанием следующих элементов: **WS \_ TABSTOP** и **WS \_**.</span><span class="sxs-lookup"><span data-stu-id="8d5ce-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="8d5ce-113">Если стиль не указан, используется стиль по умолчанию `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="8d5ce-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="8d5ce-114">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8d5ce-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8d5ce-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="8d5ce-115">Examples</span></span>

<span data-ttu-id="8d5ce-116">В следующем примере демонстрируется использование оператора **ртекст** :</span><span class="sxs-lookup"><span data-stu-id="8d5ce-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="8d5ce-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d5ce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5ce-118">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="8d5ce-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="8d5ce-119">**СТОЛБЕЦ CTEXT**</span><span class="sxs-lookup"><span data-stu-id="8d5ce-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="8d5ce-120">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="8d5ce-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="8d5ce-121">**лтекст**</span><span class="sxs-lookup"><span data-stu-id="8d5ce-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 