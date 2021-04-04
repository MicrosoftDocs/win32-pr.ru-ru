---
title: Сообщение LVM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкколор ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Элементы управления Windows для LVM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988907"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="ce4a4-105">\_Сообщение LVM сетбкколор</span><span class="sxs-lookup"><span data-stu-id="ce4a4-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="ce4a4-106">Задает цвет фона для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="ce4a4-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="ce4a4-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="ce4a4-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce4a4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce4a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4a4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce4a4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce4a4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ce4a4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce4a4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce4a4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4a4-112">Цвет фона для установки или значение CLR \_ None для отсутствия цвета фона.</span><span class="sxs-lookup"><span data-stu-id="ce4a4-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="ce4a4-113">Элементы управления "представление списка" с фоновыми цветами перерисуются значительно быстрее, чем без фоновых цветов.</span><span class="sxs-lookup"><span data-stu-id="ce4a4-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4a4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce4a4-114">Return value</span></span>

<span data-ttu-id="ce4a4-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ce4a4-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4a4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ce4a4-116">Requirements</span></span>



| <span data-ttu-id="ce4a4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ce4a4-117">Requirement</span></span> | <span data-ttu-id="ce4a4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ce4a4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4a4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce4a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4a4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce4a4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce4a4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce4a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4a4-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce4a4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce4a4-123">Header</span><span class="sxs-lookup"><span data-stu-id="ce4a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce4a4-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4a4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





