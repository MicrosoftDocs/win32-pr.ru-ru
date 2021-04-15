---
title: Событие Player. KeyDown
description: Событие KeyDown возникает при нажатии клавиши. | Событие Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Событие KeyDown проигрыватель Windows Media Player
- Событие KeyDown проигрыватель Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689240"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="15893-107">Событие Player. KeyDown</span><span class="sxs-lookup"><span data-stu-id="15893-107">Player.KeyDown event</span></span>

<span data-ttu-id="15893-108">Событие **KeyDown** возникает при нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="15893-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="15893-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15893-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="15893-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="15893-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15893-111">*нкэйкоде*</span><span class="sxs-lookup"><span data-stu-id="15893-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="15893-112">**Число** (**int**), указывающее, какой физический ключ нажат.</span><span class="sxs-lookup"><span data-stu-id="15893-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="15893-113">Возможные значения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="15893-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="15893-114">*ншифтстате*</span><span class="sxs-lookup"><span data-stu-id="15893-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="15893-115">**Число** (**int**), задающее битовую глубину, которая соответствует клавише Shift (бит 0), клавиша Ctrl (бит 1) и клавиша Alt (бит 2).</span><span class="sxs-lookup"><span data-stu-id="15893-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="15893-116">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="15893-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="15893-117">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="15893-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="15893-118">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="15893-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15893-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15893-119">Return value</span></span>

<span data-ttu-id="15893-120">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="15893-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15893-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15893-121">Remarks</span></span>

<span data-ttu-id="15893-122">Аргумент *нкэйкоде* задает физический ключ.</span><span class="sxs-lookup"><span data-stu-id="15893-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="15893-123">В следующих таблицах приведены возможные значения для основных ключей на стандартной клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="15893-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="15893-124">Значения для основных ключей.</span><span class="sxs-lookup"><span data-stu-id="15893-124">Values for the main keys.</span></span>



