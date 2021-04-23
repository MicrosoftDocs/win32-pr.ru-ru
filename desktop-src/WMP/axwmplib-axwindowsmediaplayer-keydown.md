---
title: Событие KeyDown объекта Аксвиндовсмедиаплайер
description: Событие KeyDown возникает при нажатии клавиши. | Событие KeyDown объекта Аксвиндовсмедиаплайер
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Событие KeyDown объекта Аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699029"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="60d67-105">Событие KeyDown объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="60d67-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="60d67-106">Событие KeyDown возникает при нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="60d67-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="60d67-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="60d67-107">Event Data</span></span>

<span data-ttu-id="60d67-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кэйдовневенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="60d67-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="60d67-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кэйдовневент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="60d67-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="60d67-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="60d67-110">Property</span></span>    | <span data-ttu-id="60d67-111">Описание</span><span class="sxs-lookup"><span data-stu-id="60d67-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d67-112">нкэйкоде</span><span class="sxs-lookup"><span data-stu-id="60d67-112">nKeyCode</span></span>    | <span data-ttu-id="60d67-113">System. Int16Specifies, на котором нажата физическая клавиша.</span><span class="sxs-lookup"><span data-stu-id="60d67-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="60d67-114">Возможные значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="60d67-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="60d67-115">ншифтстате</span><span class="sxs-lookup"><span data-stu-id="60d67-115">nShiftState</span></span> | <span data-ttu-id="60d67-116">System. Int16 — битовые биты с наименее значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="60d67-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="60d67-117">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="60d67-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="60d67-118">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="60d67-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="60d67-119">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="60d67-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60d67-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60d67-120">Remarks</span></span>

<span data-ttu-id="60d67-121">Свойство **нкэйкоде** Указывает физический ключ.</span><span class="sxs-lookup"><span data-stu-id="60d67-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="60d67-122">В следующих таблицах приведены возможные значения для основных ключей на стандартной клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="60d67-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="60d67-123">Значения для основных ключей.</span><span class="sxs-lookup"><span data-stu-id="60d67-123">Values for the main keys.</span></span>



