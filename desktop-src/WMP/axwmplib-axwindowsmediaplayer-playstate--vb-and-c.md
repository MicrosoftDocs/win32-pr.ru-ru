---
title: Аксвиндовсмедиаплайер. Плайстате, свойство
description: Свойство Плайстате возвращает значение перечисления, указывающее состояние операции проигрывателя Windows Media.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Проигрыватель Windows Media для свойства Плайстате
- Плайстате свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Плайстате
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699076"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="a9011-106">Аксвиндовсмедиаплайер. Плайстате, свойство</span><span class="sxs-lookup"><span data-stu-id="a9011-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="a9011-107">Свойство Плайстате возвращает значение перечисления, указывающее состояние операции проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a9011-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="a9011-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a9011-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9011-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9011-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="a9011-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a9011-110">Property value</span></span>

<span data-ttu-id="a9011-111">Значение перечисления Вмплиб. Вмпплайстате.</span><span class="sxs-lookup"><span data-stu-id="a9011-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9011-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9011-112">Remarks</span></span>

<span data-ttu-id="a9011-113">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="a9011-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="a9011-114">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="a9011-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="a9011-115">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="a9011-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="a9011-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="a9011-116">Examples</span></span>

<span data-ttu-id="a9011-117">В следующем примере свойство Плайстате используется для вывода текущего состояния воспроизведения проигрывателя в метке.</span><span class="sxs-lookup"><span data-stu-id="a9011-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="a9011-118">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="a9011-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="a9011-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a9011-119">Requirements</span></span>



| <span data-ttu-id="a9011-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a9011-120">Requirement</span></span> | <span data-ttu-id="a9011-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a9011-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9011-122">Версия</span><span class="sxs-lookup"><span data-stu-id="a9011-122">Version</span></span><br/>   | <span data-ttu-id="a9011-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a9011-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a9011-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9011-124">Namespace</span></span><br/> | <span data-ttu-id="a9011-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="a9011-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a9011-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="a9011-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a9011-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a9011-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9011-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9011-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9011-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a9011-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a9011-130">**Событие Аксвиндовсмедиаплайер. Плайстатечанже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a9011-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="a9011-131">**вмпплайстате**</span><span class="sxs-lookup"><span data-stu-id="a9011-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





