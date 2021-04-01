---
title: Сообщение TBM_GETTHUMBRECT (Коммктрл. h)
description: Получает размер и положение ограничивающего прямоугольника для ползунка в TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Элементы управления Windows для TBM_GETTHUMBRECT сообщений
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071647"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="d81f2-104">\_Сообщение ТБМ жетсумбрект</span><span class="sxs-lookup"><span data-stu-id="d81f2-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="d81f2-105">Получает размер и положение ограничивающего прямоугольника для ползунка в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d81f2-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d81f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d81f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d81f2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d81f2-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d81f2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d81f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d81f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d81f2-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d81f2-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="d81f2-111">Сообщение заполняет эту структуру ограничивающим прямоугольником ползунка TrackBar в клиентских координатах окна TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d81f2-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81f2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d81f2-112">Return value</span></span>

<span data-ttu-id="d81f2-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d81f2-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81f2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d81f2-114">Requirements</span></span>



| <span data-ttu-id="d81f2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d81f2-115">Requirement</span></span> | <span data-ttu-id="d81f2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d81f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d81f2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d81f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d81f2-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d81f2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d81f2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d81f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d81f2-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d81f2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d81f2-121">Header</span><span class="sxs-lookup"><span data-stu-id="d81f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d81f2-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d81f2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

