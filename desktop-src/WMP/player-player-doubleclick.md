---
title: Событие Player. DoubleClick
description: Событие DoubleClick возникает, когда пользователь дважды щелкает кнопку мыши.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- Проигрыватель Windows Media Event DoubleClick
- Проигрыватель Windows Media Event DoubleClick, класс Player
- Класс проигрывателя Windows Media Player, событие DoubleClick
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3670bfbf3b72fad64f8fb515f5151920b34f52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708317"
---
# <a name="playerdoubleclick-event"></a><span data-ttu-id="cd678-106">Событие Player. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="cd678-106">Player.DoubleClick event</span></span>

<span data-ttu-id="cd678-107">Событие **DoubleClick** возникает, когда пользователь дважды щелкает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="cd678-107">The **DoubleClick** event occurs when the user double-clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd678-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd678-108">Syntax</span></span>


```JScript
Player.DoubleClick(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="cd678-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd678-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd678-110">*нбуттон*</span><span class="sxs-lookup"><span data-stu-id="cd678-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="cd678-111">**Число** (**int**), задающее битовую глубину, соответствующую левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="cd678-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="cd678-112">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="cd678-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cd678-113">Задан только один из битов, указывающий кнопку, вызвавшую событие.</span><span class="sxs-lookup"><span data-stu-id="cd678-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="cd678-114">*ншифтстате*</span><span class="sxs-lookup"><span data-stu-id="cd678-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="cd678-115">**Число** (**int**), задающее битовую глубину, которая соответствует клавише Shift (бит 0), клавиша Ctrl (бит 1) и клавиша Alt (бит 2).</span><span class="sxs-lookup"><span data-stu-id="cd678-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="cd678-116">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="cd678-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="cd678-117">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="cd678-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="cd678-118">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="cd678-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="cd678-119">*fX*</span><span class="sxs-lookup"><span data-stu-id="cd678-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="cd678-120">**Число** (**длинное**), определяющее координату x указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cd678-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="cd678-121">*Обозначения*</span><span class="sxs-lookup"><span data-stu-id="cd678-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="cd678-122">**Число** (**длинное**), указывающее координату y указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cd678-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd678-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd678-123">Return value</span></span>

<span data-ttu-id="cd678-124">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cd678-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd678-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd678-125">Remarks</span></span>

<span data-ttu-id="cd678-126">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cd678-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="cd678-127">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="cd678-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="cd678-128">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd678-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd678-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cd678-129">Requirements</span></span>



| <span data-ttu-id="cd678-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cd678-130">Requirement</span></span> | <span data-ttu-id="cd678-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cd678-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd678-132">Версия</span><span class="sxs-lookup"><span data-stu-id="cd678-132">Version</span></span><br/> | <span data-ttu-id="cd678-133">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd678-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="cd678-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cd678-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd678-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd678-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd678-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd678-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd678-137">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="cd678-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