| <span data-ttu-id="60d67-124">Ключ</span><span class="sxs-lookup"><span data-stu-id="60d67-124">Key</span></span>                     | <span data-ttu-id="60d67-125">Значение</span><span class="sxs-lookup"><span data-stu-id="60d67-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="60d67-126">A – Z</span><span class="sxs-lookup"><span data-stu-id="60d67-126">A-Z</span></span>                     | <span data-ttu-id="60d67-127">65-90</span><span class="sxs-lookup"><span data-stu-id="60d67-127">65-90</span></span>   |
| <span data-ttu-id="60d67-128">0-9</span><span class="sxs-lookup"><span data-stu-id="60d67-128">0-9</span></span>                     | <span data-ttu-id="60d67-129">48-56</span><span class="sxs-lookup"><span data-stu-id="60d67-129">48-56</span></span>   |
| <span data-ttu-id="60d67-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="60d67-130">F1-F12</span></span>                  | <span data-ttu-id="60d67-131">112-123</span><span class="sxs-lookup"><span data-stu-id="60d67-131">112-123</span></span> |
| <span data-ttu-id="60d67-132">ESC</span><span class="sxs-lookup"><span data-stu-id="60d67-132">ESC</span></span>                     | <span data-ttu-id="60d67-133">27</span><span class="sxs-lookup"><span data-stu-id="60d67-133">27</span></span>      |
| <span data-ttu-id="60d67-134">TAB</span><span class="sxs-lookup"><span data-stu-id="60d67-134">TAB</span></span>                     | <span data-ttu-id="60d67-135">9</span><span class="sxs-lookup"><span data-stu-id="60d67-135">9</span></span>       |
| <span data-ttu-id="60d67-136">Caps Lock</span><span class="sxs-lookup"><span data-stu-id="60d67-136">CAPS LOCK</span></span>               | <span data-ttu-id="60d67-137">20</span><span class="sxs-lookup"><span data-stu-id="60d67-137">20</span></span>      |
| <span data-ttu-id="60d67-138">SHIFT (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="60d67-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="60d67-139">16</span><span class="sxs-lookup"><span data-stu-id="60d67-139">16</span></span>      |
| <span data-ttu-id="60d67-140">CTRL (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="60d67-140">CTRL (left or right)</span></span>    | <span data-ttu-id="60d67-141">17</span><span class="sxs-lookup"><span data-stu-id="60d67-141">17</span></span>      |
| <span data-ttu-id="60d67-142">ALT (слева или справа)</span><span class="sxs-lookup"><span data-stu-id="60d67-142">ALT (left or right)</span></span>     | <span data-ttu-id="60d67-143">18</span><span class="sxs-lookup"><span data-stu-id="60d67-143">18</span></span>      |
| <span data-ttu-id="60d67-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="60d67-144">SPACE</span></span>                   | <span data-ttu-id="60d67-145">32</span><span class="sxs-lookup"><span data-stu-id="60d67-145">32</span></span>      |
| <span data-ttu-id="60d67-146">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="60d67-146">BACKSPACE</span></span>               | <span data-ttu-id="60d67-147">8</span><span class="sxs-lookup"><span data-stu-id="60d67-147">8</span></span>       |
| <span data-ttu-id="60d67-148">ВВОД</span><span class="sxs-lookup"><span data-stu-id="60d67-148">ENTER</span></span>                   | <span data-ttu-id="60d67-149">13</span><span class="sxs-lookup"><span data-stu-id="60d67-149">13</span></span>      |
| <span data-ttu-id="60d67-150">Клавиша с логотипом Windows, слева</span><span class="sxs-lookup"><span data-stu-id="60d67-150">Windows logo key, left</span></span>  | <span data-ttu-id="60d67-151">91</span><span class="sxs-lookup"><span data-stu-id="60d67-151">91</span></span>      |
| <span data-ttu-id="60d67-152">Клавиша с логотипом Windows, справа</span><span class="sxs-lookup"><span data-stu-id="60d67-152">Windows logo key, right</span></span> | <span data-ttu-id="60d67-153">92</span><span class="sxs-lookup"><span data-stu-id="60d67-153">92</span></span>      |
| <span data-ttu-id="60d67-154">Ключ приложения</span><span class="sxs-lookup"><span data-stu-id="60d67-154">Application key</span></span>         | <span data-ttu-id="60d67-155">93</span><span class="sxs-lookup"><span data-stu-id="60d67-155">93</span></span>      |



 

<span data-ttu-id="60d67-156">Значения клавиш для ввода чисел.</span><span class="sxs-lookup"><span data-stu-id="60d67-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="60d67-157">Ключ</span><span class="sxs-lookup"><span data-stu-id="60d67-157">Key</span></span>               | <span data-ttu-id="60d67-158">Значение</span><span class="sxs-lookup"><span data-stu-id="60d67-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="60d67-159">0-9</span><span class="sxs-lookup"><span data-stu-id="60d67-159">0-9</span></span>               | <span data-ttu-id="60d67-160">96-105</span><span class="sxs-lookup"><span data-stu-id="60d67-160">96-105</span></span> |
| <span data-ttu-id="60d67-161">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="60d67-161">NUM LOCK</span></span>          | <span data-ttu-id="60d67-162">144</span><span class="sxs-lookup"><span data-stu-id="60d67-162">144</span></span>    |
| <span data-ttu-id="60d67-163">РАЗДЕЛИТЬ (/)</span><span class="sxs-lookup"><span data-stu-id="60d67-163">DIVIDE (/)</span></span>        | <span data-ttu-id="60d67-164">111</span><span class="sxs-lookup"><span data-stu-id="60d67-164">111</span></span>    |
| <span data-ttu-id="60d67-165">УМНОЖИТЬ ( \* )</span><span class="sxs-lookup"><span data-stu-id="60d67-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="60d67-166">106</span><span class="sxs-lookup"><span data-stu-id="60d67-166">106</span></span>    |
| <span data-ttu-id="60d67-167">ВЫЧИТАНИе (-)</span><span class="sxs-lookup"><span data-stu-id="60d67-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="60d67-168">109</span><span class="sxs-lookup"><span data-stu-id="60d67-168">109</span></span>    |
| <span data-ttu-id="60d67-169">ДОБАВИТЬ (+)</span><span class="sxs-lookup"><span data-stu-id="60d67-169">ADD (+)</span></span>           | <span data-ttu-id="60d67-170">107</span><span class="sxs-lookup"><span data-stu-id="60d67-170">107</span></span>    |
| <span data-ttu-id="60d67-171">РАЗДЕЛИТЕЛЬ (Enter)</span><span class="sxs-lookup"><span data-stu-id="60d67-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="60d67-172">108</span><span class="sxs-lookup"><span data-stu-id="60d67-172">108</span></span>    |
| <span data-ttu-id="60d67-173">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="60d67-173">DECIMAL (.)</span></span>       | <span data-ttu-id="60d67-174">110</span><span class="sxs-lookup"><span data-stu-id="60d67-174">110</span></span>    |



 

<span data-ttu-id="60d67-175">Значения для клавиш навигации.</span><span class="sxs-lookup"><span data-stu-id="60d67-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="60d67-176">Ключ</span><span class="sxs-lookup"><span data-stu-id="60d67-176">Key</span></span>         | <span data-ttu-id="60d67-177">Значение</span><span class="sxs-lookup"><span data-stu-id="60d67-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="60d67-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="60d67-178">INSERT</span></span>      | <span data-ttu-id="60d67-179">45</span><span class="sxs-lookup"><span data-stu-id="60d67-179">45</span></span>    |
| <span data-ttu-id="60d67-180">DELETE</span><span class="sxs-lookup"><span data-stu-id="60d67-180">DELETE</span></span>      | <span data-ttu-id="60d67-181">46</span><span class="sxs-lookup"><span data-stu-id="60d67-181">46</span></span>    |
| <span data-ttu-id="60d67-182">HOME</span><span class="sxs-lookup"><span data-stu-id="60d67-182">HOME</span></span>        | <span data-ttu-id="60d67-183">36</span><span class="sxs-lookup"><span data-stu-id="60d67-183">36</span></span>    |
| <span data-ttu-id="60d67-184">END</span><span class="sxs-lookup"><span data-stu-id="60d67-184">END</span></span>         | <span data-ttu-id="60d67-185">35</span><span class="sxs-lookup"><span data-stu-id="60d67-185">35</span></span>    |
| <span data-ttu-id="60d67-186">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="60d67-186">PAGE UP</span></span>     | <span data-ttu-id="60d67-187">33</span><span class="sxs-lookup"><span data-stu-id="60d67-187">33</span></span>    |
| <span data-ttu-id="60d67-188">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="60d67-188">PAGE DOWN</span></span>   | <span data-ttu-id="60d67-189">34</span><span class="sxs-lookup"><span data-stu-id="60d67-189">34</span></span>    |
| <span data-ttu-id="60d67-190">СТРЕЛКА ВВЕРХ</span><span class="sxs-lookup"><span data-stu-id="60d67-190">UP ARROW</span></span>    | <span data-ttu-id="60d67-191">38</span><span class="sxs-lookup"><span data-stu-id="60d67-191">38</span></span>    |
| <span data-ttu-id="60d67-192">СТРЕЛКА ВНИЗ</span><span class="sxs-lookup"><span data-stu-id="60d67-192">DOWN ARROW</span></span>  | <span data-ttu-id="60d67-193">40</span><span class="sxs-lookup"><span data-stu-id="60d67-193">40</span></span>    |
| <span data-ttu-id="60d67-194">СТРЕЛКА ВЛЕВО</span><span class="sxs-lookup"><span data-stu-id="60d67-194">LEFT ARROW</span></span>  | <span data-ttu-id="60d67-195">37</span><span class="sxs-lookup"><span data-stu-id="60d67-195">37</span></span>    |
| <span data-ttu-id="60d67-196">СТРЕЛКА ВПРАВО</span><span class="sxs-lookup"><span data-stu-id="60d67-196">RIGHT ARROW</span></span> | <span data-ttu-id="60d67-197">39</span><span class="sxs-lookup"><span data-stu-id="60d67-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="60d67-198">Требования</span><span class="sxs-lookup"><span data-stu-id="60d67-198">Requirements</span></span>



| <span data-ttu-id="60d67-199">Требование</span><span class="sxs-lookup"><span data-stu-id="60d67-199">Requirement</span></span> | <span data-ttu-id="60d67-200">Значение</span><span class="sxs-lookup"><span data-stu-id="60d67-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d67-201">Версия</span><span class="sxs-lookup"><span data-stu-id="60d67-201">Version</span></span><br/>   | <span data-ttu-id="60d67-202">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="60d67-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="60d67-203">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60d67-203">Namespace</span></span><br/> | <span data-ttu-id="60d67-204">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="60d67-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="60d67-205">Сборка</span><span class="sxs-lookup"><span data-stu-id="60d67-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="60d67-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="60d67-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d67-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60d67-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d67-208">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="60d67-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





