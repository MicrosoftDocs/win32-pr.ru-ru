---
title: Элемент управления ДЕФПУШБУТТОН
description: Определяет элемент управления принудительной кнопки по умолчанию.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Меню элементов управления ДЕФПУШБУТТОН и другие ресурсы
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672239"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="a4e86-104">Элемент управления ДЕФПУШБУТТОН</span><span class="sxs-lookup"><span data-stu-id="a4e86-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="a4e86-105">Определяет элемент управления принудительной кнопки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4e86-105">Defines a default push-button control.</span></span> <span data-ttu-id="a4e86-106">Элемент управления является небольшим прямоугольником с полужирным контуром, представляющим ответ по умолчанию для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4e86-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="a4e86-107">Заданный текст отображается внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="a4e86-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="a4e86-108">Элемент управления выделяет кнопку обычным образом, когда пользователь нажимает на нее указатель мыши и отправляет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="a4e86-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a4e86-109"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="a4e86-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="a4e86-110">Текст, который должен быть центрирован в прямоугольной области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a4e86-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="a4e86-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="a4e86-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a4e86-112">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a4e86-112">Control styles.</span></span> <span data-ttu-id="a4e86-113">Это значение может быть сочетанием следующих стилей: **BS \_ дефпушбуттон**, **WS \_ TABSTOP**, **WS \_ Group** и **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="a4e86-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="a4e86-114">Если стиль не указан, используется стиль по умолчанию `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="a4e86-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="a4e86-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4e86-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4e86-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="a4e86-116">Examples</span></span>

<span data-ttu-id="a4e86-117">В этом примере определяется элемент управления принудительной кнопки по умолчанию, помеченный как Cancel:</span><span class="sxs-lookup"><span data-stu-id="a4e86-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="a4e86-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4e86-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e86-119">Кнопки Push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="a4e86-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="a4e86-120">**PUSHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="a4e86-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="a4e86-121">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="a4e86-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




