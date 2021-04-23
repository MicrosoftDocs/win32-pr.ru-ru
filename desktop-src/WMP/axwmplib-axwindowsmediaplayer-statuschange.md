---
title: Событие StatusChange объекта Аксвиндовсмедиаплайер
description: Событие StatusChange возникает при изменении значения свойства Status. | Событие StatusChange объекта Аксвиндовсмедиаплайер
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Событие StatusChange в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695038"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c0b0a-105">Событие StatusChange объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="c0b0a-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c0b0a-106">Событие **StatusChange** возникает при изменении значения свойства **Status** .</span><span class="sxs-lookup"><span data-stu-id="c0b0a-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="c0b0a-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="c0b0a-107">Event Data</span></span>

<span data-ttu-id="c0b0a-108">Это событие не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="c0b0a-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b0a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c0b0a-109">Requirements</span></span>



| <span data-ttu-id="c0b0a-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c0b0a-110">Requirement</span></span> | <span data-ttu-id="c0b0a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c0b0a-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b0a-112">Версия</span><span class="sxs-lookup"><span data-stu-id="c0b0a-112">Version</span></span><br/>   | <span data-ttu-id="c0b0a-113">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c0b0a-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c0b0a-114">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0b0a-114">Namespace</span></span><br/> | <span data-ttu-id="c0b0a-115">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="c0b0a-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c0b0a-116">Сборка</span><span class="sxs-lookup"><span data-stu-id="c0b0a-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c0b0a-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c0b0a-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b0a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0b0a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b0a-119">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c0b0a-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c0b0a-120">**Аксвиндовсмедиаплайер. Status (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c0b0a-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





