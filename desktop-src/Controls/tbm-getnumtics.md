---
title: Сообщение TBM_GETNUMTICS (Коммктрл. h)
description: Возвращает количество делений в TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Элементы управления Windows для TBM_GETNUMTICS сообщений
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988368"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="eb453-104">\_Сообщение ТБМ жетнумтикс</span><span class="sxs-lookup"><span data-stu-id="eb453-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="eb453-105">Возвращает количество делений в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="eb453-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb453-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb453-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb453-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb453-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="eb453-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb453-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb453-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb453-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="eb453-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb453-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb453-111">Return value</span></span>

<span data-ttu-id="eb453-112">Если [флаг деления](trackbar-control-styles.md) не установлен, он возвращает значение 2 для начального и конечного тактов.</span><span class="sxs-lookup"><span data-stu-id="eb453-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="eb453-113">Если [**задан \_ параметр TBS**](trackbar-control-styles.md) , он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="eb453-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="eb453-114">В противном случае он принимает разность между минимальным и максимальным диапазоном, делит их на тактовую частоту и добавляет 2.</span><span class="sxs-lookup"><span data-stu-id="eb453-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb453-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb453-115">Remarks</span></span>

<span data-ttu-id="eb453-116">Сообщение **ТБМ \_ жетнумтикс** подсчитывает все деления, включая первый и последний деления, созданные с помощью TrackBar.</span><span class="sxs-lookup"><span data-stu-id="eb453-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb453-117">Требования</span><span class="sxs-lookup"><span data-stu-id="eb453-117">Requirements</span></span>



| <span data-ttu-id="eb453-118">Требование</span><span class="sxs-lookup"><span data-stu-id="eb453-118">Requirement</span></span> | <span data-ttu-id="eb453-119">Значение</span><span class="sxs-lookup"><span data-stu-id="eb453-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb453-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb453-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eb453-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb453-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb453-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb453-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eb453-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb453-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb453-124">Header</span><span class="sxs-lookup"><span data-stu-id="eb453-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb453-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb453-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





