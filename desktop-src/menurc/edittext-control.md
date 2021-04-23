---
title: Элемент управления EDITTEXT
description: Определяет элемент управления "поле ввода", принадлежащий классу EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Меню элементов управления EDITTEXT и другие ресурсы
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790560"
---
# <a name="edittext-control"></a><span data-ttu-id="cd279-104">Элемент управления EDITTEXT</span><span class="sxs-lookup"><span data-stu-id="cd279-104">EDITTEXT control</span></span>

<span data-ttu-id="cd279-105">Определяет элемент управления "поле ввода", принадлежащий классу EDIT.</span><span class="sxs-lookup"><span data-stu-id="cd279-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="cd279-106">Он создает прямоугольную область, в которой пользователь может вводить и редактировать текст.</span><span class="sxs-lookup"><span data-stu-id="cd279-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="cd279-107">Элемент управления отображает курсор, когда пользователь нажимает на него указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="cd279-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="cd279-108">Пользователь может использовать клавиатуру для ввода текста или редактирования существующего текста.</span><span class="sxs-lookup"><span data-stu-id="cd279-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="cd279-109">Ключи редактирования включают в себя клавиши BACKSPACE и DELETE.</span><span class="sxs-lookup"><span data-stu-id="cd279-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="cd279-110">Пользователь может также использовать мышь, чтобы выбрать символы для удаления или выбрать место для вставки новых символов.</span><span class="sxs-lookup"><span data-stu-id="cd279-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="cd279-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="cd279-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="cd279-112">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="cd279-112">Control styles.</span></span> <span data-ttu-id="cd279-113">Это значение может быть сочетанием стилей класса изменить и следующими стилями: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** и **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="cd279-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="cd279-114">Если стиль не указан, используется стиль по умолчанию `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="cd279-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="cd279-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd279-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cd279-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="cd279-116">Examples</span></span>

<span data-ttu-id="cd279-117">В следующем примере демонстрируется использование оператора **EditText** :</span><span class="sxs-lookup"><span data-stu-id="cd279-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="cd279-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd279-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd279-119">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="cd279-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 