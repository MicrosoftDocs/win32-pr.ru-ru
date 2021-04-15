---
title: Сообщение TTM_GETDELAYTIME (Коммктрл. h)
description: Извлекает начальные, всплывающие и повторно отображаемые длительности, заданные для элемента управления ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Элементы управления Windows для TTM_GETDELAYTIME сообщений
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654505"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="d97ec-104">\_Сообщение ТТМ жетделайтиме</span><span class="sxs-lookup"><span data-stu-id="d97ec-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="d97ec-105">Извлекает начальные, всплывающие и повторно отображаемые длительности, заданные для элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d97ec-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d97ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d97ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d97ec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d97ec-108">Флаг, указывающий, какое значение длительности будет получено.</span><span class="sxs-lookup"><span data-stu-id="d97ec-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="d97ec-109">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d97ec-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="d97ec-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d97ec-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d97ec-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d97ec-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="d97ec-112"><dt>**ТТДТ \_ аутопоп**</dt></span><span class="sxs-lookup"><span data-stu-id="d97ec-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="d97ec-113">Получение количества времени, в течение которого окно подсказки остается видимым, если указатель мыши находится в ограничивающем прямоугольнике инструмента.</span><span class="sxs-lookup"><span data-stu-id="d97ec-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="d97ec-114"><dt>**\_Начальная ттдт**</dt></span><span class="sxs-lookup"><span data-stu-id="d97ec-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="d97ec-115">Получение времени, в течение которого указатель должен оставаться свободным внутри ограничивающего прямоугольника инструмента, прежде чем появится окно подсказки.</span><span class="sxs-lookup"><span data-stu-id="d97ec-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="d97ec-116"><dt>**ТТДТ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d97ec-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="d97ec-117">Получение времени, затрачиваемого на отображение последующих окон всплывающей подсказки при переходе указателя с одного инструмента на другое.</span><span class="sxs-lookup"><span data-stu-id="d97ec-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="d97ec-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d97ec-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d97ec-119">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d97ec-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97ec-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d97ec-120">Return value</span></span>

<span data-ttu-id="d97ec-121">Возвращает и значение типа INT с заданной длительностью в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="d97ec-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97ec-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d97ec-122">Requirements</span></span>



| <span data-ttu-id="d97ec-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d97ec-123">Requirement</span></span> | <span data-ttu-id="d97ec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d97ec-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d97ec-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d97ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d97ec-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d97ec-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d97ec-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d97ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d97ec-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d97ec-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d97ec-129">Header</span><span class="sxs-lookup"><span data-stu-id="d97ec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d97ec-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d97ec-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d97ec-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d97ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d97ec-132">**ТТМ \_ сетделайтиме**</span><span class="sxs-lookup"><span data-stu-id="d97ec-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





