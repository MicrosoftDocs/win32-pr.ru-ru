---
title: Ивмпнетворк Фрамесскиппед, свойство
description: Свойство Фрамесскиппед возвращает общее число кадров, пропущенных во время воспроизведения.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Проигрыватель Windows Media для свойства Фрамесскиппед
- Фрамесскиппед свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Фрамесскиппед
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668555"
---
# <a name="iwmpnetworkframesskipped-property"></a><span data-ttu-id="5bea5-106">Свойство Ивмпнетворк:: Фрамесскиппед</span><span class="sxs-lookup"><span data-stu-id="5bea5-106">IWMPNetwork::framesSkipped property</span></span>

<span data-ttu-id="5bea5-107">Свойство **фрамесскиппед** возвращает общее число кадров, пропущенных во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5bea5-107">The **framesSkipped** property gets the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bea5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bea5-108">Syntax</span></span>


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5bea5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5bea5-109">Property value</span></span>

<span data-ttu-id="5bea5-110">Значение **System. Int32** , равное количеству пропущенных кадров.</span><span class="sxs-lookup"><span data-stu-id="5bea5-110">A **System.Int32** that is the number of frames skipped.</span></span>

## <a name="examples"></a><span data-ttu-id="5bea5-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="5bea5-111">Examples</span></span>

<span data-ttu-id="5bea5-112">В следующем примере кода используется **фрамесскиппед** для вывода общего числа кадров, пропущенных во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5bea5-112">The following code example uses **framesSkipped** to display the total number of frames skipped during playback.</span></span> <span data-ttu-id="5bea5-113">Сведения отображаются в метке, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="5bea5-113">The information is displayed in a label when the user clicks a button.</span></span> <span data-ttu-id="5bea5-114">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="5bea5-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5bea5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5bea5-115">Requirements</span></span>



| <span data-ttu-id="5bea5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5bea5-116">Requirement</span></span> | <span data-ttu-id="5bea5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5bea5-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bea5-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5bea5-118">Version</span></span><br/>   | <span data-ttu-id="5bea5-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5bea5-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5bea5-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5bea5-120">Namespace</span></span><br/> | <span data-ttu-id="5bea5-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="5bea5-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5bea5-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="5bea5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5bea5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5bea5-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bea5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bea5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bea5-125">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5bea5-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





