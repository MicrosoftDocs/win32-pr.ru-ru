---
title: Событие Медиаколлектиончанже объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектиончанже возникает при изменении коллекции носителей. | Событие Медиаколлектиончанже объекта Аксвиндовсмедиаплайер
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- Событие Медиаколлектиончанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699012"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="13638-105">Событие Медиаколлектиончанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="13638-105">MediaCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="13638-106">Событие Медиаколлектиончанже возникает при изменении коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="13638-106">The MediaCollectionChange event occurs when the media collection changes.</span></span>

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="13638-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="13638-107">Event Data</span></span>

<span data-ttu-id="13638-108">Это событие не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="13638-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="13638-109">Требования</span><span class="sxs-lookup"><span data-stu-id="13638-109">Requirements</span></span>



| <span data-ttu-id="13638-110">Требование</span><span class="sxs-lookup"><span data-stu-id="13638-110">Requirement</span></span> | <span data-ttu-id="13638-111">Значение</span><span class="sxs-lookup"><span data-stu-id="13638-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13638-112">Версия</span><span class="sxs-lookup"><span data-stu-id="13638-112">Version</span></span><br/>   | <span data-ttu-id="13638-113">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="13638-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="13638-114">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13638-114">Namespace</span></span><br/> | <span data-ttu-id="13638-115">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="13638-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="13638-116">Сборка</span><span class="sxs-lookup"><span data-stu-id="13638-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13638-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13638-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13638-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13638-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13638-119">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="13638-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13638-120">**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="13638-120">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13638-121">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="13638-121">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





