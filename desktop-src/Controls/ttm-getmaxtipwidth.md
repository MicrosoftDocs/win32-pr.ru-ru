---
title: Сообщение TTM_GETMAXTIPWIDTH (Коммктрл. h)
description: Возвращает максимальную ширину окна подсказки.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Элементы управления Windows для TTM_GETMAXTIPWIDTH сообщений
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988674"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="7bf10-104">\_Сообщение ТТМ жетмакстипвидс</span><span class="sxs-lookup"><span data-stu-id="7bf10-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="7bf10-105">Возвращает максимальную ширину окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="7bf10-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bf10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bf10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf10-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7bf10-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7bf10-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7bf10-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7bf10-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bf10-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7bf10-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7bf10-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf10-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bf10-111">Return value</span></span>

<span data-ttu-id="7bf10-112">Возвращает значение **типа int** , представляющее максимальную ширину подсказок в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7bf10-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="7bf10-113">Если максимальная ширина не была задана ранее, сообщение возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="7bf10-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf10-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bf10-114">Remarks</span></span>

<span data-ttu-id="7bf10-115">Максимальное значение ширины подсказки не указывает фактическую ширину окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="7bf10-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="7bf10-116">Вместо этого, если строка подсказки превышает максимальную ширину, элемент управления разбивает текст на несколько строк, используя пробелы для определения разрывов строк.</span><span class="sxs-lookup"><span data-stu-id="7bf10-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="7bf10-117">Если текст не может быть разбит на несколько строк, он будет отображаться в одной строке.</span><span class="sxs-lookup"><span data-stu-id="7bf10-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="7bf10-118">Длина этой строки может превысить максимальную ширину подсказки.</span><span class="sxs-lookup"><span data-stu-id="7bf10-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf10-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7bf10-119">Requirements</span></span>



| <span data-ttu-id="7bf10-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7bf10-120">Requirement</span></span> | <span data-ttu-id="7bf10-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7bf10-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf10-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bf10-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf10-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7bf10-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7bf10-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bf10-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf10-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7bf10-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bf10-126">Header</span><span class="sxs-lookup"><span data-stu-id="7bf10-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf10-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf10-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf10-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bf10-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf10-129">**ТТМ \_ сетмакстипвидс**</span><span class="sxs-lookup"><span data-stu-id="7bf10-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