| <span data-ttu-id="15893-125">Ключ</span><span class="sxs-lookup"><span data-stu-id="15893-125">Key</span></span>                     | <span data-ttu-id="15893-126">Значение</span><span class="sxs-lookup"><span data-stu-id="15893-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="15893-127">A – Z</span><span class="sxs-lookup"><span data-stu-id="15893-127">A-Z</span></span>                     | <span data-ttu-id="15893-128">65-90</span><span class="sxs-lookup"><span data-stu-id="15893-128">65-90</span></span>   |
| <span data-ttu-id="15893-129">0-9</span><span class="sxs-lookup"><span data-stu-id="15893-129">0-9</span></span>                     | <span data-ttu-id="15893-130">48-56</span><span class="sxs-lookup"><span data-stu-id="15893-130">48-56</span></span>   |
| <span data-ttu-id="15893-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="15893-131">F1-F12</span></span>                  | <span data-ttu-id="15893-132">112-123</span><span class="sxs-lookup"><span data-stu-id="15893-132">112-123</span></span> |
| <span data-ttu-id="15893-133">ESC</span><span class="sxs-lookup"><span data-stu-id="15893-133">ESC</span></span>                     | <span data-ttu-id="15893-134">27</span><span class="sxs-lookup"><span data-stu-id="15893-134">27</span></span>      |
| <span data-ttu-id="15893-135">TAB</span><span class="sxs-lookup"><span data-stu-id="15893-135">TAB</span></span>                     | <span data-ttu-id="15893-136">9</span><span class="sxs-lookup"><span data-stu-id="15893-136">9</span></span>       |
| <span data-ttu-id="15893-137">Caps Lock</span><span class="sxs-lookup"><span data-stu-id="15893-137">CAPS LOCK</span></span>               | <span data-ttu-id="15893-138">20</span><span class="sxs-lookup"><span data-stu-id="15893-138">20</span></span>      |
| <span data-ttu-id="15893-139">SHIFT (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="15893-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="15893-140">16</span><span class="sxs-lookup"><span data-stu-id="15893-140">16</span></span>      |
| <span data-ttu-id="15893-141">CTRL (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="15893-141">CTRL (left or right)</span></span>    | <span data-ttu-id="15893-142">17</span><span class="sxs-lookup"><span data-stu-id="15893-142">17</span></span>      |
| <span data-ttu-id="15893-143">ALT (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="15893-143">ALT (left or right)</span></span>     | <span data-ttu-id="15893-144">18</span><span class="sxs-lookup"><span data-stu-id="15893-144">18</span></span>      |
| <span data-ttu-id="15893-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="15893-145">SPACE</span></span>                   | <span data-ttu-id="15893-146">32</span><span class="sxs-lookup"><span data-stu-id="15893-146">32</span></span>      |
| <span data-ttu-id="15893-147">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="15893-147">BACKSPACE</span></span>               | <span data-ttu-id="15893-148">8</span><span class="sxs-lookup"><span data-stu-id="15893-148">8</span></span>       |
| <span data-ttu-id="15893-149">ВВОД</span><span class="sxs-lookup"><span data-stu-id="15893-149">ENTER</span></span>                   | <span data-ttu-id="15893-150">13</span><span class="sxs-lookup"><span data-stu-id="15893-150">13</span></span>      |
| <span data-ttu-id="15893-151">Клавиша с логотипом Windows, слева</span><span class="sxs-lookup"><span data-stu-id="15893-151">Windows logo key, left</span></span>  | <span data-ttu-id="15893-152">91</span><span class="sxs-lookup"><span data-stu-id="15893-152">91</span></span>      |
| <span data-ttu-id="15893-153">Клавиша с логотипом Windows, справа</span><span class="sxs-lookup"><span data-stu-id="15893-153">Windows logo key, right</span></span> | <span data-ttu-id="15893-154">92</span><span class="sxs-lookup"><span data-stu-id="15893-154">92</span></span>      |
| <span data-ttu-id="15893-155">Ключ приложения</span><span class="sxs-lookup"><span data-stu-id="15893-155">Application key</span></span>         | <span data-ttu-id="15893-156">93</span><span class="sxs-lookup"><span data-stu-id="15893-156">93</span></span>      |



 

<span data-ttu-id="15893-157">Значения клавиш для ввода чисел.</span><span class="sxs-lookup"><span data-stu-id="15893-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="15893-158">Ключ</span><span class="sxs-lookup"><span data-stu-id="15893-158">Key</span></span>               | <span data-ttu-id="15893-159">Значение</span><span class="sxs-lookup"><span data-stu-id="15893-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="15893-160">0-9</span><span class="sxs-lookup"><span data-stu-id="15893-160">0-9</span></span>               | <span data-ttu-id="15893-161">96-105</span><span class="sxs-lookup"><span data-stu-id="15893-161">96-105</span></span> |
| <span data-ttu-id="15893-162">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="15893-162">NUM LOCK</span></span>          | <span data-ttu-id="15893-163">144</span><span class="sxs-lookup"><span data-stu-id="15893-163">144</span></span>    |
| <span data-ttu-id="15893-164">РАЗДЕЛИТЬ (/)</span><span class="sxs-lookup"><span data-stu-id="15893-164">DIVIDE (/)</span></span>        | <span data-ttu-id="15893-165">111</span><span class="sxs-lookup"><span data-stu-id="15893-165">111</span></span>    |
| <span data-ttu-id="15893-166">УМНОЖИТЬ ( \* )</span><span class="sxs-lookup"><span data-stu-id="15893-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="15893-167">106</span><span class="sxs-lookup"><span data-stu-id="15893-167">106</span></span>    |
| <span data-ttu-id="15893-168">ВЫЧИТАНИе (-)</span><span class="sxs-lookup"><span data-stu-id="15893-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="15893-169">109</span><span class="sxs-lookup"><span data-stu-id="15893-169">109</span></span>    |
| <span data-ttu-id="15893-170">ДОБАВИТЬ (+)</span><span class="sxs-lookup"><span data-stu-id="15893-170">ADD (+)</span></span>           | <span data-ttu-id="15893-171">107</span><span class="sxs-lookup"><span data-stu-id="15893-171">107</span></span>    |
| <span data-ttu-id="15893-172">РАЗДЕЛИТЕЛЬ (Enter)</span><span class="sxs-lookup"><span data-stu-id="15893-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="15893-173">108</span><span class="sxs-lookup"><span data-stu-id="15893-173">108</span></span>    |
| <span data-ttu-id="15893-174">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="15893-174">DECIMAL (.)</span></span>       | <span data-ttu-id="15893-175">110</span><span class="sxs-lookup"><span data-stu-id="15893-175">110</span></span>    |



 

<span data-ttu-id="15893-176">Значения для клавиш навигации.</span><span class="sxs-lookup"><span data-stu-id="15893-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="15893-177">Ключ</span><span class="sxs-lookup"><span data-stu-id="15893-177">Key</span></span>         | <span data-ttu-id="15893-178">Значение</span><span class="sxs-lookup"><span data-stu-id="15893-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="15893-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="15893-179">INSERT</span></span>      | <span data-ttu-id="15893-180">45</span><span class="sxs-lookup"><span data-stu-id="15893-180">45</span></span>    |
| <span data-ttu-id="15893-181">DELETE</span><span class="sxs-lookup"><span data-stu-id="15893-181">DELETE</span></span>      | <span data-ttu-id="15893-182">46</span><span class="sxs-lookup"><span data-stu-id="15893-182">46</span></span>    |
| <span data-ttu-id="15893-183">HOME</span><span class="sxs-lookup"><span data-stu-id="15893-183">HOME</span></span>        | <span data-ttu-id="15893-184">36</span><span class="sxs-lookup"><span data-stu-id="15893-184">36</span></span>    |
| <span data-ttu-id="15893-185">END</span><span class="sxs-lookup"><span data-stu-id="15893-185">END</span></span>         | <span data-ttu-id="15893-186">35</span><span class="sxs-lookup"><span data-stu-id="15893-186">35</span></span>    |
| <span data-ttu-id="15893-187">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="15893-187">PAGE UP</span></span>     | <span data-ttu-id="15893-188">33</span><span class="sxs-lookup"><span data-stu-id="15893-188">33</span></span>    |
| <span data-ttu-id="15893-189">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="15893-189">PAGE DOWN</span></span>   | <span data-ttu-id="15893-190">34</span><span class="sxs-lookup"><span data-stu-id="15893-190">34</span></span>    |
| <span data-ttu-id="15893-191">СТРЕЛКА ВВЕРХ</span><span class="sxs-lookup"><span data-stu-id="15893-191">UP ARROW</span></span>    | <span data-ttu-id="15893-192">38</span><span class="sxs-lookup"><span data-stu-id="15893-192">38</span></span>    |
| <span data-ttu-id="15893-193">СТРЕЛКА ВНИЗ</span><span class="sxs-lookup"><span data-stu-id="15893-193">DOWN ARROW</span></span>  | <span data-ttu-id="15893-194">40</span><span class="sxs-lookup"><span data-stu-id="15893-194">40</span></span>    |
| <span data-ttu-id="15893-195">СТРЕЛКА ВЛЕВО</span><span class="sxs-lookup"><span data-stu-id="15893-195">LEFT ARROW</span></span>  | <span data-ttu-id="15893-196">37</span><span class="sxs-lookup"><span data-stu-id="15893-196">37</span></span>    |
| <span data-ttu-id="15893-197">СТРЕЛКА ВПРАВО</span><span class="sxs-lookup"><span data-stu-id="15893-197">RIGHT ARROW</span></span> | <span data-ttu-id="15893-198">39</span><span class="sxs-lookup"><span data-stu-id="15893-198">39</span></span>    |



 

<span data-ttu-id="15893-199">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="15893-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="15893-200">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="15893-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="15893-201">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="15893-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="15893-202">Требования</span><span class="sxs-lookup"><span data-stu-id="15893-202">Requirements</span></span>



| <span data-ttu-id="15893-203">Требование</span><span class="sxs-lookup"><span data-stu-id="15893-203">Requirement</span></span> | <span data-ttu-id="15893-204">Значение</span><span class="sxs-lookup"><span data-stu-id="15893-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15893-205">Версия</span><span class="sxs-lookup"><span data-stu-id="15893-205">Version</span></span><br/> | <span data-ttu-id="15893-206">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="15893-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="15893-207">DLL</span><span class="sxs-lookup"><span data-stu-id="15893-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="15893-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15893-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15893-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15893-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15893-210">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="15893-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





