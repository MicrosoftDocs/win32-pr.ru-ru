---
title: Элемент управления ПУШБОКС
description: Определяет элемент управления "флажок", который идентичен кнопке, за исключением того, что он не отображает поверхность или кадр кнопки. отображается только текст.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Меню элементов управления ПУШБОКС и другие ресурсы
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3e81e11c7d9a87c4f5501b114ef77cdb88b07
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133154"
---
# <a name="pushbox-control"></a><span data-ttu-id="0e997-104">Элемент управления ПУШБОКС</span><span class="sxs-lookup"><span data-stu-id="0e997-104">PUSHBOX control</span></span>

<span data-ttu-id="0e997-105">Определяет элемент управления "флажок", который идентичен кнопке, за исключением [**того, что**](pushbutton-control.md)он не отображает поверхность или кадр кнопки. отображается только текст.</span><span class="sxs-lookup"><span data-stu-id="0e997-105">Defines a push-box control, which is identical to a [**PUSHBUTTON**](pushbutton-control.md), except that it does not display a button face or frame; only the text appears.</span></span>

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0e997-106"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="0e997-106"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0e997-107">Стили для пушбокс, которые могут быть сочетанием стиля **BS \_ пушбокс** и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0e997-107">Styles for the pushbox, which can be a combination of the **BS\_PUSHBOX** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0e997-108">Если стиль не указан, используется стиль по умолчанию `BS_PUSHBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0e997-108">If you do not specify a style, the default style is `BS_PUSHBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0e997-109">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e997-109">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0e997-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e997-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e997-111">Кнопки Push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="0e997-111">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="0e997-112">**PUSHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="0e997-112">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> </dl>

 

 




