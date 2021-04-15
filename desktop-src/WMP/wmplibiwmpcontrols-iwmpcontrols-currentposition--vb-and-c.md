---
title: Ивмпконтролс currentPosition, свойство
description: Свойство currentPosition Возвращает или задает текущую позицию в элементе мультимедиа в секундах с начала.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Проигрыватель Windows Media для свойства currentPosition
- currentPosition свойство проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, свойство currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689310"
---
# <a name="iwmpcontrolscurrentposition-property"></a><span data-ttu-id="d1f58-106">Свойство Ивмпконтролс:: currentPosition</span><span class="sxs-lookup"><span data-stu-id="d1f58-106">IWMPControls::currentPosition property</span></span>

<span data-ttu-id="d1f58-107">Свойство **CurrentPosition** Возвращает или задает текущую позицию в элементе мультимедиа в секундах с начала.</span><span class="sxs-lookup"><span data-stu-id="d1f58-107">The **currentPosition** property gets or sets the current position in the media item in seconds from the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f58-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1f58-108">Syntax</span></span>


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a><span data-ttu-id="d1f58-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d1f58-109">Property value</span></span>

<span data-ttu-id="d1f58-110">Значение **System. Double** , которое является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="d1f58-110">A **System.Double** that is the current position.</span></span>

## <a name="examples"></a><span data-ttu-id="d1f58-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1f58-111">Examples</span></span>

<span data-ttu-id="d1f58-112">В следующем примере **CurrentPosition** используется для поиска расположения, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="d1f58-112">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="d1f58-113">В ответ на нажатие кнопки **CurrentPosition** задается значение, указанное в текстовом поле с именем невпоситион.</span><span class="sxs-lookup"><span data-stu-id="d1f58-113">In response to a button click, **currentPosition** is set to the value entered in a text box called newPosition.</span></span> <span data-ttu-id="d1f58-114">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="d1f58-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d1f58-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d1f58-115">Requirements</span></span>



| <span data-ttu-id="d1f58-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d1f58-116">Requirement</span></span> | <span data-ttu-id="d1f58-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d1f58-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f58-118">Версия</span><span class="sxs-lookup"><span data-stu-id="d1f58-118">Version</span></span><br/>   | <span data-ttu-id="d1f58-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d1f58-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d1f58-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1f58-120">Namespace</span></span><br/> | <span data-ttu-id="d1f58-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d1f58-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d1f58-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="d1f58-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d1f58-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d1f58-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f58-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1f58-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f58-125">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d1f58-125">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d1f58-126">**Ивмпконтролс. Куррентпоситионстринг (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d1f58-126">**IWMPControls.currentPositionString (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





