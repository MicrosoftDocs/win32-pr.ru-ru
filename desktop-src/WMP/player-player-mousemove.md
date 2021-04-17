---
title: Событие Player. MouseMove
description: Событие MouseMove возникает при перемещении указателя мыши. | Событие Player. MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Проигрыватель Windows Media, событие MouseMove
- Класс проигрывателя Windows Media для события MouseMove
- Класс проигрывателя Windows Media Player, событие MouseMove
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704245"
---
# <a name="playermousemove-event"></a><span data-ttu-id="2084c-107">Событие Player. MouseMove</span><span class="sxs-lookup"><span data-stu-id="2084c-107">Player.MouseMove event</span></span>

<span data-ttu-id="2084c-108">Событие **MouseMove** возникает при перемещении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="2084c-108">The **MouseMove** event occurs when the mouse pointer is moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="2084c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2084c-109">Syntax</span></span>


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="2084c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2084c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2084c-111">*нбуттон*</span><span class="sxs-lookup"><span data-stu-id="2084c-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="2084c-112">**Число** (**int**), задающее битовую глубину, соответствующую левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="2084c-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="2084c-113">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="2084c-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2084c-114">Могут быть заданы некоторые, все или никакие биты, указывающие на то, что нажаты некоторые, все или ни одна из кнопок.</span><span class="sxs-lookup"><span data-stu-id="2084c-114">Some, all, or none of the bits can be set, indicating that some, all, or none of the buttons are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2084c-115">*ншифтстате*</span><span class="sxs-lookup"><span data-stu-id="2084c-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="2084c-116">**Число** (**int**), задающее битовую глубину, которая соответствует клавише Shift (бит 0), клавиша Ctrl (бит 1) и клавиша Alt (бит 2).</span><span class="sxs-lookup"><span data-stu-id="2084c-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="2084c-117">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="2084c-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2084c-118">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="2084c-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="2084c-119">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="2084c-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2084c-120">*fX*</span><span class="sxs-lookup"><span data-stu-id="2084c-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="2084c-121">**Число** (**длинное**), определяющее координату x указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2084c-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2084c-122">*Обозначения*</span><span class="sxs-lookup"><span data-stu-id="2084c-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="2084c-123">**Число** (**длинное**), указывающее координату y указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2084c-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2084c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2084c-124">Return value</span></span>

<span data-ttu-id="2084c-125">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2084c-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2084c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2084c-126">Remarks</span></span>

<span data-ttu-id="2084c-127">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="2084c-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="2084c-128">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="2084c-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="2084c-129">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2084c-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="2084c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2084c-130">Requirements</span></span>



| <span data-ttu-id="2084c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2084c-131">Requirement</span></span> | <span data-ttu-id="2084c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2084c-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2084c-133">Версия</span><span class="sxs-lookup"><span data-stu-id="2084c-133">Version</span></span><br/> | <span data-ttu-id="2084c-134">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2084c-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2084c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2084c-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="2084c-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2084c-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2084c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2084c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2084c-138">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="2084c-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





