---
title: Ивмпконтролс. доступ (VB и C)
description: Свойство Available (метод Get- \_ Available в C \) получает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- Проигрыватель Windows Media Ивмпконтролс. Available (VB и C)
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688847"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="bea45-104">Ивмпконтролс. доступ (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="bea45-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="bea45-105">Свойство **Available** (метод Get- **\_ Available** в C#) получает значение, указывающее, доступен ли указанный тип сведений или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="bea45-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="bea45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bea45-106">Parameters</span></span>

<span data-ttu-id="bea45-107">*бстритем*</span><span class="sxs-lookup"><span data-stu-id="bea45-107">*bstrItem*</span></span>

<span data-ttu-id="bea45-108">Строка System. String, которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bea45-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="bea45-109">Значение</span><span class="sxs-lookup"><span data-stu-id="bea45-109">Value</span></span>           | <span data-ttu-id="bea45-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bea45-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea45-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="bea45-111">currentItem</span></span>     | <span data-ttu-id="bea45-112">Обнаруживает, может ли пользователь задать свойство **ивмпконтролс. currentItem** .</span><span class="sxs-lookup"><span data-stu-id="bea45-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="bea45-113">куррентмаркер</span><span class="sxs-lookup"><span data-stu-id="bea45-113">currentMarker</span></span>   | <span data-ttu-id="bea45-114">Обнаруживает, может ли пользователь перейти к определенному маркеру.</span><span class="sxs-lookup"><span data-stu-id="bea45-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="bea45-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="bea45-115">currentPosition</span></span> | <span data-ttu-id="bea45-116">Обнаруживает, может ли пользователь перейти к определенной должности в файле.</span><span class="sxs-lookup"><span data-stu-id="bea45-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="bea45-117">Некоторые файлы не поддерживают поиск.</span><span class="sxs-lookup"><span data-stu-id="bea45-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="bea45-118">фастфорвард</span><span class="sxs-lookup"><span data-stu-id="bea45-118">fastForward</span></span>     | <span data-ttu-id="bea45-119">Обнаруживает, поддерживает ли файл быструю пересылку и можно ли вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="bea45-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="bea45-120">Многие типы файлов (и динамические потоки) не поддерживают Фастфорвард.</span><span class="sxs-lookup"><span data-stu-id="bea45-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="bea45-121">фастреверсе</span><span class="sxs-lookup"><span data-stu-id="bea45-121">fastReverse</span></span>     | <span data-ttu-id="bea45-122">Обнаруживает, поддерживает ли файл Фастреверсе и можно ли вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="bea45-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="bea45-123">Многие типы файлов (и динамические потоки) не поддерживают Фастреверсе.</span><span class="sxs-lookup"><span data-stu-id="bea45-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="bea45-124">Далее</span><span class="sxs-lookup"><span data-stu-id="bea45-124">next</span></span>            | <span data-ttu-id="bea45-125">Обнаруживает, может ли пользователь перейти к следующей записи списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bea45-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="bea45-126">pause</span><span class="sxs-lookup"><span data-stu-id="bea45-126">pause</span></span>           | <span data-ttu-id="bea45-127">Обнаруживает, доступен ли метод **ивмпконтролс. Pause** .</span><span class="sxs-lookup"><span data-stu-id="bea45-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="bea45-128">играть</span><span class="sxs-lookup"><span data-stu-id="bea45-128">play</span></span>            | <span data-ttu-id="bea45-129">Обнаруживает, доступен ли метод **ивмпконтролс. Play** .</span><span class="sxs-lookup"><span data-stu-id="bea45-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="bea45-130">Предыдущее время</span><span class="sxs-lookup"><span data-stu-id="bea45-130">previous</span></span>        | <span data-ttu-id="bea45-131">Обнаруживает, может ли пользователь перейти к предыдущей записи списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bea45-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="bea45-132">Шаг</span><span class="sxs-lookup"><span data-stu-id="bea45-132">step</span></span>            | <span data-ttu-id="bea45-133">Обнаруживает, доступен ли метод **IWMPControls2. Step** во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bea45-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="bea45-134">stop</span><span class="sxs-lookup"><span data-stu-id="bea45-134">stop</span></span>            | <span data-ttu-id="bea45-135">Обнаруживает, доступен ли метод **ивмпконтролс. останавливаться** .</span><span class="sxs-lookup"><span data-stu-id="bea45-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="bea45-136">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bea45-136">Property Value</span></span>

<span data-ttu-id="bea45-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="bea45-137">**System.Boolean**</span></span>

<span data-ttu-id="bea45-138">Значение **System. Boolean** , указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="bea45-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea45-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bea45-139">Remarks</span></span>

<span data-ttu-id="bea45-140">**Ивмпконтролс. Available** — это свойство в Visual Basic, которое принимает параметр.</span><span class="sxs-lookup"><span data-stu-id="bea45-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="bea45-141">В C# он называется методом **ивмпконтролс. Get- \_ Available** .</span><span class="sxs-lookup"><span data-stu-id="bea45-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="bea45-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="bea45-142">Examples</span></span>

<span data-ttu-id="bea45-143">В следующем примере используется свойство **Available** (метод Get- **\_ Available** в C#), чтобы убедиться, что текущий элемент мультимедиа поддерживает свойство **CurrentPosition** .</span><span class="sxs-lookup"><span data-stu-id="bea45-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="bea45-144">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="bea45-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="bea45-145">Требования</span><span class="sxs-lookup"><span data-stu-id="bea45-145">Requirements</span></span>



| <span data-ttu-id="bea45-146">Требование</span><span class="sxs-lookup"><span data-stu-id="bea45-146">Requirement</span></span> | <span data-ttu-id="bea45-147">Значение</span><span class="sxs-lookup"><span data-stu-id="bea45-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea45-148">Версия</span><span class="sxs-lookup"><span data-stu-id="bea45-148">Version</span></span><br/>   | <span data-ttu-id="bea45-149">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bea45-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bea45-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bea45-150">Namespace</span></span><br/> | <span data-ttu-id="bea45-151">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="bea45-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bea45-152">Сборка</span><span class="sxs-lookup"><span data-stu-id="bea45-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bea45-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bea45-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea45-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bea45-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea45-155">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bea45-156">**Ивмпконтролс. currentItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bea45-157">**Ивмпконтролс. Pause (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bea45-158">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bea45-159">**Ивмпконтролс. останавливаться (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bea45-160">**IWMPControls2. Step (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bea45-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





