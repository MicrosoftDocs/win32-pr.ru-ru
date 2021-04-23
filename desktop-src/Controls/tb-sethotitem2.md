---
title: Сообщение TB_SETHOTITEM2 (Коммктрл. h)
description: Задает горячий элемент на панели инструментов.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Элементы управления Windows для TB_SETHOTITEM2 сообщений
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803137"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="6757b-104">\_Сообщение SETHOTITEM2 ТБ</span><span class="sxs-lookup"><span data-stu-id="6757b-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="6757b-105">Задает горячий элемент на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="6757b-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6757b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6757b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6757b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6757b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6757b-108">Индекс элемента, который будет активным.</span><span class="sxs-lookup"><span data-stu-id="6757b-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="6757b-109">Если это значение равно-1, ни один из элементов не будет активным.</span><span class="sxs-lookup"><span data-stu-id="6757b-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="6757b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6757b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6757b-111">Сочетание \_ флагов хикф XXX.</span><span class="sxs-lookup"><span data-stu-id="6757b-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="6757b-112">См. <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**нмтбхотитем**</a>.</span><span class="sxs-lookup"><span data-stu-id="6757b-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6757b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6757b-113">Return value</span></span>

<span data-ttu-id="6757b-114">Возвращает индекс предыдущего горячего элемента или значение-1, если элемент не был активным.</span><span class="sxs-lookup"><span data-stu-id="6757b-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6757b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6757b-115">Remarks</span></span>

<span data-ttu-id="6757b-116">Поведение этого сообщения не определено для панелей инструментов, не имеющих [**\_ неструктурированного стиля тбстиле**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6757b-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6757b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6757b-117">Requirements</span></span>



| <span data-ttu-id="6757b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6757b-118">Requirement</span></span> | <span data-ttu-id="6757b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6757b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6757b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6757b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6757b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6757b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6757b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6757b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6757b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6757b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6757b-124">Header</span><span class="sxs-lookup"><span data-stu-id="6757b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6757b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6757b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





