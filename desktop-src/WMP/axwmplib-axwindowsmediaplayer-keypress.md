---
title: Событие KeyPress объекта Аксвиндовсмедиаплайер
description: Событие KeyPress возникает при нажатии и отпускании клавиши. | Событие KeyPress объекта Аксвиндовсмедиаплайер
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Событие KeyPress объекта Аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699027"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="16a56-105">Событие KeyPress объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="16a56-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="16a56-106">Событие KeyPress возникает при нажатии и отпускании клавиши.</span><span class="sxs-lookup"><span data-stu-id="16a56-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="16a56-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="16a56-107">Event Data</span></span>

<span data-ttu-id="16a56-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кэйпрессевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="16a56-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="16a56-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кэйпрессевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="16a56-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="16a56-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="16a56-110">Property</span></span>      | <span data-ttu-id="16a56-111">Описание</span><span class="sxs-lookup"><span data-stu-id="16a56-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16a56-112">**нкэйасЦии**</span><span class="sxs-lookup"><span data-stu-id="16a56-112">**nKeyAscii**</span></span> | <span data-ttu-id="16a56-113">System. Int16Specifies — стандартный числовой код ANSI для символа.</span><span class="sxs-lookup"><span data-stu-id="16a56-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16a56-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16a56-114">Remarks</span></span>

<span data-ttu-id="16a56-115">Это событие возникает, когда нажатие клавиши приводит к вводу любого печатного символа клавиатуры, клавиши CTRL в сочетании с символом из стандартного алфавита или одного из нескольких специальных символов, а также клавишей Ввод или BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="16a56-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a56-116">Требования</span><span class="sxs-lookup"><span data-stu-id="16a56-116">Requirements</span></span>



| <span data-ttu-id="16a56-117">Требование</span><span class="sxs-lookup"><span data-stu-id="16a56-117">Requirement</span></span> | <span data-ttu-id="16a56-118">Значение</span><span class="sxs-lookup"><span data-stu-id="16a56-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a56-119">Версия</span><span class="sxs-lookup"><span data-stu-id="16a56-119">Version</span></span><br/>   | <span data-ttu-id="16a56-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="16a56-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16a56-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="16a56-121">Namespace</span></span><br/> | <span data-ttu-id="16a56-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="16a56-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16a56-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="16a56-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16a56-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="16a56-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a56-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16a56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a56-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="16a56-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





