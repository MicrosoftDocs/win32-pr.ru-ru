---
title: Сообщение TTM_SETMAXTIPWIDTH (Коммктрл. h)
description: Задает максимальную ширину окна подсказки.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Элементы управления Windows для TTM_SETMAXTIPWIDTH сообщений
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262194"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="4b244-104">\_Сообщение ТТМ сетмакстипвидс</span><span class="sxs-lookup"><span data-stu-id="4b244-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="4b244-105">Задает максимальную ширину окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="4b244-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b244-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b244-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b244-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4b244-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4b244-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4b244-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b244-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b244-110">Максимальная ширина окна подсказки, или значение-1, чтобы разрешить любую ширину.</span><span class="sxs-lookup"><span data-stu-id="4b244-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b244-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b244-111">Return value</span></span>

<span data-ttu-id="4b244-112">Возвращает предыдущую максимальную ширину всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="4b244-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b244-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b244-113">Remarks</span></span>

<span data-ttu-id="4b244-114">Значение максимальной ширины не указывает фактическую ширину окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="4b244-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="4b244-115">Вместо этого, если строка подсказки превышает максимальную ширину, элемент управления разбивает текст на несколько строк, используя пробелы для определения разрывов строк.</span><span class="sxs-lookup"><span data-stu-id="4b244-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="4b244-116">Если текст не может быть разбит на несколько строк, он отображается в одной строке, что может превысить максимальную ширину подсказки.</span><span class="sxs-lookup"><span data-stu-id="4b244-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b244-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4b244-117">Requirements</span></span>



| <span data-ttu-id="4b244-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4b244-118">Requirement</span></span> | <span data-ttu-id="4b244-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4b244-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b244-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b244-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b244-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b244-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b244-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b244-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b244-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b244-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b244-124">Header</span><span class="sxs-lookup"><span data-stu-id="4b244-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b244-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b244-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b244-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b244-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b244-127">**ТТМ \_ жетмакстипвидс**</span><span class="sxs-lookup"><span data-stu-id="4b244-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





