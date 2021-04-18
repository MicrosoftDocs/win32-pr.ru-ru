---
title: Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер
description: Событие Аудиолангуажечанже возникает при изменении текущего звукового языка. | Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Событие Аудиолангуажечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694393"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2222a-105">Событие Аудиолангуажечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="2222a-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2222a-106">Событие Аудиолангуажечанже возникает при изменении текущего звукового языка.</span><span class="sxs-lookup"><span data-stu-id="2222a-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="2222a-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="2222a-107">Event Data</span></span>

<span data-ttu-id="2222a-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ аудиолангуажечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="2222a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="2222a-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ аудиолангуажечанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="2222a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="2222a-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="2222a-110">Property</span></span>   | <span data-ttu-id="2222a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2222a-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2222a-112">**Надежно**</span><span class="sxs-lookup"><span data-stu-id="2222a-112">**langID**</span></span> | <span data-ttu-id="2222a-113">**System. Int32** Уникально идентифицирует определенный диалект языка, называемый языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="2222a-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2222a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2222a-114">Remarks</span></span>

<span data-ttu-id="2222a-115">Код локали (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="2222a-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="2222a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2222a-116">Requirements</span></span>



| <span data-ttu-id="2222a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2222a-117">Requirement</span></span> | <span data-ttu-id="2222a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2222a-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2222a-119">Версия</span><span class="sxs-lookup"><span data-stu-id="2222a-119">Version</span></span><br/>   | <span data-ttu-id="2222a-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2222a-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2222a-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2222a-121">Namespace</span></span><br/> | <span data-ttu-id="2222a-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="2222a-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2222a-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="2222a-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2222a-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2222a-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2222a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2222a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2222a-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2222a-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2222a-127">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2222a-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





