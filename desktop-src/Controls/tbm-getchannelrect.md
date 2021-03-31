---
title: Сообщение TBM_GETCHANNELRECT (Коммктрл. h)
description: Получает размер и расположение ограничивающего прямоугольника для канала TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Элементы управления Windows для TBM_GETCHANNELRECT сообщений
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988369"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="8526a-104">\_Сообщение ТБМ жетчаннелрект</span><span class="sxs-lookup"><span data-stu-id="8526a-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="8526a-105">Получает размер и расположение ограничивающего прямоугольника для канала TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8526a-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="8526a-106">(Канал — это область, в которой перемещается ползунок.</span><span class="sxs-lookup"><span data-stu-id="8526a-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="8526a-107">Он содержит выделение при выборе диапазона.)</span><span class="sxs-lookup"><span data-stu-id="8526a-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="8526a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8526a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8526a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8526a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8526a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8526a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8526a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8526a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8526a-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8526a-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8526a-113">Сообщение заполняет эту структуру ограничивающим прямоугольником канала в клиентских координатах окна TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8526a-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8526a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8526a-114">Return value</span></span>

<span data-ttu-id="8526a-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8526a-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8526a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8526a-116">Requirements</span></span>



| <span data-ttu-id="8526a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8526a-117">Requirement</span></span> | <span data-ttu-id="8526a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8526a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8526a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8526a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8526a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8526a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8526a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8526a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8526a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8526a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8526a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8526a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8526a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8526a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

