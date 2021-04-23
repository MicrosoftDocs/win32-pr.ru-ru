---
title: Сообщение TB_GETSTYLE (Коммктрл. h)
description: Извлекает стили, используемые в данный момент для элемента управления ToolBar.
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- Элементы управления Windows для TB_GETSTYLE сообщений
topic_type:
- apiref
api_name:
- TB_GETSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8de0addae729a4a8c641d21fd1771137d8c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492129"
---
# <a name="tb_getstyle-message"></a><span data-ttu-id="4bf65-104">\_Сообщение о стиле ТБ</span><span class="sxs-lookup"><span data-stu-id="4bf65-104">TB\_GETSTYLE message</span></span>

<span data-ttu-id="4bf65-105">Извлекает стили, используемые в данный момент для элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="4bf65-105">Retrieves the styles currently in use for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bf65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bf65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bf65-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4bf65-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4bf65-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4bf65-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bf65-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4bf65-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4bf65-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf65-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bf65-111">Return value</span></span>

<span data-ttu-id="4bf65-112">Возвращает значение **типа DWORD** , которое является сочетанием [стилей элементов управления панели инструментов](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4bf65-112">Returns a **DWORD** value that is a combination of [toolbar control styles](toolbar-control-and-button-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf65-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4bf65-113">Requirements</span></span>



| <span data-ttu-id="4bf65-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4bf65-114">Requirement</span></span> | <span data-ttu-id="4bf65-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4bf65-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf65-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bf65-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf65-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4bf65-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bf65-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bf65-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf65-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4bf65-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bf65-120">Header</span><span class="sxs-lookup"><span data-stu-id="4bf65-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bf65-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf65-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





