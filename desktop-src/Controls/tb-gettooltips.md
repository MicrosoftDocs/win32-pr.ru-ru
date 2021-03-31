---
title: Сообщение TB_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для элемента управления ToolTip (при наличии), связанного с панелью инструментов.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- Элементы управления Windows для TB_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071706"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="cd481-104">\_Сообщение о СОсказках в ТБ</span><span class="sxs-lookup"><span data-stu-id="cd481-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="cd481-105">Получает маркер для элемента управления ToolTip (при наличии), связанного с панелью инструментов.</span><span class="sxs-lookup"><span data-stu-id="cd481-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd481-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd481-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd481-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd481-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cd481-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cd481-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cd481-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd481-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cd481-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cd481-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd481-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd481-111">Return value</span></span>

<span data-ttu-id="cd481-112">Возвращает маркер для элемента управления ToolTip или **значение NULL** , если у панели инструментов нет связанной подсказки.</span><span class="sxs-lookup"><span data-stu-id="cd481-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd481-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cd481-113">Requirements</span></span>



| <span data-ttu-id="cd481-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cd481-114">Requirement</span></span> | <span data-ttu-id="cd481-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cd481-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd481-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd481-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd481-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd481-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd481-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd481-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd481-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd481-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd481-120">Header</span><span class="sxs-lookup"><span data-stu-id="cd481-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd481-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd481-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





