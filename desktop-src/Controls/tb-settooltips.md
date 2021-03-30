---
title: Сообщение TB_SETTOOLTIPS (Коммктрл. h)
description: Связывает элемент управления ToolTip с панелью инструментов.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Элементы управления Windows для TB_SETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071378"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="70756-104">\_Сообщение СЕТТУЛТИПС ТБ</span><span class="sxs-lookup"><span data-stu-id="70756-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="70756-105">Связывает элемент управления ToolTip с панелью инструментов.</span><span class="sxs-lookup"><span data-stu-id="70756-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="70756-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70756-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70756-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70756-108">Обработчик для элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="70756-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="70756-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70756-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="70756-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="70756-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70756-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70756-111">Return value</span></span>

<span data-ttu-id="70756-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="70756-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70756-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70756-113">Remarks</span></span>

<span data-ttu-id="70756-114">Все кнопки, добавленные на панель инструментов перед отправкой сообщения **\_ сеттултипс ТБ** , не будут зарегистрированы в элементе управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="70756-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="70756-115">Требования</span><span class="sxs-lookup"><span data-stu-id="70756-115">Requirements</span></span>



| <span data-ttu-id="70756-116">Требование</span><span class="sxs-lookup"><span data-stu-id="70756-116">Requirement</span></span> | <span data-ttu-id="70756-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70756-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70756-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70756-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70756-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70756-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70756-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70756-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70756-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70756-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70756-122">Header</span><span class="sxs-lookup"><span data-stu-id="70756-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70756-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="70756-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





