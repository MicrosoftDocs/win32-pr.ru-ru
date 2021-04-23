---
title: Событие Player. KeyUp
description: Событие KeyUp возникает при отпускании клавиши. | Событие Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Проигрыватель Windows Media, событие KeyUp
- Клавиша Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685301"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="5c49f-107">Событие Player. KeyUp</span><span class="sxs-lookup"><span data-stu-id="5c49f-107">Player.KeyUp event</span></span>

<span data-ttu-id="5c49f-108">Событие **KeyUp** возникает при отпускании клавиши.</span><span class="sxs-lookup"><span data-stu-id="5c49f-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c49f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c49f-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="5c49f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c49f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c49f-111">*нкэйкоде*</span><span class="sxs-lookup"><span data-stu-id="5c49f-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="5c49f-112">**Число** (**int**), указывающее, какой физический ключ нажат.</span><span class="sxs-lookup"><span data-stu-id="5c49f-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="5c49f-113">Возможные значения см. в разделе [событие Player. KeyDown](player-player-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="5c49f-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c49f-114">*ншифтстате*</span><span class="sxs-lookup"><span data-stu-id="5c49f-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="5c49f-115">**Число** (**int**), задающее битовую глубину, которая соответствует клавише Shift (бит 0), клавиша Ctrl (бит 1) и клавиша Alt (бит 2).</span><span class="sxs-lookup"><span data-stu-id="5c49f-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="5c49f-116">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="5c49f-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5c49f-117">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="5c49f-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="5c49f-118">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="5c49f-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c49f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c49f-119">Return value</span></span>

<span data-ttu-id="5c49f-120">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5c49f-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c49f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c49f-121">Remarks</span></span>

<span data-ttu-id="5c49f-122">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="5c49f-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5c49f-123">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="5c49f-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5c49f-124">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c49f-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c49f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5c49f-125">Requirements</span></span>



| <span data-ttu-id="5c49f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5c49f-126">Requirement</span></span> | <span data-ttu-id="5c49f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5c49f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c49f-128">Версия</span><span class="sxs-lookup"><span data-stu-id="5c49f-128">Version</span></span><br/> | <span data-ttu-id="5c49f-129">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5c49f-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5c49f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5c49f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c49f-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c49f-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c49f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c49f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c49f-133">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="5c49f-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





