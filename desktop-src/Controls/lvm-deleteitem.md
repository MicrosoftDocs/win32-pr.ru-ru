---
title: Сообщение LVM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса DeleteItem ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- Элементы управления Windows для LVM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135138"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="665d7-105">\_Сообщение LVM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="665d7-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="665d7-106">Удаляет элемент из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="665d7-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="665d7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ DeleteItem ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="665d7-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="665d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="665d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="665d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="665d7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="665d7-110">Индекс удаляемого элемента списка.</span><span class="sxs-lookup"><span data-stu-id="665d7-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="665d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="665d7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="665d7-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="665d7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="665d7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="665d7-113">Return value</span></span>

<span data-ttu-id="665d7-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="665d7-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="665d7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="665d7-115">Requirements</span></span>



| <span data-ttu-id="665d7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="665d7-116">Requirement</span></span> | <span data-ttu-id="665d7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="665d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="665d7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="665d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="665d7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="665d7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="665d7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="665d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="665d7-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="665d7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="665d7-122">Header</span><span class="sxs-lookup"><span data-stu-id="665d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="665d7-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="665d7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





