---
title: Элемент управления автоradiobutton
description: Определяет автоматический элемент управления "переключатель". Этот элемент управления автоматически выполняет взаимное исключение с другими элементами управления "автоradiobutton" в той же группе. Когда эта кнопка выбрана, приложение получает извещение о \_ нажатии млрд долл.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Меню элемента управления автоradiobutton и другие ресурсы
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783888"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="0e2b1-106">Элемент управления автоradiobutton</span><span class="sxs-lookup"><span data-stu-id="0e2b1-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="0e2b1-107">Определяет автоматический элемент управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="0e2b1-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="0e2b1-108">Этот элемент управления автоматически выполняет взаимное исключение с другими элементами управления " **автоradiobutton** " в той же группе.</span><span class="sxs-lookup"><span data-stu-id="0e2b1-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="0e2b1-109">Когда эта кнопка выбрана, приложение получает извещение о **\_ нажатии млрд долл**.</span><span class="sxs-lookup"><span data-stu-id="0e2b1-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0e2b1-110"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="0e2b1-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="0e2b1-111">Текст, который будет отображаться рядом с переключателем.</span><span class="sxs-lookup"><span data-stu-id="0e2b1-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="0e2b1-112"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="0e2b1-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0e2b1-113">Стили для автоматического переключателя, которые могут быть сочетанием стилей классов кнопок и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0e2b1-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0e2b1-114">Если стиль не указан, используется стиль по умолчанию `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0e2b1-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0e2b1-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e2b1-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0e2b1-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e2b1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e2b1-117">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="0e2b1-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0e2b1-118">Переключатели</span><span class="sxs-lookup"><span data-stu-id="0e2b1-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="0e2b1-119">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="0e2b1-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




