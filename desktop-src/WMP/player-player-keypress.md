---
title: Событие Player. KeyPress
description: Событие KeyPress возникает при нажатии и отпускании клавиши. | Событие Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Проигрыватель Windows Media событие KeyPress
- Проигрыватель Windows Media событие KeyPress, класс Player
- Класс проигрывателя Windows Media Player, событие KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704234"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="cc63d-107">Событие Player. KeyPress</span><span class="sxs-lookup"><span data-stu-id="cc63d-107">Player.KeyPress event</span></span>

<span data-ttu-id="cc63d-108">Событие **KeyPress** возникает при нажатии и отпускании клавиши.</span><span class="sxs-lookup"><span data-stu-id="cc63d-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc63d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc63d-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="cc63d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc63d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc63d-111">*нкэйасЦии*</span><span class="sxs-lookup"><span data-stu-id="cc63d-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="cc63d-112">**Number** (**целое** число), задающее стандартный числовой код ANSI для символа.</span><span class="sxs-lookup"><span data-stu-id="cc63d-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc63d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc63d-113">Return value</span></span>

<span data-ttu-id="cc63d-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc63d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc63d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc63d-115">Remarks</span></span>

<span data-ttu-id="cc63d-116">Это событие возникает, когда нажатие клавиши приводит к вводу любого печатного символа клавиатуры, клавиши CTRL в сочетании с символом из стандартного алфавита или одного из нескольких специальных символов, а также клавишей Ввод или BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="cc63d-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="cc63d-117">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cc63d-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="cc63d-118">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="cc63d-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="cc63d-119">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cc63d-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc63d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cc63d-120">Requirements</span></span>



| <span data-ttu-id="cc63d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cc63d-121">Requirement</span></span> | <span data-ttu-id="cc63d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cc63d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc63d-123">Версия</span><span class="sxs-lookup"><span data-stu-id="cc63d-123">Version</span></span><br/> | <span data-ttu-id="cc63d-124">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cc63d-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="cc63d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cc63d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc63d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc63d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc63d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc63d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc63d-128">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="cc63d-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





