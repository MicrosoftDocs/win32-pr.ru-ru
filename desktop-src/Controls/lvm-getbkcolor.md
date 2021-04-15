---
title: Сообщение LVM_GETBKCOLOR (Коммктрл. h)
description: Возвращает цвет фона элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жетбкколор ListView.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- Элементы управления Windows для LVM_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489075"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="2e99e-105">\_Сообщение LVM жетбкколор</span><span class="sxs-lookup"><span data-stu-id="2e99e-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="2e99e-106">Возвращает цвет фона элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="2e99e-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="2e99e-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="2e99e-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e99e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e99e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e99e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e99e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e99e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2e99e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e99e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e99e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e99e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2e99e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e99e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e99e-113">Return value</span></span>

<span data-ttu-id="2e99e-114">Возвращает цвет фона элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="2e99e-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e99e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2e99e-115">Requirements</span></span>



| <span data-ttu-id="2e99e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2e99e-116">Requirement</span></span> | <span data-ttu-id="2e99e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2e99e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e99e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e99e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e99e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e99e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e99e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e99e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e99e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e99e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e99e-122">Header</span><span class="sxs-lookup"><span data-stu-id="2e99e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e99e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e99e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





