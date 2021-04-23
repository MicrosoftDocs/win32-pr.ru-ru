---
title: Сообщение LVM_UPDATE (Коммктрл. h)
description: Обновляет элемент представления списка. Если элемент управления "список" имеет \_ стиль АВТОУПОРЯДОЧИТЬ LVS, этот макрос приводит к упорядочиванию элемента управления "список". Это сообщение можно отправить явно или с помощью \_ макроса обновления ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Элементы управления Windows для LVM_UPDATE сообщений
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891497"
---
# <a name="lvm_update-message"></a><span data-ttu-id="7571b-106">\_Сообщение об обновлении LVM</span><span class="sxs-lookup"><span data-stu-id="7571b-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="7571b-107">Обновляет элемент представления списка.</span><span class="sxs-lookup"><span data-stu-id="7571b-107">Updates a list-view item.</span></span> <span data-ttu-id="7571b-108">Если элемент управления "список" имеет стиль [**\_ Автоупорядочить LVS**](list-view-window-styles.md) , этот макрос приводит к упорядочиванию элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="7571b-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="7571b-109">Это сообщение можно отправить явно или с помощью макроса [**\_ обновления ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .</span><span class="sxs-lookup"><span data-stu-id="7571b-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7571b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7571b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7571b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7571b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7571b-112">Индекс обновляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="7571b-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="7571b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7571b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7571b-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7571b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7571b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7571b-115">Return value</span></span>

<span data-ttu-id="7571b-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7571b-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7571b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7571b-117">Requirements</span></span>



| <span data-ttu-id="7571b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7571b-118">Requirement</span></span> | <span data-ttu-id="7571b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7571b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7571b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7571b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7571b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7571b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7571b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7571b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7571b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7571b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7571b-124">Header</span><span class="sxs-lookup"><span data-stu-id="7571b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7571b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7571b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





