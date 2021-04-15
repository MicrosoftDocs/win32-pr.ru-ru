---
title: Пользовательские значения Draw (Коммктрл. h)
description: В этом разделе перечислены значения, используемые для обнаружения частей элемента управления TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648637"
---
# <a name="custom-draw-values"></a><span data-ttu-id="a031c-103">Пользовательские значения рисования</span><span class="sxs-lookup"><span data-stu-id="a031c-103">Custom Draw Values</span></span>

<span data-ttu-id="a031c-104">В этом разделе перечислены значения, используемые для обнаружения частей элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a031c-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="a031c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="a031c-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="a031c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a031c-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="a031c-107"><dt>**\_канал тбкд**</dt></span><span class="sxs-lookup"><span data-stu-id="a031c-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="a031c-108">Определяет канал, вдоль которого проводятся маркеры Thumb элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a031c-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="a031c-109"><dt>**ТБКД \_ бегунок**</dt></span><span class="sxs-lookup"><span data-stu-id="a031c-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="a031c-110">Определяет маркер Thumb элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a031c-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="a031c-111">Это часть элемента управления, который перемещает пользователь.</span><span class="sxs-lookup"><span data-stu-id="a031c-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="a031c-112"><dt>**ТБКД \_ ТИКС**</dt></span><span class="sxs-lookup"><span data-stu-id="a031c-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="a031c-113">Определяет деления, отображаемые вдоль границы элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a031c-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="a031c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a031c-114">Remarks</span></span>

<span data-ttu-id="a031c-115">Пользовательские значения рисования, например, задаются в элементе **двитемспек** структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .</span><span class="sxs-lookup"><span data-stu-id="a031c-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a031c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a031c-116">Requirements</span></span>



| <span data-ttu-id="a031c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a031c-117">Requirement</span></span> | <span data-ttu-id="a031c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a031c-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a031c-119">Header</span><span class="sxs-lookup"><span data-stu-id="a031c-119">Header</span></span><br/> | <dl> <span data-ttu-id="a031c-120"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a031c-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





