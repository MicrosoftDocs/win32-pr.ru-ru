---
title: Ивмпконтролс Куррентпоситионстринг, свойство
description: Свойство Куррентпоситионстринг получает текущую позицию в элементе мультимедиа в виде строки в формате чч мм СС (часы, минуты и секунды).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- Проигрыватель Windows Media для свойства Куррентпоситионстринг
- Куррентпоситионстринг свойство проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, свойство Куррентпоситионстринг
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689311"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="1a599-106">Свойство Ивмпконтролс:: Куррентпоситионстринг</span><span class="sxs-lookup"><span data-stu-id="1a599-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="1a599-107">Свойство **куррентпоситионстринг** получает текущую позицию в элементе мультимедиа в виде строки, отформатированной как чч: мм: СС (часы, минуты и секунды).</span><span class="sxs-lookup"><span data-stu-id="1a599-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="1a599-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a599-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a599-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a599-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="1a599-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1a599-110">Property value</span></span>

<span data-ttu-id="1a599-111">Форматированная **Строка System. String** , которая является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="1a599-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a599-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a599-112">Remarks</span></span>

<span data-ttu-id="1a599-113">Если размер элемента мультимедиа меньше часа, текущая позиция форматируется как MM: SS (минуты и секунды).</span><span class="sxs-lookup"><span data-stu-id="1a599-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="1a599-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a599-114">Examples</span></span>

<span data-ttu-id="1a599-115">В следующем примере запускается таймер, который запускает событие с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="1a599-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="1a599-116">В обработчике событий таймера метка обновляется с помощью **куррентпоситионстринг**.</span><span class="sxs-lookup"><span data-stu-id="1a599-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="1a599-117">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="1a599-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1a599-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1a599-118">Requirements</span></span>



| <span data-ttu-id="1a599-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1a599-119">Requirement</span></span> | <span data-ttu-id="1a599-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a599-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a599-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1a599-121">Version</span></span><br/>   | <span data-ttu-id="1a599-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a599-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1a599-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a599-123">Namespace</span></span><br/> | <span data-ttu-id="1a599-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="1a599-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1a599-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="1a599-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1a599-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1a599-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a599-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a599-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a599-128">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1a599-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1a599-129">**Ивмпконтролс. currentPosition (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1a599-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





