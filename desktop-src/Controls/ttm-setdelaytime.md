---
title: Сообщение TTM_SETDELAYTIME (Коммктрл. h)
description: Задает начальную, всплывающую и отображаемую длительность для элемента управления ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Элементы управления Windows для TTM_SETDELAYTIME сообщений
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988670"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="95770-104">\_Сообщение ТТМ сетделайтиме</span><span class="sxs-lookup"><span data-stu-id="95770-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="95770-105">Задает начальную, всплывающую и отображаемую длительность для элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="95770-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="95770-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95770-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95770-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95770-108">Флаг, указывающий, какое значение времени следует задать.</span><span class="sxs-lookup"><span data-stu-id="95770-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="95770-109">Этот параметр может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="95770-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="95770-110">Значение</span><span class="sxs-lookup"><span data-stu-id="95770-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="95770-111">Значение</span><span class="sxs-lookup"><span data-stu-id="95770-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="95770-112"><dt>**ТТДТ \_ аутопоп**</dt></span><span class="sxs-lookup"><span data-stu-id="95770-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="95770-113">Задайте время, в течение которого окно подсказки остается видимым, если указатель мыши находится в ограничивающем прямоугольнике инструмента.</span><span class="sxs-lookup"><span data-stu-id="95770-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="95770-114">Чтобы вернуть время задержки аутопоп к значению по умолчанию, присвойте параметру *lParam* значение-1.</span><span class="sxs-lookup"><span data-stu-id="95770-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="95770-115"><dt>**\_Начальная ттдт**</dt></span><span class="sxs-lookup"><span data-stu-id="95770-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="95770-116">Задайте количество времени, в течение которого указатель должен оставаться на месте в ограничивающем прямоугольнике инструмента перед отображением окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="95770-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="95770-117">Чтобы вернуть начальное время задержки к значению по умолчанию, присвойте параметру *lParam* значение-1.</span><span class="sxs-lookup"><span data-stu-id="95770-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="95770-118"><dt>**ТТДТ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95770-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="95770-119">Задайте время, необходимое для отображения последующих окон всплывающей подсказки при переходе указателя с одного инструмента на другое.</span><span class="sxs-lookup"><span data-stu-id="95770-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="95770-120">Чтобы вернуть время задержки повторного отображения к значению по умолчанию, установите параметр *lParam* в значение-1.</span><span class="sxs-lookup"><span data-stu-id="95770-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="95770-121"><dt>**ТТДТ \_ автоматически**</dt></span><span class="sxs-lookup"><span data-stu-id="95770-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="95770-122">Установите все три значения времени задержки в пропорции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95770-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="95770-123">Время аутопоп будет в десять раз больше начального времени, а время повторного отображения будет равно одному пятое начальное время.</span><span class="sxs-lookup"><span data-stu-id="95770-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="95770-124">Если этот флаг установлен, используйте положительное значение *lParam* , чтобы указать начальное время в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="95770-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="95770-125">Присвойте параметру *lParam* отрицательное значение, чтобы получить все три значения времени задержки до значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95770-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95770-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95770-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95770-127">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает время задержки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="95770-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="95770-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="95770-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95770-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95770-129">Return value</span></span>

<span data-ttu-id="95770-130">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="95770-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="95770-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95770-131">Remarks</span></span>

<span data-ttu-id="95770-132">Время задержки по умолчанию зависит от времени двойного щелчка.</span><span class="sxs-lookup"><span data-stu-id="95770-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="95770-133">Для времени двойного щелчка по умолчанию 500 мс, начальное, аутопопное и повторно отображаемое время задержки равно 500 мс, 5000ms и 100 мс соответственно.</span><span class="sxs-lookup"><span data-stu-id="95770-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="95770-134">В следующем фрагменте кода функция [**жетдаублекликктиме**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) используется для определения трех значений времени задержки для любой системы.</span><span class="sxs-lookup"><span data-stu-id="95770-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="95770-135">Требования</span><span class="sxs-lookup"><span data-stu-id="95770-135">Requirements</span></span>



| <span data-ttu-id="95770-136">Требование</span><span class="sxs-lookup"><span data-stu-id="95770-136">Requirement</span></span> | <span data-ttu-id="95770-137">Значение</span><span class="sxs-lookup"><span data-stu-id="95770-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95770-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95770-138">Minimum supported client</span></span><br/> | <span data-ttu-id="95770-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95770-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95770-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95770-140">Minimum supported server</span></span><br/> | <span data-ttu-id="95770-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95770-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95770-142">Header</span><span class="sxs-lookup"><span data-stu-id="95770-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="95770-143"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95770-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95770-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95770-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95770-145">**ТТМ \_ жетделайтиме**</span><span class="sxs-lookup"><span data-stu-id="95770-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 

