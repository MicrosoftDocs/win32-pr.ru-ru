---
title: Сообщение LVM_SETTEXTBKCOLOR (Коммктрл. h)
description: Задает цвет фона для текста в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстбкколор ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Элементы управления Windows для LVM_SETTEXTBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071456"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="27fac-105">\_Сообщение LVM сеттекстбкколор</span><span class="sxs-lookup"><span data-stu-id="27fac-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="27fac-106">Задает цвет фона для текста в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="27fac-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="27fac-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сеттекстбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="27fac-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27fac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="27fac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27fac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27fac-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="27fac-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="27fac-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="27fac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27fac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27fac-112">Новый цвет фона текста.</span><span class="sxs-lookup"><span data-stu-id="27fac-112">New text background color.</span></span> <span data-ttu-id="27fac-113">Это может быть "CLR \_ None" для отсутствия цвета фона.</span><span class="sxs-lookup"><span data-stu-id="27fac-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27fac-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27fac-114">Return value</span></span>

<span data-ttu-id="27fac-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="27fac-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="27fac-116">Requirements</span></span>



| <span data-ttu-id="27fac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="27fac-117">Requirement</span></span> | <span data-ttu-id="27fac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="27fac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27fac-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27fac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27fac-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27fac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27fac-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27fac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27fac-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27fac-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27fac-123">Header</span><span class="sxs-lookup"><span data-stu-id="27fac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="27fac-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="27fac-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





