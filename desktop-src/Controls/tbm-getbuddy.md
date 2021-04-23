---
title: Сообщение TBM_GETBUDDY (Коммктрл. h)
description: Получает маркер для окна элемента управления TrackBar в заданном месте. Указанное расположение задается относительно ориентации элемента управления (по горизонтали или по вертикали).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Элементы управления Windows для TBM_GETBUDDY сообщений
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989432"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="32723-105">\_Сообщение ТБМ приятель</span><span class="sxs-lookup"><span data-stu-id="32723-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="32723-106">Получает маркер для окна элемента управления TrackBar в заданном месте.</span><span class="sxs-lookup"><span data-stu-id="32723-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="32723-107">Указанное расположение задается относительно ориентации элемента управления (по горизонтали или по вертикали).</span><span class="sxs-lookup"><span data-stu-id="32723-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="32723-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32723-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32723-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32723-110">Значение, указывающее, какой маркер оконного окна будет извлекаться по относительному расположению.</span><span class="sxs-lookup"><span data-stu-id="32723-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="32723-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="32723-111">This value can be one of the following:</span></span>



| <span data-ttu-id="32723-112">Значение</span><span class="sxs-lookup"><span data-stu-id="32723-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="32723-113">Значение</span><span class="sxs-lookup"><span data-stu-id="32723-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="32723-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="32723-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="32723-115">Получает маркер для собеседника слева от TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32723-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="32723-116">Если элемент управления TrackBar использует стиль [**по \_ вертикали**](trackbar-control-styles.md) , сообщение будет извлекать собеседника над TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32723-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="32723-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="32723-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="32723-118">Получает маркер, расположенный справа от TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32723-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="32723-119">Если элемент управления TrackBar использует стиль [**по \_ вертикали**](trackbar-control-styles.md) , сообщение будет извлекать собеседника под TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32723-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="32723-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32723-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32723-121">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="32723-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32723-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32723-122">Return value</span></span>

<span data-ttu-id="32723-123">Возвращает маркер для окна собеседника в расположении, указанном параметром *wParam*, или **значение NULL** , если в этом расположении не существует дружественного окна.</span><span class="sxs-lookup"><span data-stu-id="32723-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="32723-124">Требования</span><span class="sxs-lookup"><span data-stu-id="32723-124">Requirements</span></span>



| <span data-ttu-id="32723-125">Требование</span><span class="sxs-lookup"><span data-stu-id="32723-125">Requirement</span></span> | <span data-ttu-id="32723-126">Значение</span><span class="sxs-lookup"><span data-stu-id="32723-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32723-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32723-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32723-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32723-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32723-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32723-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32723-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32723-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32723-131">Header</span><span class="sxs-lookup"><span data-stu-id="32723-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="32723-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="32723-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





