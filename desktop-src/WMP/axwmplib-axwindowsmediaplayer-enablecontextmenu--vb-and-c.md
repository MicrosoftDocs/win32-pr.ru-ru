---
title: Аксвиндовсмедиаплайер. Енаблеконтекстмену, свойство
description: Свойство Енаблеконтекстмену получает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Проигрыватель Windows Media для свойства Енаблеконтекстмену
- Енаблеконтекстмену свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Енаблеконтекстмену
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694460"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a><span data-ttu-id="7c2f4-106">Аксвиндовсмедиаплайер. Енаблеконтекстмену, свойство</span><span class="sxs-lookup"><span data-stu-id="7c2f4-106">AxWindowsMediaPlayer.enableContextMenu property</span></span>

<span data-ttu-id="7c2f4-107">Свойство Енаблеконтекстмену получает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="7c2f4-107">The enableContextMenu property gets or sets a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2f4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c2f4-108">Syntax</span></span>


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="7c2f4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7c2f4-109">Property value</span></span>

<span data-ttu-id="7c2f4-110">Значение System. Boolean, указывающее, следует ли включить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="7c2f4-110">A System.Boolean value that indicates whether to enable the context menu.</span></span> <span data-ttu-id="7c2f4-111">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="7c2f4-111">The default value is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c2f4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c2f4-112">Remarks</span></span>

<span data-ttu-id="7c2f4-113">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="7c2f4-113">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2f4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7c2f4-114">Requirements</span></span>



| <span data-ttu-id="7c2f4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7c2f4-115">Requirement</span></span> | <span data-ttu-id="7c2f4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c2f4-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2f4-117">Версия</span><span class="sxs-lookup"><span data-stu-id="7c2f4-117">Version</span></span><br/>   | <span data-ttu-id="7c2f4-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7c2f4-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7c2f4-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c2f4-119">Namespace</span></span><br/> | <span data-ttu-id="7c2f4-120">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="7c2f4-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7c2f4-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="7c2f4-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7c2f4-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7c2f4-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c2f4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c2f4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2f4-124">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7c2f4-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





