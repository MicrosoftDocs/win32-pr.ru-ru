---
title: Интерфейс IWMPControls2 (VB и C) (Wmp.h)
description: Предоставляет метод, который дополняет интерфейс Ивмпконтролс.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB и C) интерфейс проигрывателя Windows Media
- IWMPControls2 (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688846"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="c8e3a-105">Интерфейс IWMPControls2 (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="c8e3a-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="c8e3a-106">Предоставляет метод, который дополняет интерфейс [**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .</span><span class="sxs-lookup"><span data-stu-id="c8e3a-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="c8e3a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c8e3a-107">Members</span></span>

<span data-ttu-id="c8e3a-108">Интерфейс **IWMPControls2 (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8e3a-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="c8e3a-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c8e3a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8e3a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c8e3a-110">Methods</span></span>

<span data-ttu-id="c8e3a-111">Интерфейс **IWMPControls2 (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c8e3a-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="c8e3a-112">Метод</span><span class="sxs-lookup"><span data-stu-id="c8e3a-112">Method</span></span>                                                           | <span data-ttu-id="c8e3a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c8e3a-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8e3a-114">**первом**</span><span class="sxs-lookup"><span data-stu-id="c8e3a-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="c8e3a-115">Перемещает текущий элемент мультимедиа в следующий кадр или предыдущий кадр и закрепляет воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="c8e3a-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="c8e3a-116">В следующем примере кода показано, как получить доступ к интерфейсу [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) .</span><span class="sxs-lookup"><span data-stu-id="c8e3a-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="c8e3a-117">В примере кода приведено значение [**ивмпконтролс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) , которое свойство [**аксвиндовсмедиаплайер. Ктлконтролс**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) возвращает значение **IWMPControls2** .</span><span class="sxs-lookup"><span data-stu-id="c8e3a-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="c8e3a-118">Для **C#**:</span><span class="sxs-lookup"><span data-stu-id="c8e3a-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="c8e3a-119">Для **VB**:</span><span class="sxs-lookup"><span data-stu-id="c8e3a-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="c8e3a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c8e3a-120">Requirements</span></span>



| <span data-ttu-id="c8e3a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c8e3a-121">Requirement</span></span> | <span data-ttu-id="c8e3a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c8e3a-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c8e3a-123">Header</span><span class="sxs-lookup"><span data-stu-id="c8e3a-123">Header</span></span><br/> | <dl> <span data-ttu-id="c8e3a-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e3a-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e3a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8e3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e3a-126">**ивмпконтролс**</span><span class="sxs-lookup"><span data-stu-id="c8e3a-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="c8e3a-127">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="c8e3a-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8e3a-128">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c8e3a-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8e3a-129">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c8e3a-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





