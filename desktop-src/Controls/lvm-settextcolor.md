---
title: Сообщение LVM_SETTEXTCOLOR (Коммктрл. h)
description: Задает цвет текста для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстколор ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Элементы управления Windows для LVM_SETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135590"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="8a8c1-105">\_Сообщение LVM сеттекстколор</span><span class="sxs-lookup"><span data-stu-id="8a8c1-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="8a8c1-106">Задает цвет текста для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="8a8c1-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="8a8c1-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сеттекстколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="8a8c1-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a8c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a8c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a8c1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8a8c1-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8a8c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a8c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a8c1-112">Объект [**COLORREF**](/windows/desktop/gdi/colorref) , указывающий новый цвет текста.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a8c1-113">Return value</span></span>

<span data-ttu-id="8a8c1-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8a8c1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8c1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8a8c1-115">Requirements</span></span>



| <span data-ttu-id="8a8c1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8a8c1-116">Requirement</span></span> | <span data-ttu-id="8a8c1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8a8c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8c1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a8c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8c1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a8c1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a8c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8c1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a8c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a8c1-122">Header</span><span class="sxs-lookup"><span data-stu-id="8a8c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a8c1-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a8c1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

