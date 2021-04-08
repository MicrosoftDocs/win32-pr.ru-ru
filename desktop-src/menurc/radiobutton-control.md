---
title: Элемент управления RADIOBUTTON
description: Определяет элемент управления "переключатель".
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Меню элементов управления RADIOBUTTON и другие ресурсы
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070003"
---
# <a name="radiobutton-control"></a><span data-ttu-id="b4344-104">Элемент управления RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="b4344-104">RADIOBUTTON control</span></span>

<span data-ttu-id="b4344-105">Определяет элемент управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="b4344-105">Defines a radio-button control.</span></span> <span data-ttu-id="b4344-106">Элемент управления представляет собой небольшой круг с текстом, который отображается рядом с ним, как правило, справа.</span><span class="sxs-lookup"><span data-stu-id="b4344-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="b4344-107">Элемент управления выделяет окружность и отправляет сообщение родительскому окну, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="b4344-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="b4344-108">Элемент управления удаляет выделение и отправляет сообщение при следующем выборе кнопки.</span><span class="sxs-lookup"><span data-stu-id="b4344-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b4344-109"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="b4344-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b4344-110">Стили для переключателя, которые могут быть сочетанием стилей классов кнопок и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="b4344-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="b4344-111">Если стиль не указан, используется стиль по умолчанию `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="b4344-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="b4344-112">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b4344-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b4344-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="b4344-113">Examples</span></span>

<span data-ttu-id="b4344-114">В следующем примере демонстрируется использование оператора **RADIOBUTTON** :</span><span class="sxs-lookup"><span data-stu-id="b4344-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="b4344-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4344-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4344-116">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="b4344-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="b4344-117">Переключатели</span><span class="sxs-lookup"><span data-stu-id="b4344-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 