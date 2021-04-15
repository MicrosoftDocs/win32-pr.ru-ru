---
title: Ивмпнетворк Лостпаккетс, свойство
description: Свойство Лостпаккетс возвращает число потерянных пакетов.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Проигрыватель Windows Media для свойства Лостпаккетс
- Лостпаккетс свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Лостпаккетс
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668849"
---
# <a name="iwmpnetworklostpackets-property"></a><span data-ttu-id="e3a4d-106">Свойство Ивмпнетворк:: Лостпаккетс</span><span class="sxs-lookup"><span data-stu-id="e3a4d-106">IWMPNetwork::lostPackets property</span></span>

<span data-ttu-id="e3a4d-107">Свойство **лостпаккетс** возвращает число потерянных пакетов.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-107">The **lostPackets** property gets the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a4d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3a4d-108">Syntax</span></span>


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e3a4d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e3a4d-109">Property value</span></span>

<span data-ttu-id="e3a4d-110">Значение **System. Int32** , равное количеству потерянных пакетов.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-110">A **System.Int32** that is the number of lost packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a4d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3a4d-111">Remarks</span></span>

<span data-ttu-id="e3a4d-112">Это свойство включает только пакеты потокового мультимедиа и возвращает нуль при использовании протокола HTTP, который не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-112">This property includes streaming media packets only, and will return zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="e3a4d-113">Пакеты могут быть потеряны по ряду причин, таким как тип и качество сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-113">Packets can be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="e3a4d-114">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="e3a4d-115">Значение не сбрасывается, если воспроизведение приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-115">The value is not reset if playback is paused.</span></span> <span data-ttu-id="e3a4d-116">Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .</span><span class="sxs-lookup"><span data-stu-id="e3a4d-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="e3a4d-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="e3a4d-117">Examples</span></span>

<span data-ttu-id="e3a4d-118">В следующем примере кода используется **лостпаккетс** для вывода общего числа потерянных пакетов во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-118">The following code example uses **lostPackets** to display the total number of packets lost during playback.</span></span> <span data-ttu-id="e3a4d-119">Сведения отображаются в метке, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-119">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="e3a4d-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="e3a4d-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e3a4d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e3a4d-121">Requirements</span></span>



| <span data-ttu-id="e3a4d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e3a4d-122">Requirement</span></span> | <span data-ttu-id="e3a4d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e3a4d-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a4d-124">Версия</span><span class="sxs-lookup"><span data-stu-id="e3a4d-124">Version</span></span><br/>   | <span data-ttu-id="e3a4d-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e3a4d-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e3a4d-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3a4d-126">Namespace</span></span><br/> | <span data-ttu-id="e3a4d-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="e3a4d-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e3a4d-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="e3a4d-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3a4d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a4d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a4d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3a4d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a4d-131">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3a4d-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3a4d-132">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3a4d-132">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





